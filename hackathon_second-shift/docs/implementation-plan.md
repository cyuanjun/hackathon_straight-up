# Implementation Plan — Second Shift

Companion to `second-shift.md`. The spec is the *what* and *why*; this document is the *how* — actor flows, onboarding, and the diagrams a builder needs to trace any scenario end-to-end before writing code.

---

## Table of contents

1. [Overview](#1-overview)
2. [System architecture](#2-system-architecture)
3. [Onboarding flow](#3-onboarding-flow)
4. [User flows](#4-user-flows)
5. [Daily + weekly cycles](#5-daily--weekly-cycles)
6. [Escalation ladder](#6-escalation-ladder)
7. [Privacy / visibility map](#7-privacy--visibility-map)
8. [Voice agent pipeline](#8-voice-agent-pipeline)
9. [Build sequencing](#9-build-sequencing)
10. [Open questions](#10-open-questions)

---

## 1. Overview

Second Shift automates the unpaid caregiver work dual-income families do between their day jobs, their own kids, and their ageing parents. The primary user is the **sandwich-generation adult child**, not the elderly parent. The product redistributes load across siblings, surfaces signals to the family GP, and provides a persona-driven voice companion for the parent — all while keeping the parent's raw replies private and the agent's actions auditable.

### Actors

| Actor | Role in product | Primary surface |
|---|---|---|
| **Mdm Lim** (elderly parent) | Receives voice check-ins, voice-replies; unit being cared for | Private Telegram voice thread with Aunty May |
| **Sarah** (primary caregiver daughter) | Installs bot; default-follow-up person; usually carries the most load | Shared family Telegram group + on-duty DMs |
| **Marcus** (rotating sibling) | On-duty on assigned days; receives @-mentions + drafted nudges | Shared family Telegram group |
| **Spouse / less-involved family member** | Observes load; can opt in to rotation | Shared family Telegram group (read-only default) |
| **Family GP** (polyclinic) | Consumes next-visit briefing at appointments | PDF / QR at visit — no inbound channel from agent |
| **Aunty May** | AI persona — interface, not an actor with agency | Voice messages to parent; plain @-mentions to family |

### Surfaces

| Surface | Audience | Medium | Content |
|---|---|---|---|
| **Parent surface** | Mdm Lim only | Telegram voice messages (async) | Check-ins, nudges, relayed family messages |
| **Family surface** | Siblings + spouse | Shared Telegram group | Events, outcomes, load dashboard, drafts-to-send, weekly digest |
| **GP surface** | Polyclinic doctor | PDF (printed) / QR code | 6-week briefing: adherence, symptoms, anomalies |

### Guardrails (recap)

Six non-negotiables, enforced at the code level, not just the prompt:

1. **AI disclosure on demand** — "Are you a real person?" → "No, I'm an AI." Always. Immediately.
2. **No clinical agency** — no medical advice, no health claims, no impersonating a nurse/doctor. Medical topics → log for GP briefing + ping on-duty sibling. The agent **never** contacts the GP directly.
3. **Escalation ladder by blast radius** — see [§6](#6-escalation-ladder).
4. **Signed receipts** — every agent action produces an ed25519-signed ledger entry visible to all siblings.
5. **Parent privacy** — her raw voice replies stay in the private Aunty May thread. Family sees outcomes/summaries only.
6. **Persona stability** — Aunty May never emulates a real person (e.g. a late spouse); stable voice/memory across sessions.

### Scope anchor

**The 60-second hero demo in the spec is the MVP definition.** Every feature in this plan exists because it appears in that demo or is required for it to run end-to-end. If a proposed feature doesn't trace back to the hero scene, it is roadmap — not this week.

---

## 2. System architecture

```
    ┌──────────────────────────────────────────────────────────────────┐
    │                       INGEST (multimodal)                         │
    │                                                                   │
    │   Parent voice ──┐    SMS / email ──┐    Photo (bill, doc) ──┐    │
    │   (Telegram)     │    (webhooks)    │    (Telegram)          │    │
    └──────────────────┼──────────────────┼────────────────────────┼────┘
                       │                  │                        │
                       ▼                  ▼                        ▼
                  ┌─────────────────────────────────────────────────┐
                  │  CLASSIFY + EXTRACT  (GPT-4o-mini — cheap/fast) │
                  │  {medical, financial, social, admin, escalate}  │
                  └────────────────────────┬────────────────────────┘
                                           │
                  ┌────────────────────────▼────────────────────────┐
                  │  PATTERN + ANOMALY REASONING                    │
                  │  • adherence patterns (missed doses, time-of-day) │
                  │  • symptom diary recurrences (knee pain 5 days)  │
                  │  • bill anomalies (+40% electricity)             │
                  │  • sibling load graph (who handled what, when)   │
                  └────────────────────────┬────────────────────────┘
                                           │
                  ┌────────────────────────▼────────────────────────┐
                  │  PLAN + DECIDE  (GPT-5 — reasoning)              │
                  │  blast radius → { auto-act | draft | escalate }  │
                  └───────────┬───────────┬────────────┬────────────┘
                              │           │            │
             ┌────────────────▼──┐   ┌────▼──────┐    ┌▼──────────────────┐
             │  TOOL EXECUTION   │   │  NUDGE    │    │  GP BRIEFING      │
             │  (function calls) │   │  GEN      │    │  (longitudinal)    │
             │  • Aunty May voice│   │  drafts   │    │  → structured PDF  │
             │    (ElevenLabs)   │   │  in       │    │  at visit          │
             │  • bill payment   │   │  family's │    │                    │
             │  • appt booking   │   │  voice    │    │                    │
             └────────┬──────────┘   └─────┬─────┘    └──────────┬─────────┘
                      │                    │                     │
                      └────────────────────┼─────────────────────┘
                                           ▼
                  ┌──────────────────────────────────────────────┐
                  │  SIGNED RECEIPTS LEDGER  (ed25519 MVP)       │
                  │  {agent_id, action, ts, blast_radius,        │
                  │   rollback_token, actor_visible_to}          │
                  └────────────────────────┬─────────────────────┘
                                           │
                  ┌────────────────────────▼─────────────────────┐
                  │  DIGESTS + ALERTS                             │
                  │  • family group: event posts + weekly digest  │
                  │  • parent: warm voice nudges                  │
                  │  • GP: pre-visit briefing PDF                 │
                  └───────────────────────────────────────────────┘
```

Each arrow is a named decision point — useful for the architecture slide.

---

## 3. Onboarding flow

One-time, ~10 minutes. Runs entirely in the family Telegram group plus one parent handoff. Every step produces a signed receipt so consent is auditable.

```
  Sarah (primary caregiver)           Family group            Mdm Lim (parent)
          │                                │                          │
  ┌───────┴────────┐                       │                          │
  │ 0. /start bot  │                       │                          │
  │    in family   │                       │                          │
  │    group       │                       │                          │
  └───────┬────────┘                       │                          │
          │ bot added ─────────────────────▶                          │
          │                                │                          │
          │                    ┌───────────┴──────────┐                │
          │                    │ 1. CONSENT PROMPT    │                │
          │                    │ "Tap ✓ to consent"   │                │
          │                    │ for each member      │                │
          │                    │ (inline button)      │                │
          │                    └───────────┬──────────┘                │
          │                                │ receipt per consent       │
          │                                │                           │
  ┌───────┴────────┐                       │                           │
  │ 2. PARENT DATA │                       │                           │
  │    form-driven │                       │                           │
  │    • meds      │                       │                           │
  │    • appts     │                       │                           │
  │    • bills     │                       │                           │
  │    • rotation  │                       │                           │
  │    • language  │                       │                           │
  └───────┬────────┘                       │                           │
          │                                │                           │
          │                                │                           │
          │                                │    ┌──────────────────────┴────────┐
          │                                │    │ 3. PARENT INTRO (voice msg)   │
          │                                │    │ "你好 Auntie Lim, 我是        │
          │                                │    │  Aunty May, an AI helper to   │
          │                                │    │  keep you safe. 不是真人 ah." │
          │                                │    │ explicit AI disclosure        │
          │                                │    └──────────┬────────────────────┘
          │                                │               │ parent replies OR
          │                                │               │ silent > 24h → phone
          │                                │               │ handoff to Sarah
          │                                │               │
          │                    ┌───────────┴──────────┐    │
          │                    │ 4. VISIBILITY CONFIG │    │
          │                    │ defaults shown;      │    │
          │                    │ tap to adjust        │    │
          │                    └───────────┬──────────┘    │
          │                                │               │
          │                    ┌───────────┴──────────┐    │
          │                    │ 5. FIRST CYCLE ARMED │    │
          │                    │ "Next check-in:      │    │
          │                    │  Tue 8:45 AM"        │    │
          │                    └──────────────────────┘    │
          │                                                │
```

### Step detail

- **Step 0 — Initiation.** Primary caregiver (usually Sarah) adds the bot to the family group and types `/start`.
- **Step 1 — Family consent.** Every member of the group gets an inline "I consent" button. Bot records consent per user as a signed receipt. Consent is **per member, not group-level** — a family member can decline without leaving the group.
- **Step 2 — Parent data entry.** Form-driven (Telegram WebApp or simple inline form). Fields: medications + schedule, polyclinic appointments, bill accounts (email/SMS to forward), on-duty rotation pattern (days of week, round-robin, custom), language (MVP: Mandarin or English), parent's preferred address form (e.g. "Auntie Lim" vs given name).
- **Step 3 — Parent introduction.** Aunty May sends her first voice message to Mdm Lim in the chosen language. Opens with warm greeting + **explicit AI disclosure** (see script in spec §Guardrails). If parent silent > 24h, escalate to primary caregiver to do an in-person or phone handoff; bot does NOT retry automatically.
- **Step 4 — Visibility configuration.** Family agrees in-group on defaults. Built-in defaults: all events visible to all siblings; parent's raw voice replies NEVER leave her private thread; load dashboard visible to all. Individual privacy is opt-in only.
- **Step 5 — First daily cycle armed.** Bot confirms next morning's check-in time and goes quiet.

### Sample signed receipt

```json
{
  "receipt_id": "r_01HXX3YQ8PQK2N...",
  "agent_id": "second-shift-bot",
  "action": "consent.record",
  "subject": "user:tg_123456789",
  "timestamp": "2026-04-20T14:02:31+08:00",
  "blast_radius": "low",
  "details": { "consent_type": "family_member", "version": "1.0" },
  "visible_to": ["family_group:987654321"],
  "signature": "ed25519:3YqL8...zN2",
  "rollback_token": "rb_consent_01HXX3YQ8PQK2N"
}
```

Every action in the system — from a consent tap to a bill payment to a nudge draft — produces one of these. The receipts feed is what Sandy will ask to see.

---

## 4. User flows

Each flow is a short sequence diagram + numbered steps. All flows assume onboarding is complete.

### 4.1 Mdm Lim (elderly parent) — daily cycle

```
  Aunty May                              Mdm Lim
      │                                     │
      │  8:45 AM voice message (Mandarin)   │
      │  "早安啊, 吃了早餐和早药吗?"          │
      ├────────────────────────────────────▶│
      │                                     │
      │                                     │ records voice reply:
      │                                     │ "吃了早餐" (breakfast yes,
      │                                     │  meds not mentioned)
      │◀────────────────────────────────────┤
      │                                     │
      │  STT → classify → meds unconfirmed  │
      │  warm ack: "好, 记得吃药, 我等下     │
      │  再 check"                           │
      ├────────────────────────────────────▶│
      │                                     │
      │  (15-min confirmation window)       │
      │                                     │
      │  if unconfirmed → post to family    │
      │  (Mdm Lim is NOT notified)          │
      │                                     │
      │  9:14 AM check-back                 │
      │  "Auntie Lim, 吃了吗?"               │
      ├────────────────────────────────────▶│
      │                                     │
      │                                     │ "哎哟, 刚才忘了. 现在吃了."
      │◀────────────────────────────────────┤
      │                                     │
      │  STT → confirmed → resolution posts │
      │  to family group (she doesn't see)  │
      │                                     │
```

**Ad-hoc paths:**
- Parent voice-notes a symptom ("今天脚痛") → logged to diary + added to next-visit briefing; if recurrence pattern detected (e.g. 5 days in a row), flagged to family group.
- Parent asks to talk to a family member ("叫 Sarah 打电话给我") → Aunty May posts to family group, tags appropriate person.
- Parent raises heavy topic (death, grief, end-of-life) → Aunty May acknowledges briefly, does NOT engage as therapist, routes to on-duty sibling.
- Parent asks "are you a real person?" → disclosure script fires immediately.

**Privacy line:** Mdm Lim's voice content never enters the family group. Only outcome states ("morning meds confirmed 09:14") and anomaly summaries (classified, redacted) do.

### 4.2 Sarah (primary caregiver) — default path

```
  Family group                          Sarah (Bukit Timah, in stand-up)
      │                                            │
      │  9:02 AM event post:                       │
      │  "Aunty May's check-in:                    │
      │   breakfast ✓, morning meds ✗.             │
      │   @Marcus on-duty Tue. Draft ⬇️"            │
      │                                            │
      │  (Sarah is NOT @-mentioned; sees but       │
      │   isn't paged — stays in meeting)          │
      │                                            │
      │  9:14 AM resolution post: "✓ confirmed"    │
      │                                            │
      │  (Sarah glances at it as stand-up ends)    │
      │                                            │
      ...
      │  12:30 PM: "Electricity bill +40%.         │
      │   Fan overnight x3 last week. @Sarah       │
      │   you're free at lunch. Draft ⬇️"           │
      │                                            │
      │                                            │ reads drafted message,
      │                                            │ sends to Ma privately,
      │                                            │ taps ✓ Sent in group
      │                                            │
```

**On-duty days (her rotation):** mechanics identical to Marcus's flow (§4.3). **Weekly digest (Friday evening):** receives load dashboard — who handled what, notable events, upcoming. **Pre-visit:** if accompanying to polyclinic, receives briefing PDF the evening before.

### 4.3 Marcus (rotating sibling) — on-duty path

```
  Family group                          Marcus (shifts at Changi)
      │                                            │
      │  9:02 AM event post w/ @-mention           │
      │  "@Marcus — you're on-duty Tuesdays.       │
      │   Morning meds unconfirmed. 3rd this       │
      │   week, logged for Sat GP. Draft ⬇️"        │
      │                                            │
      │  ┌────────────────────────────────┐        │
      │  │ Drafted nudge (in family voice)│        │
      │  │ "妈, 吃药了吗?"                 │        │
      │  │ [Copy]  [Send as DM to Ma]     │        │
      │  └────────────────────────────────┘        │
      ├───────────────────────────────────────────▶│
      │                                            │ taps [Copy]
      │                                            │ opens DM w/ Ma
      │                                            │ sends
      │                                            │ returns to group
      │                                            │ taps ✓ Sent
      │◀───────────────────────────────────────────┤
      │                                            │
      │  "Marcus sent the nudge at 09:03"           │
      │  (visible to whole family; load log        │
      │   credit to Marcus, not Sarah)             │
      │                                            │
```

**The AIF wedge:** the drafted nudge is learned from the family's prior messages — tone, vocatives, code-switch pattern. Marcus doesn't have to think about *what to say* or *how to soften it* — that's the invisible emotional labour Sarah normally does. He only does the mechanical part (copy-send-✓), and credit lands fairly in the load graph.

**Off-duty days:** Marcus sees all group events but is not @-mentioned. He can still step in; if he does, load graph credits him.

### 4.4 Spouse / less-involved family member

Read-only by default. Sees:
- All event posts (no @-mention → no push notification)
- Weekly digest + load dashboard — **this is the moment the invisible labour becomes visible**
- Can opt into the rotation at any time via `/optin` (receives @-mentions on assigned days thereafter)
- Can opt out of specific categories (e.g. "pings only if high-priority") without leaving the group

No forced participation. The load dashboard alone is the C4 AIF payload.

### 4.5 Family GP / polyclinic doctor

```
  Second Shift backend                  Family GP
         │                                   │
         │  T-24h before appointment:        │
         │  generate 6-week briefing PDF     │
         │  (adherence patterns + symptom    │
         │   recurrences + anomalies +       │
         │   family notes)                   │
         │                                   │
         │  → PDF to Sarah (accompanying)    │
         │  → QR code version                 │
         │                                   │
         │                                   │
         │  At visit: Sarah hands over /     │
         │  doctor scans QR                  │
         ├──────────────────────────────────▶│
         │                                   │
         │                                   │ reads structured briefing,
         │                                   │ asks targeted questions,
         │                                   │ 2-min consult is now
         │                                   │ data-rich
         │                                   │
         │  (No return channel. Agent does   │
         │   NOT message the GP. GP notes go │
         │   back via existing polyclinic    │
         │   systems, not via our bot.)      │
         │                                   │
```

**One artifact per visit**, never a continuous feed. This keeps us clear of Wanting's "AI doctor" concern — we're a briefing generator, not a clinical agent.

---

## 5. Daily + weekly cycles

### 5.1 Daily cycle (full sequence)

```
  08:45  Aunty May → Mdm Lim: morning voice check-in
  08:46  Mdm Lim voice reply → STT → classify
  08:47  Warm ack back to Mdm Lim (confirmations logged)
  09:00  Confirmation window closes
         ├─ all confirmed → silent log, no family post
         └─ unconfirmed   → post to family group + @on-duty + drafted nudge
  09:03  On-duty sibling sends nudge privately, taps ✓ Sent in group
  09:14  Aunty May check-back with Mdm Lim
         ├─ confirmed now → resolution post to family
         └─ still missing → escalate one tier
  ...    Ad-hoc events throughout the day:
         • symptom voice-note     → diary + pattern check
         • bill anomaly           → family post + @on-duty
         • appointment approach   → reminder to parent + accompanier
         • distress signal        → route to on-duty sibling
  21:00  End-of-day tidy: receipts ledger written; nothing posted
```

### 5.2 Weekly cycle

```
  Mon→Thu   daily cycles; load graph accumulates
  Fri 18:00 weekly digest posted to family group:
            • load distribution (bar chart: who handled what)
            • notable events (anomalies, unusual spend, symptom clusters)
            • upcoming: next week's appointments + admin
  Sun       rotation rolls over; next week's on-duty assignments posted
  (pre-visit) T-24h before any polyclinic appointment:
            • briefing PDF generated from last 6 weeks
            • sent to accompanier; QR code ready for GP
```

---

## 6. Escalation ladder

Blast radius determines autonomy. The agent chooses the tier deterministically from action-type; LLM never self-promotes across tiers.

```
                    ┌───────────────────────────────┐
                    │      INCOMING EVENT           │
                    └────────────────┬──────────────┘
                                     │
          ┌──────────────────────────┼──────────────────────────┐
          │                          │                          │
          │                  clinical mention?                   │
          │                          │                          │
          │                          ▼ yes                      │
          │              ┌────────────────────────┐             │
          │              │ CLINICAL TIER          │             │
          │              │ ─────────────────      │             │
          │              │ • NEVER acts           │             │
          │              │ • logs to GP briefing  │             │
          │              │ • pings on-duty sib    │             │
          │              │ • "I'm not a doctor"   │             │
          │              │   script to parent     │             │
          │              │ Example: parent says   │             │
          │              │ "my chest hurts"       │             │
          │              └────────────────────────┘             │
          │                                                      │
          ▼ non-clinical                                         │
  ┌───────────────┐                                              │
  │ blast radius? │                                              │
  └──────┬────────┘                                              │
         │                                                        │
    ┌────┼─────┬─────────┬──────────────┐                        │
    │    │     │         │              │                        │
    ▼    │     ▼         │              ▼                        │
  LOW   │   MEDIUM       │             HIGH                      │
        │                │                                        │
  ┌─────────────┐  ┌───────────────────┐  ┌──────────────────┐   │
  │ auto-act    │  │ draft to family   │  │ NO action until  │   │
  │ + log       │  │ group, @on-duty,  │  │ explicit family- │   │
  │             │  │ wait for human    │  │ group approval   │   │
  │ • reminder  │  │ send              │  │                  │   │
  │ • log entry │  │                   │  │ • large payment  │   │
  │ • diary     │  │ • message to Ma   │  │ • appt change    │   │
  │ • digest    │  │ • bill < S$200    │  │ • legal / banking│   │
  └─────────────┘  └───────────────────┘  └──────────────────┘   │
```

**Rule:** when in doubt, tier up. Every tier transition generates a signed receipt. High-tier approvals require an explicit ✓ from a family member, not just silence.

---

## 7. Privacy / visibility map

Who sees what. One table, memorise it; this is the slide Sandy studies.

|                              | Mdm Lim (parent) | Family group | GP |
|------------------------------|:----------------:|:------------:|:--:|
| Her own voice messages       | ✓                |              |    |
| Her voice replies (raw audio)| ✓                |              |    |
| Transcripts of her replies   | ✓ (not shown)    | redacted only| ✓ summary |
| Confirmation outcomes        |                  | ✓            | ✓ |
| Adherence patterns           |                  | ✓            | ✓ |
| Symptom diary recurrences    |                  | ✓ summarised | ✓ full |
| Bill anomalies               |                  | ✓            |    |
| Load dashboard (who did what)|                  | ✓            |    |
| Signed receipts feed         |                  | ✓            |    |
| Weekly digest                |                  | ✓            |    |
| Briefing PDF                 |                  | (accompanier)| ✓ |
| Who else is in the family grp|                  | ✓            |    |
| AI disclosure                | ✓ (on demand)    | ✓            | ✓ (PDF states it) |

```
                      ┌─────────────────────────────┐
                      │      PRIVATE THREAD         │
                      │  Aunty May ⇄ Mdm Lim         │
                      │  (voice in/out, raw audio)  │
                      └──────────────┬──────────────┘
                                     │
                                     │ only: outcomes,
                                     │ classified signals,
                                     │ summarised content
                                     ▼
                      ┌─────────────────────────────┐
                      │      FAMILY GROUP           │
                      │  siblings + spouse          │
                      │  (events, dashboard,        │
                      │   drafts, digests)          │
                      └──────────────┬──────────────┘
                                     │
                                     │ per-visit only,
                                     │ structured summary
                                     ▼
                      ┌─────────────────────────────┐
                      │      GP BRIEFING PDF        │
                      │  at polyclinic visits       │
                      └─────────────────────────────┘
```

Data flows downward only. The GP never gets live stream; the family never gets raw voice; the parent never sees the family group.

---

## 8. Voice agent pipeline

Reference diagram — stack rationale lives in `second-shift.md` §Tech stack choices.

```
  Mdm Lim records voice in Telegram
           │
           ▼
  Telegram Bot API — voice message handler (opus)
           │
           ▼
  MERaLiON-AudioLLM — STT (Mandarin + English code-switch)
           │   ↓ if language-confidence < threshold
           └── Whisper-large-v3 fallback
           │
           ▼
  GPT-5 dialogue — persona, memory, tone, script rails
           │   (tool use: family_post, diary_log, escalate)
           ▼
  ElevenLabs Multilingual v2 — TTS (Mandarin + English voices)
           │
           ▼
  Telegram Bot API — sendVoice
           │
           ▼
  Mdm Lim plays; hears Aunty May (stable voice across sessions)
```

**MVP languages:** Mandarin + English only. Hokkien / Malay / Tamil are phase-2 roadmap.

---

## 9. Build sequencing

Aligned with the week plan in `second-shift.md`. One-line per day for quick scan.

| Day | Build target | Interview target | Risk to watch |
|---|---|---|---|
| **Mon 20 Apr** | Repo, Supabase, Telegram bot, LLM auth, scaffolding; ingest pipeline (voice → classify → log) | Book all Tue/Wed slots | Scope slipping past hero demo |
| **Tue 21 Apr** | Sibling rotation + load graph; Aunty May voice loop end-to-end (STT→LLM→TTS) | 2 of 3 first interviews | Voice loop latency at demo |
| **Wed 22 Apr** | Bills anomaly + weekly digest; signed receipts; tool-use layer (polyclinic + bill mocks) | 6 interviews total by EOD | Mock/real boundary unclear |
| **Thu 23 Apr** | Hero demo runs front-to-back; fix top 3 bugs; family-group UI polish; rehearse pitch @ 3min | — | Persona slippage into clinical |
| **Fri 24 Apr** | Buffer day; record backup demo video; deck polish | — | Over-tweaking; sleep instead |
| **Sat 25 Apr** | Submit by 12:00 PM; pitches at 1:00 PM | — | Audio/video on org laptop |

---

## 10. Open questions

Running list for the builder. Resolve as they block work. Keep < 10 items.

1. **Bot hosting account** — which Telegram account owns the bot token? (affects handover if team splits)
2. **Backend hosting** — FastAPI on Fly.io, Render, or Railway for the 5-day window?
3. **Voice storage** — where do raw opus files live? Supabase Storage vs S3; retention policy for parent voice (default: 30 days, deletable on request).
4. **MERaLiON access** — is the model accessible via hosted API or do we self-host? Fallback plan if latency is poor.
5. **Load-graph algorithm** — round-robin with load-weighting, or pure fair-share? Need a one-liner for the pitch.
6. **Rotation conflict resolution** — what happens when on-duty person is unreachable (DND, abroad)? Auto-failover to next sibling after N minutes?
7. **Bill ingestion** — email forwarding address vs SMS gateway? For the MVP, forwarding is simpler.
8. **Briefing PDF generation** — WeasyPrint, LaTeX, or HTML-to-PDF? Pick the least fragile.
9. **Mock polyclinic API** — hand-rolled or HealthHub sandbox if we can get access in 5 days?
10. **Demo-day failover** — pre-record the voice-exchange clip as a backup video; decide the cutoff (e.g. if live voice fails within first 10 seconds, switch to video).

---

*This plan is a companion to `second-shift.md`. When they disagree, the spec wins — update this file to match.*
