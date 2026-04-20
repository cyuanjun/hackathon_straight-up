# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository state

Pre-build. Planning material lives in `docs/`:
- `docs/second-shift.md` — the locked scope/spec for a 5-day hackathon build (Mon 2026-04-20 → Sat 2026-04-25, submission Fri 12:00 PM). Defines scope, guardrails, demo script, and stack decisions.
- `docs/implementation-plan.md` — companion plan: per-user flows, onboarding flow, daily/weekly cycles, privacy map, open questions. Read this to trace any scenario end-to-end before coding.

**Read both before writing any code.** When they disagree, the spec (`second-shift.md`) wins.

Parent directory (`../`) holds hackathon context referenced by the spec:
- `challenge-statements.md` — the 25 hackathon challenges and judge panel
- `ideas.md`, `ideas-per-challenge.md` — ideation history; the spec stacks ideas 1 + 3 + 5 + 18 from there

## Product in one line

Automates the "second shift" for sandwich-generation caregivers: medical workflow + family coordination + financial ops + admin, around an ageing parent. Primary user is the **adult child**, not the elderly parent. There are two surfaces: (a) elderly parent ⇄ "Aunty May" persona over Telegram voice messages, (b) family group chat on Telegram for siblings/spouse.

## Non-negotiable product guardrails

These are pitch-critical and will be probed in Q&A. Don't soften them in code or copy:

- **AI disclosure on demand** — if anyone asks "are you a real person?", Aunty May answers "No, I'm an AI" immediately. Never accepts requests to pretend to be human.
- **No clinical agency** — never give medical advice (even "drink more water"), never impersonate a nurse/doctor, never make health claims. Medical topics route to GP briefing + on-duty sibling; the agent does NOT call the GP itself.
- **Blast-radius escalation ladder** — low: auto-act; medium (msg to parent, bill < S$200): draft for family approval; high (large payment, med/legal): no action without explicit family-group approval; clinical: never acts, logs for GP.
- **Signed receipts** — every agent action produces a signed ledger entry (ed25519 for MVP, C2PA aspirational) visible to all siblings.
- **Parent privacy** — parent's voice replies stay in the private Aunty May thread. Family group sees outcomes/summaries only, never raw voice content.
- **Persona stability** — Aunty May never emulates a real person (e.g. a late spouse). Warm, SG-English with Mandarin; not saccharine, not clinical.

## Planned tech stack

When implementing, default to these unless there's a specific reason to deviate (spec rationale in `docs/second-shift.md`):

| Layer | Choice |
|---|---|
| Backend | Python + FastAPI |
| Reasoning LLM | GPT-5 (primary), GPT-4o-mini (fast routing/classification) |
| STT | MERaLiON-AudioLLM (primary, SG-first), Whisper-large-v3 (fallback) |
| TTS | ElevenLabs Multilingual v2 |
| DB | Supabase (Postgres + RLS) |
| Frontend | Next.js + Tailwind — **family group view only**; parent surface lives inside Telegram |
| Messaging | Telegram Bot API (`sendVoice` / `voice` handler) — **not WhatsApp** (provisioning > 1 week) |
| Tool use | OpenAI function calling + MCP for external integrations |
| Signing | ed25519 for MVP receipts feed |

**MVP language scope: Mandarin + English only.** Hokkien/Malay/Tamil are phase-2 roadmap, not hackathon scope.

## What must be real vs mocked

The spec is explicit about this — respect it, scope creep kills the demo:

- **Must be real:** Telegram bot (both family-group messages AND Aunty May voice exchange — same transport, two surfaces); signed receipts feed
- **Mocked with real UI:** polyclinic appointment booking, bill ingestion from email/SMS, bill payment flow
- **Slide-only (do not build):** deep polyclinic/insurance/banking integrations, multi-family fleet mgmt, CareShield/MediSave/CPF integrations

## The hero demo is the scope anchor

The 60-second scene in `docs/second-shift.md` ("Hero demo script") is the live demo. Any feature not required to make that scene run front-to-back is roadmap, not MVP. When in doubt about whether to build something, check: does the hero demo need it?

## AI pipeline shape (for Nishith's "load-bearing AI" bar)

5–7 step agentic pipeline — ingest → classify/extract → pattern+anomaly reasoning → decide/plan → tool exec / nudge gen / GP briefing → signed receipts → digest. Each arrow should have an explicit decision point (auto-act / draft-for-approval / escalate / hold). Avoid any single "Claude does it" shortcut — show tool schemas and human-in-the-loop gates.

## Working conventions

- No code yet — when adding it, create directories rather than piling files into the root.
- The parent repo `.gitignore` already covers macOS cruft (`.DS_Store`, etc.). Add language-specific ignores as stacks land.
- Git user is `cyuanjun`; main branch is `main`; commits in this repo so far are doc-only.
