# Ideas

Generated from `challenge-statements.md` — each idea is grounded in the archetypes, routes around the "done-to-death" defaults, and maps to real panel champions. Each card is self-contained so you can pull any one into a separate terminal for a deep-dive.

---

## TL;DR — top 5

Each of these has ≥3 panel champions, a clear 5–7 step AI pipeline, SEA-specific grounding, isn't on the done-to-death list, and is demoable in a week. Since 67% of rubric score is Challenge-Solution Fit + Tech Execution, these are the structurally safest bets.

1. **[Filial Proxy](#1-filial-proxy)** — A4 + D4 + E2. Bing Wen + Wanting + Sandy. Uniquely SEA (overseas diaspora + filial piety). CareShield/MediSave admin agent for overseas adult children.
2. **[Numbers Honestly](#2-numbers-honestly)** — D6 (AIF). Janet + Hester + Wanting. Triple-champion AIF tailwind. RAG-grounded fertility + career simulator with *honest uncertainty*.
3. **[Fair Share Agent](#3-fair-share-agent)** — C4 (AIF) + C3. Janet + Hester + Gabrielle. Absorbs coordination labor, doesn't just measure it.
4. **[Portfolio Passport](#10-portfolio-passport)** — B5 (AIF). Janet + Hester + Gabrielle. Triple-champion AIF. Replaces network/pedigree with signed real-world proof of work.
5. **[Hawker Inventory Agent](#14-hawker-inventory-agent)** — E3. Nishith + James + SEA VCs + Desmond. Nishith-bait: real multilingual voice → demand-model → auto-ordering pipeline. Strongest non-AIF lane.

---

## All 14 ideas

### 1. Filial Proxy

**Tackles:** A4 (ageing, independent living) + D4 (caregiver burnout) + E2 (governance / auditability)
**For:** Mdm Lim, 78, Toa Payoh 4-room, widow — *and* her daughter in London who can't manage her CareShield claims, polyclinic appointments, and MediSave top-ups across timezones.

**The insight.** Every existing eldercare product targets the elderly person. The real caregiver is the adult child overseas, drowning in parent-admin they can't physically do from abroad. The SEA specificity is filial piety as an obligation + Singapore's diasporic reality (adult children in Shanghai / London / NY). Not a fall-detector — a *proxy* that does the admin.

**AI pipeline:**
1. **Ingest** — voice calls from Mdm Lim (Mandarin/Hokkien), SMS from CareShield, emails from polyclinic
2. **Classify** — admin task / medical update / urgent / social chit-chat
3. **Plan** — what action? (file claim / book appointment / top up MediSave / call pharmacy / escalate)
4. **Execute** — tool-use against CareShield portal, HealthHub, polyclinic booking API, pharmacy phone tree
5. **Receipt log** — every action written to an auditable ledger the adult child can scrub
6. **Escalation** — ambiguity or high-stakes action pings adult child for approval
7. **Weekly digest** — summary to daughter in London: what happened, what's next, what needs her

**Panel champions:** Bing Wen (CPF/ageing + CareShield), Wanting (public-health pragmatism), Sandy (agent permissions + audit). Three strong, plus James for scale.

**Risk:** Real CareShield/HealthHub APIs aren't integratable in a week — demo must mock them. Mitigation: make *one* integration real (e.g., actual polyclinic appointment via HealthHub test env, or a real phone call to a pharmacy IVR using a voice model); mock the rest but show the architecture credibly.

---

### 2. Numbers Honestly

**Tackles:** D6 (fertility vs career, AIF) + D5 (health literacy) + B5 (opportunity access, AIF)
**For:** Charmaine, 33, senior associate at a SG law firm, partner track in 3 years, IVF ideally this year — nobody has modelled the trade-off honestly.

**The insight.** Existing apps are fertility *trackers* (Flo, Clue). Existing advice is motivational platitudes. What Charmaine needs is a *scenario simulator*: "If you start IVF at 34 vs 37, here's the fertility success-rate delta from peer-reviewed data, here's the partner-track outcome distribution, here's your CPF trajectory either way — with honest uncertainty bounds."

**AI pipeline:**
1. **Intake** — guided form: age, career track, firm, relationship status, health markers, financial state
2. **Retrieve (RAG)** — peer-reviewed fertility age-curve literature + SG firm-leave policies + career-pause meta-analyses + CPF/CareShield/childcare-subsidy rules
3. **Simulate** — Monte Carlo over 3–5 named pathways (start IVF now / defer 2yr / defer 4yr / forego)
4. **Score** — per-pathway: fertility success-rate distribution, career outcome distribution, financial outcome (incl. CPF projection)
5. **Narrate** — LLM composes pathway descriptions *with uncertainty ranges visible*; no single-number claims
6. **Compare** — side-by-side, honest about confidence intervals
7. **Save / share** — export to partner, revisit quarterly as inputs change

**Panel champions:** Janet (AIF sponsor), Hester, Wanting. **Triple-champion + AIF tailwind** — structurally highest-scoring on this panel.

**Risk:** (a) Wanting will torch hallucinated rates — RAG sources must be real, citations visible. (b) Emotional tone matters. Mitigation: ship with 3 real peer-reviewed sources per claim; never a single number, always a range.

---

### 3. Fair Share Agent

**Tackles:** C4 (invisible cognitive labor, AIF) + C3 (fragmented communication)
**For:** Siti, 20, NTU class rep. Carries the coordination load for 4 male teammates who ride free.

**The insight.** Every "invisible labor" product measures the gap and makes Siti the nag with new data. That's the done-to-death trap. The novel move: the agent *absorbs the coordination labor itself* — drafts the nudges, chases non-responders, builds status updates, handles the RSVP Tetris — so Siti stops being the chaser. Measurement is optional and private.

**AI pipeline:**
1. **Ingest** — team chat history via Telegram / WhatsApp / Slack MCP connectors
2. **Extract** — coordination acts: reminders, follow-ups, chasers, emotional-management moves
3. **Attribute** — graph: who does the coordination work today
4. **Absorb** — agent takes over the reminders / follow-ups / status summaries
5. **Redistribute** — drafts nudges to non-responders in that person's tone, not Siti's
6. **Report** — weekly private dashboard for Siti; optional team-shared dashboard
7. **Hand-back** — Siti can un-assign any coordination task, agent holds the line

**Panel champions:** Janet (AIF sponsor), Hester, Gabrielle. Triple-champion AIF.

**Risk:** Public load-tracking shames teammates. Mitigation: dashboard private by default; absorption is the product, measurement is side-feature.

---

### 4. Remix Club for Teen Girls

**Tackles:** A5 (AI adoption gap, AIF) + E5 (prompt user → architect, AIF)
**For:** Aisyah, 15, IP school Sec 3. Uses ChatGPT for homework but never builds. Mother thinks AI is "not for girls."

**The insight.** Coding bootcamps with female branding fail because they frame AI as STEM. Aisyah doesn't need to learn to code — she needs to build agents for things she *already* cares about (K-pop scheduling, fandom digests, friend-group logistics, event coordination). The product is a Discord/Telegram-native visual agent scaffolder where teens remix each other's agents. Fork culture, not curriculum.

**AI pipeline:**
1. **Intake** — teen types/voices what she wants in natural language
2. **Scaffold** — LLM emits a starter agent (prompt + tool graph) in readable visual format
3. **Remix** — she edits nodes + tool calls via drag UI; agent schema visible
4. **Sandbox** — run agent in isolated env, see intermediate reasoning
5. **Fork** — share agent to friend; friend edits and forks back
6. **Compare** — "your agent vs mine — why did mine do better?"
7. **Graduate** — as she gets comfortable, expose raw schema / MCP tool definitions

**Panel champions:** Janet (AIF sponsor), Hester, Gabrielle. Triple-champion AIF. Sandy secondary (AI education policy).

**Risk:** Minors + generative AI + DMs = safeguarding risk. Mitigation: moderated sandbox; no open DMs; fork is the social primitive, not chat.

---

### 5. Next-Visit Briefing

**Tackles:** D1 (preventive health accessible) + D3 (Asian-context fit) + D4 (caregiver version)
**For:** Uncle Tan, 47, hawker at Old Airport Road. 14h days, BMI 29, pre-diabetic. Polyclinic told him to "eat less rice." He doesn't know where to start.

**The insight.** Uncle Tan has *already been to the polyclinic*. He got generic advice because the doctor had 2 minutes and no context. What's missing is the bridge between visits — daily micro-adjustments that respect his real constraints, and a *briefing for his next visit* that turns those 2 minutes from "eat less rice" into a data-rich conversation.

**AI pipeline:**
1. **Ingest** — polyclinic discharge note (OCR + structured extract), patient voice diary (Mandarin/Hokkien/English), optional meal photos
2. **Classify** — food against an Asian-context nutrient/GI DB (not MyFitnessPal's Western baseline)
3. **Recommend** — tomorrow's micro-adjustment ("half-portion rice at breakfast, kangkong on the side")
4. **Log** — longitudinal patient record, 7-day adherence
5. **Compose** — next-visit briefing PDF/QR: "patient reports X, ate Y most days, adherence ~70%, symptoms Z"
6. **Hand-off** — patient shows QR to GP at next visit; GP sees real data
7. **Loop** — after visit, ingest updated note, repeat

**Panel champions:** Wanting (NHG pipeline — this is exactly her rubric), Bing Wen (if tied to MediSave / CHAS), James (SEA scale).

**Risk:** Wanting will destroy any whiff of "AI doctor." Frame strictly as patient translator + clinician decision support — never diagnosis. Human-in-the-loop, visible uncertainty, disclaimers.

---

### 6. Brain Gigs

**Tackles:** B2 (low-friction earning) + B1 (skills → income) + A3 (unequal AI personalisation)
**For:** Fariz, 19, NITEC grad doing food delivery while studying. Wants S$500/mo using his brain.

**The insight.** Gig platforms assume Fariz has a resume-able "skill." He doesn't. But he has *tacit* knowledge — delivery geography, Malay-English translation, food-culture fluency of specific neighborhoods. The novel move: an AI agent extracts tacit knowledge and productizes it into micro-services that pay today — no resume, no interview.

**AI pipeline:**
1. **Interview** — 5-min voice conversation: what do you know that others don't?
2. **Extract** — tacit knowledge → listable services ("Tampines local-food tour, voice chat, S$15" / "Malay menu translation, S$20/menu")
3. **Price** — benchmark against Carousell / local marketplaces
4. **List** — auto-publish to Carousell / FB Marketplace with optimized copy
5. **Mediate** — handle inbound inquiries in his tone, book confirmed orders
6. **Execute** — coach him through delivery (first 3 times)
7. **Pay + portfolio** — PayNow receipt, growing proof-of-work for higher-value gigs

**Panel champions:** Gabrielle (student / early career), Bing Wen (WIS / low-income equity), Desmond (SG ecosystem viability).

**Risk:** Trust/fraud on first transaction. Mitigation: capped first-gig value (S$10 trial), AI-mediated dispute resolution, PayNow escrow.

---

### 7. Predict-Then-See

**Tackles:** E4 (preserving human agency) + D5 (health literacy)
**For:** Ethan, 16, Sec 4. Uses Claude for every homework question. No longer sure if he understands calculus or if Claude does.

**The insight.** "AI off" toggles don't work because they fight the user. The novel move: *friction that rewards self-knowledge*. Before Claude answers, the user predicts the answer and rates their confidence. Then they see where they were right, where they were wrong, and what concept the gap lived on.

**AI pipeline:**
1. **Intercept** — user submits query to Claude
2. **Elicit** — "before I answer: what do you think, and how confident?"
3. **Answer** — Claude answers
4. **Diff** — compare user prediction vs answer; localize the gap
5. **Tag** — concept cluster (e.g. "chain rule," "integration by parts")
6. **Aggregate** — weekly blindspot report, confidence calibration curve
7. **Coach** — targeted practice on weakest concept

**Panel champions:** Sandy (agency-preserving AI is her policy sweet spot), Gabrielle (student product).

**Risk:** Friction = abandonment. Mitigation: make friction rewarding (streak, calibration score, blindspot heatmap); ship as default-off, opt-in "training mode."

---

### 8. Receipts

**Tackles:** A1 (ambient AI agents and trust) + E2 (governance / auditability by default)
**For:** Daniel, 34, freelance designer in Tiong Bahru. Lets his AI agent handle Grab bookings, Carousell DMs, and bill payments. Lost S$400 to a phishing reply last month.

**The insight.** Permissions dashboards are an engineer's mental model of trust. Consumers don't want rules — they want *receipts*: a credit-card-statement-style timeline of every action their agents took, with one-tap undo on each. The novel primitive is a signed, user-facing activity feed; the trust UX is retrospective accountability, not prospective policy.

**AI pipeline:**
1. **Intercept** — agent action attempted (tool call / API request / outbound message)
2. **Sign** — C2PA-style signature: "this action was taken by agent X on behalf of Daniel at time T"
3. **Classify** — what kind of action, what blast radius ($ / data / social)
4. **Log** — user-facing timeline UI (Apple Wallet-esque)
5. **One-tap rollback** — for reversible actions (message sent, booking made); flag irreversibles upfront
6. **Pattern detection** — alert on suspicious sequences (new domain, amount spike, unknown recipient)
7. **Weekly digest** — summary + share selected receipts as provenance proof (e.g., "my agent did reply that; here's the signed log")

**Panel champions:** Sandy (policy + agent trust), Nishith (signed-infrastructure depth), James (consumer-scale).

**Risk:** "Credit-card statement for agents" sounds like logging, not product. Mitigation: demo must show the rollback + fraud-catch moment, not just the feed. Pick one killer detection scenario (e.g. agent replies to phishing) and show the one-tap save.

---

### 9. Authenticity Letter

**Tackles:** A2 (fragile authenticity in a synthetic world)
**For:** Priya, 29, HR manager at an SME in Tanjong Pagar. Screens 40 CVs a week; two recent hires had AI-fabricated portfolios.

**The insight.** AI content detectors are a losing game. The novel move is *positive authenticity* — a short live structured interview with an AI that produces a signed, time-stamped, replayable authenticity artefact. Instead of "is this resume AI-written?" the HR system asks "has this candidate produced a 5-minute signed live session?" Flips the burden from suspicion to proof.

**AI pipeline:**
1. **Schedule** — candidate books a 5-min session
2. **Live structured interview** — AI asks standardized questions; records voice + video
3. **Analyse** — real-time coherence (latency, contradictions, impersonation flags)
4. **Voice biometrics** — match future sessions to this baseline
5. **Sign (C2PA)** — transcript + recording signed with candidate ID + timestamp
6. **Publish** — HR-facing verification widget attached to application
7. **Re-verify** — if doubts later, compare new voice/video against the stored baseline

**Panel champions:** Sandy (provenance is her policy sweet spot), Nishith (signed-infra depth).

**Risk:** Feels like surveillance. Mitigation: candidate-initiated (they own the artefact and re-use across applications); frame as "portable proof-of-self," not "HR verification tool."

---

### 10. Portfolio Passport

**Tackles:** B5 (opportunity access socially gated, AIF) + B1 (skills → income) + B3 (learning ↔ real work)
**For:** Hui Ling, 22, SUSS student, rental flat in Bedok. Her portfolio is stronger than the ACS-SMU pipeline her professors mentor — but the intros go to them.

**The insight.** "Blind hiring" tools that hide names still rank by pedigree through the backdoor. The novel move is making *real-world proof of work* first-class and verifiable. Every project Hui Ling ships gets signed by the actual user/client (classmate, professor, customer). Instead of "I did a scraping project for class" it's "I built this Carousell price tracker, used by 47 classmates for 3 weeks — signed by them." Employers retrieve by capability signal, not school brand.

**AI pipeline:**
1. **Intake** — project (repo link / deployed URL / doc / screenshot)
2. **Extract** — LLM extracts "what did this do, for whom, with what outcome"
3. **Identify signers** — who actually used this? surface them
4. **Auto-outreach** — one-tap "can you sign this to confirm you used it?" to each
5. **Aggregate** — per-user Portfolio Passport (signed claims + evidence)
6. **Match** — employers/opportunities query by capability signal; ranked by signed proof
7. **Weight** — referrals weighted by strength of signed evidence, not school brand

**Panel champions:** Janet (AIF sponsor), Hester (Epic Angels), Gabrielle (SMU student entrepreneurship). Triple-champion AIF. Also Desmond secondary (SG hiring).

**Risk:** Cold-start — nobody signs anything on day 1. Mitigation: seed with classmate-signed school projects where the cohort has lived network; demo with one complete example from a real user interview.

---

### 11. Quiet Clients

**Tackles:** B3 (learning ↔ real work) + B4 (entry-level compressed by AI)
**For:** Jia En, 21, NUS CS Year 3, CAP 4.8, zero deployed code — *and* Aunty Mui the hawker who has a real AI-amenable problem (her inventory mess) but can't articulate it.

**The insight.** Project-based learning platforms (Riipen, Parker Dewey) fail because they rely on enterprises posting polished briefs. SEA SMEs — hawkers, coffeeshops, trades, small retailers — have *more* real AI-amenable problems than enterprises, but they can't scope them. The novel move: an AI agent interviews the SME, extracts the real problem, scopes it into a 2-week student-doable project, supervises the handoff.

**AI pipeline:**
1. **SME intake** — voice/WhatsApp conversation in Mandarin/Malay/English
2. **Problem extraction** — LLM identifies the candidate project
3. **Feasibility scope** — break into 2-week deliverable with student-reachable tech
4. **Match** — find students with required skill signature (from Portfolio Passport if stacked)
5. **Kickoff** — spec doc + weekly milestones generated automatically
6. **Supervision** — agent attends async check-ins; flags blockers
7. **Measure impact** — SME reports outcome; signed into student's portfolio

**Panel champions:** Desmond (SG SME ecosystem), Gabrielle (student entrepreneurship), Bing Wen (if framed as Workfare SME).

**Risk:** SME-side trust — will Aunty Mui let a 21yo touch her POS? Mitigation: start with non-critical problems (inventory log analysis, not payment integration); SME can always revoke.

---

### 12. Protocol Grader

**Tackles:** D2 (unsafe experimentation in health optimisation)
**For:** Bryan, 26, software engineer. Takes 8 supplements a day based on podcasts. Stacking creatine, NAD+, ashwagandha, and a testosterone booster with zero supervision.

**The insight.** Supplement-interaction scanners are pseudo-science theatre. "DocGPT" wellness chatbots get torched by Wanting. The novel move is a *rigor layer* for any health experiment Bryan's considering: grade evidence per claim (A/B/C/D), flag dangerous interactions with real literature, and — critically — design a *safe N-of-1 experiment* with explicit rollback criteria. Scientific method as a product.

**AI pipeline:**
1. **Intake** — protocol (free text / screenshot of a podcast recommendation / link)
2. **Parse** — extract discrete claims ("NAD+ 500mg boosts NAD levels" / "ashwagandha reduces cortisol")
3. **RAG** — each claim against peer-reviewed literature
4. **Grade** — evidence level per claim (A: multiple RCTs / B: observational / C: preclinical / D: none)
5. **Interactions** — cross-reference known interactions; flag dangerous combinations with citations
6. **Experiment design** — propose N-of-1 protocol with measurable endpoints, duration, rollback triggers
7. **Follow-up** — weekly check-in; if endpoint moves adversely, trigger stop

**Panel champions:** Wanting (clinical rigor + pipeline), Sandy (safety-at-scale if framed as safety infra).

**Risk:** Liability. Mitigation: never prescribes; shows evidence and lets user decide. Hard disclaimers. Frame as "scientific method assistant," not medical advice.

---

### 13. Agent Stethoscope

**Tackles:** E1 (AI-native infra for agents) + E2 (governance / auditability)
**For:** Ishaan, 28, indie builder. Has 4 agents held together with Slack + webhooks + a Google Sheet. When they fight or loop, he has no idea why.

**The insight.** Another agent framework is noise. The real gap: multi-agent systems have no *debugger*. When Agent A asked Agent B for X and B responded with Y which A misinterpreted as Z, there is no timeline that shows this. The novel move: a sidecar that instruments live multi-agent systems and gives a cross-agent reasoning trace — with LLM-narrated "here's why they miscommunicated."

**AI pipeline:**
1. **Instrument** — sidecar hooks into MCP / webhook / queue bus (no code changes needed)
2. **Capture** — every cross-agent event stored with reasoning trace
3. **Reconstruct** — unified timeline across agents; visualize message flow
4. **Narrate** — LLM explains reasoning mismatches in plain English
5. **Rewind** — replay any agent turn with modified input
6. **Minimum repro** — export the smallest trace that reproduces a bug
7. **Share** — signed trace link for team debugging

**Panel champions:** Nishith (production agent debugging is *exactly* his lens), Sandy (observability = governance), James (scale if agent systems proliferate).

**Risk:** Devtool pitch to a mostly-VC panel will land flat unless a killer product-on-top is shown. Mitigation: lead the pitch with a consumer-agent disaster demo (an agent spending $200 twice), then reveal "this is how I caught it."

---

### 14. Hawker Inventory Agent

**Tackles:** E3 (AI applied to physical systems) + A3 (AI personalisation for underserved)
**For:** Aunty Mui, 58, hawker stall owner. Orders ingredients by WhatsApp 3×/week, always over- or under-orders, throws away ~15% of daily prep.

**The insight.** Smart-home demos, IoT dashboards, and digital-twin decks are the default E3 traps — all require hardware Aunty Mui won't install. The novel move: *zero hardware*. Runs on her existing phone and existing WhatsApp supplier. She voices her day's usage in Mandarin/Hokkien/Malay; the agent builds a per-stall demand model, drafts supplier WhatsApp messages, flags waste patterns, and answers "is fishball noodles actually profitable?"

**AI pipeline:**
1. **Voice ingest** — daily 30-second voice note in her language
2. **Multilingual STT + domain vocab** — food-specific entity extraction (bee hoon, kway teow, chilli crab paste)
3. **Demand model** — per-item, per-day-of-week, weather-adjusted forecast
4. **Order drafting** — auto-draft WhatsApp to supplier; she reviews + sends
5. **Waste attribution** — flag high-waste items, suggest portion adjustments
6. **Margin analysis** — per-dish profitability with current prices
7. **Weekly stall report** — voice summary in her language of what she made, what she wasted, what to change

**Panel champions:** Nishith (real multi-step pipeline, domain-specific STT, physical-world integration), James (SEA scale — millions of hawkers / warungs / kedai kopi across SEA), Cheryl/Daryl/Malavika (SEA VC market fit), Desmond (SG SME).

**Risk:** Hawkers are famously tool-skeptical. Mitigation: zero-onboarding product — she WhatsApps a number, agent does the rest; no app install. Demo: a real hawker using it for 3 days, measured waste reduction.

---

## Stacking map

Ideas that share primitives and could merge if you want one big swing:

- **Filial Proxy + Next-Visit Briefing** — both mediate between SG healthcare and humans who can't navigate it alone. Elderly parent + overseas child + polyclinic. Strongest Bing Wen + Wanting stack.
- **Fair Share Agent + Remix Club** — both are "agent absorbs invisible coordination work." Class rep + fandom group chat. Pure AIF / Janet stack.
- **Numbers Honestly + Predict-Then-See** — decision support with honest uncertainty and user-in-the-loop calibration. Fertility/career + health/learning. Sandy + Wanting + Janet.
- **Portfolio Passport + Quiet Clients + Brain Gigs** — the full B-theme stack. Tacit knowledge extraction → student-SME projects → signed portfolio. Could be one coherent platform for "SEA opportunity discovery." Gabrielle + Desmond + Bing Wen + Janet (if Portfolio Passport is the anchor AIF challenge).
- **Receipts + Authenticity Letter + Agent Stethoscope** — Sandy's full provenance / trust stack. Could be one "agent accountability OS" with consumer, HR, and infra surfaces.
- **Hawker Inventory Agent + Next-Visit Briefing** — both are "voice-native multilingual SEA agent with real domain vocab, real pipeline, zero hardware." Different user but same primitive. Could be the Nishith-bait mega-pitch.

---

## Coverage check

Challenges covered: A1 (Receipts), A2 (Authenticity Letter), A3 (Brain Gigs, Hawker Agent), A4 (Filial Proxy), A5 (Remix Club), B1 (Brain Gigs), B2 (Brain Gigs), B3 (Quiet Clients, Portfolio Passport), B4 (Quiet Clients), B5 (Portfolio Passport), C3 (Fair Share), C4 (Fair Share), D1 (Next-Visit Briefing), D2 (Protocol Grader), D3 (Next-Visit Briefing), D4 (Filial Proxy, Next-Visit Briefing), D5 (Predict-Then-See), D6 (Numbers Honestly), E1 (Agent Stethoscope), E2 (Filial Proxy, Receipts, Agent Stethoscope), E3 (Hawker Inventory Agent), E4 (Predict-Then-See), E5 (Remix Club).

**Intentionally skipped:** C1 (Priority collapse) and C2 (Decision fatigue) — `challenge-statements.md` flags these as weakest-advocate zones (no dedicated champion + crowded market). Enter only with a very sharp edge, not as default hackathon play.

---

## What I deliberately avoided

Everything on the per-challenge "done to death" lists: fall-detection wearables, AI-content detectors, fertility trackers, unified inboxes, habit-score dashboards, agent-framework SDKs, pink-branded anything.

Pick any card above, paste it into a separate terminal, and ask for: deck outline, tech stack choices, week-by-week build plan, interview script for Evidence-of-Demand, or a de-risking plan.
