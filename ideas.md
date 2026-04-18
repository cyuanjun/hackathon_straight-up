# Ideas

Generated from `challenge-statements.md` — each idea is grounded in the archetypes, routes around the "done-to-death" defaults, and maps to real panel champions. Each card is self-contained so you can pull any one into a separate terminal for a deep-dive.

---

## TL;DR — top picks

### If the goal is hackathon score (top 5 for the panel)

Each has ≥3 panel champions, a clear 5–7 step AI pipeline, SEA-specific grounding, isn't on the done-to-death list, and is demoable in a week. Since 67% of rubric score is Challenge-Solution Fit + Tech Execution, these are the structurally safest bets.

1. **[Filial Proxy](#1-filial-proxy)** — A4 + D4 + E2. Bing Wen + Wanting + Sandy. Uniquely SEA (overseas diaspora + filial piety). CareShield/MediSave admin agent for overseas adult children.
2. **[Numbers Honestly](#2-numbers-honestly)** — D6 (AIF). Janet + Hester + Wanting. Triple-champion AIF tailwind. RAG-grounded fertility + career simulator with *honest uncertainty*.
3. **[Fair Share Agent](#3-fair-share-agent)** — C4 (AIF) + C3. Janet + Hester + Gabrielle. Absorbs coordination labor, doesn't just measure it.
4. **[Portfolio Passport](#10-portfolio-passport)** — B5 (AIF). Janet + Hester + Gabrielle. Triple-champion AIF. Replaces network/pedigree with signed real-world proof of work.
5. **[Hawker Inventory Agent](#14-hawker-inventory-agent)** — E3. Nishith + James + SEA VCs + Desmond. Nishith-bait: real multilingual voice → demand-model → auto-ordering pipeline. Strongest non-AIF lane.

### If the goal is starting a company (top 3 for the VC bloc)

6 of 15 judges are VCs (Cheryl, Daryl, Malavika, Theresa, Joshua, Heng Xuan) plus Hester (angel) and James (corporate). What they reward: **SEA-first GTM, defensibility, business-model clarity, founder-market fit, durable moats, regional TAM**. What they punish: US-coastal copycats, hackathon-only defensibility, unclear monetization.

1. **[Envelope](#16-envelope--agent-native-payment-rail)** — A1 + E1 + E2. Nishith (Stripe!) + Sandy + James. "Stripe for agents." Payment rails designed for agents, not retrofitted from human rails. Infrastructure moat + two-sided network effect.
2. **[Kasih Credit](#15-kasih-credit--sea-alt-credit-agent)** — A3 + B2 (+ AIF if framed for women). James + Janet + SEA VCs + Heng Xuan. Alt-credit for SEA's 300M thin/no-file adults. Classic SEA fintech — massive TAM, regulatory moat, data flywheel.
3. **[MigrantMate](#18-migrantmate--ofw-remittance--household-agent)** — A3 + C3 + D4. Malavika + James + Hester. Household agent for OFWs managing family finances from 2,000km away. $150B+ remittance flow, family-network effect, category-creating.

### The bridge ideas (score well in both lenses)

If you want hackathon-win-plus-investor-conversation in one swing, these are the overlap: **[Hawker Inventory Agent](#14-hawker-inventory-agent)**, **[Portfolio Passport](#10-portfolio-passport)**, **[Agent Stethoscope](#13-agent-stethoscope)**, **[Filial Proxy](#1-filial-proxy)**.

---

## All 19 ideas

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

## VC-friendly ideas (startup-ready)

These 5 ideas are tuned for the VC bloc's lens: SEA-first GTM, defensibility, clear business model, founder-market fit, regional TAM, durable moats. They're scored slightly differently from the panel-optimised ideas above — they lead with the market wedge and include explicit BM / Moat / TAM / Founder-fit fields. Panel-champion alignment is still shown, but some of these will score mid on AIF-tailwind and high on commercial judges instead.

### 15. Kasih Credit — SEA Alt-Credit Agent

**Tackles:** A3 (unequal AI personalisation) + B2 (low-friction earning) — stacks to A5/B5 (AIF) if framed explicitly for women
**For:** Delivery drivers, hawker assistants, market stall owners, domestic helpers across SG/ID/PH/VN who are credit-invisible (thin- or no-file). ~60–70% of SEA adults fit this profile.

**The insight.** 300M+ SEA adults are thin-file or no-file. Traditional underwriting excludes them; BNPL lenders prey on them. The novel move: an AI agent that builds a verifiable alternative credit profile from gig-platform earnings (Grab/Gojek), e-wallet flows (PayNow/GCash/OVO), utility/rent payments, and behavioral signals — packaged as an *explainable* credit report banks can underwrite against.

**AI pipeline:**
1. User consent → pulls from gig platforms, e-wallets, telco top-ups, utility payments
2. Feature extraction: income regularity, essential-spend ratio, stability signals
3. Alternative credit model (LLM-augmented feature engineering + classical risk model)
4. Explainable score card: user sees exactly which behaviors help/hurt
5. Dispute + correction flow (agent handles via the relevant platform)
6. Bank-facing API: underwriters pull signed, timestamped credit report
7. Ongoing monitoring: flag lifestyle changes, auto-re-score

**Panel champions:** **James** (Intl sustainability + financial inclusion at scale — his exact lens), **Janet** (AIF if framed for women — SEA women are disproportionately thin-file), Cheryl/Daryl/Malavika (SEA VC — TAM + regulatory wedge), Heng Xuan (durable moat via data accumulation).

**Business model:** B2B2C — banks/lenders pay per underwriting pull (~$2–5/pull); consumer keeps the profile free.
**Moat:** Data flywheel (more borrowers → more signals → better scores → more banks) + regulatory compliance as barrier to entry + bank-partnership exclusivity.
**TAM:** ~300M thin/no-file SEA adults; $30B+ underserved SME+consumer credit gap (Bain/Temasek 2024).
**Founder-market fit:** Strongest if team has lived financial-exclusion experience *or* SEA banking insider knowledge. Articulate why a US competitor can't clone this: local regulator relationships, local platform integrations, language coverage, trust.

**Risk:** Bank-partnership integration isn't demo-able in a week. Mitigation: partner with one SG bank sandbox (DBS PayLah dev sandbox, UOB TMRW API), make the ingest + scoring + explanation flow real; mock the pull-to-bank step credibly.

---

### 16. Envelope — Agent-Native Payment Rail

**Tackles:** A1 (ambient AI agent trust) + E1 (AI-native infra) + E2 (governance / auditability by default)
**For:** Developers building consumer agents + the consumers whose agents will move money (starting with Daniel, 34, Tiong Bahru designer — see archetype #8).

**The insight.** Current payment rails (Stripe, cards, PayNow) assume a human authorizes each transaction. Agents need a fundamentally different primitive: *budget envelopes* with per-category limits, per-merchant whitelists, auto-revocable scopes, anomaly freezes, and signed agent-identity receipts. Nobody has built payment infra *for* the agent era — incumbents (Stripe included) are retrofitting human rails.

**AI pipeline:**
1. User creates budget envelope: $X for category Y, merchant whitelist, time-box
2. Agent requests spend → envelope checks policy + merchant verification
3. Risk model flags anomalies (new merchant, amount spike, behavioral deviation)
4. Signed transaction: receipt with agent ID, user ID, envelope ID, C2PA-style signature
5. User-facing receipt feed (natural stack with [Receipts](#8-receipts))
6. One-tap revocation / rollback for reversible merchants
7. Dispute + regulator-facing audit trail

**Panel champions:** **Nishith** (Stripe — this is literally his domain; multi-step non-trivial infra), **Sandy** (agent permissions + governance), James (global scale), Heng Xuan (infrastructure moat), Theresa (Antler solo-founder angle).

**Business model:** Usage-based (bps on agent transactions, ~30–50 bps) + enterprise SaaS tier for platforms.
**Moat:** Two-sided network effect (more agents accept → more merchants integrate) + compliance/regulator relationships + first-mover on the category.
**TAM:** Category-creating. Every consumer agent that moves money globally. SEA agent-native spend projected to hit tens of $B in late-2020s.
**Founder-market fit:** Strongest with payments-infra experience OR deep agent-systems experience. Big claim to own: "every agent will need this; today none have it."

**Risk:** "Stripe for agents" is high-ambition — demo must show one real live transaction end-to-end, not a dashboard. Mitigation: pick one killer scenario (agent buys ingredients for Aunty Mui's stall via Envelope; user sees receipt + one-tap cancel live on stage).

---

### 17. LiveTrust — Indonesian Social Commerce Trust Agent

**Tackles:** A2 (fragile authenticity) + A3 (unequal AI outcomes in consumer protection)
**For:** Indonesian and SEA social-commerce buyers on TikTok Live / Instagram Live / Shopee Live who get scammed daily by fake sellers and counterfeit products on livestreams.

**The insight.** Indonesian social commerce is $80B+ today and growing ~40% YoY. Buyers have zero trust infrastructure — they buy based on livestream energy and lose money to fake sellers. Incumbents (TikTok Shop, Shopee Live) won't fix this because their TVL depends on volume, not trust. The novel move: an AI agent that watches livestreams in real-time, verifies sellers across sessions (face consistency, voice biometrics, product provenance), surfaces an in-session trust score, and offers escrow until delivery.

**AI pipeline:**
1. Viewer opts in to a livestream (browser extension or companion app)
2. Agent ingests video + audio in real-time
3. Seller verification: face consistency across previous streams, voice biometric match, account-history cross-reference
4. Product provenance: if claimed "100% original," check against brand register
5. Trust score surfaced in-session (non-intrusive overlay)
6. Escrow offer: buyer pays into escrow, released on delivery confirmation
7. Post-transaction reputation update (signed review tied to verified purchase)

**Panel champions:** **Malavika** (East Ventures, Indonesia — her exact lens), James (SEA scale + financial inclusion/protection), Cheryl/Daryl (SEA VC), Sandy (authenticity/provenance primitive).

**Business model:** Take-rate on escrow-protected transactions (1–2%) + platform partnerships (Shopee/Lazada affiliate integrations).
**Moat:** Reputation graph — grows more valuable the bigger it gets; incumbents won't replicate without cannibalizing their own TVL.
**TAM:** SEA social commerce projected $200B+ by 2030; Indonesia alone is $80B today.
**Founder-market fit:** Must include Indonesian founder or deep ID social-commerce experience. US-founded competitor is structurally disadvantaged (language, platform relationships, seller-side networks).

**Risk:** Integrating with TikTok/IG without blessing is hard. Mitigation: start with Shopee Live (more open APIs) or ship as a browser extension / companion app that buyers install independently of the platform.

---

### 18. MigrantMate — OFW Remittance + Household Agent

**Tackles:** A3 (AI personalisation equity) + C3 (fragmented communication) + D4 (caregiver burnout — OFWs are long-distance caregivers)
**For:** Maria, 38, Filipino domestic worker in Singapore. Sends ~S$1,200/month home; also manages her kids' school fees, parents' medicine, cousin's utility bills — from her phone, across timezones, through WhatsApp threads she can't track.

**The insight.** Remittance apps (GCash, Maya, Wise) treat every transfer as atomic. OFWs actually operate a *distributed household* — recurring obligations, bill payments, dispute mediation, and emotional labor from 2,000km away. The novel move: an agent that authenticates once to the family's e-wallets, pays recurring bills on their behalf, detects anomalies, and gives Maria a weekly household financial report in Tagalog.

**AI pipeline:**
1. Multi-user auth: Maria + her mother + her kids consent to shared financial oversight
2. Ingest: family's e-wallet flows, bill SMS, utility portals, school-fee notifications
3. Schedule recurring payments (auto-execute on approved schedule)
4. Anomaly detection: unusual withdrawal, missed bill, new merchant
5. Bilingual voice interface (English/Tagalog/Bahasa/Thai/Khmer)
6. Dispute mediator: if sister "borrowed" money, agent surfaces the fact and helps Maria confront without escalating family drama
7. Weekly household financial report → Maria's WhatsApp, in her language

**Panel champions:** **Malavika** (East Ventures, SEA), **James** (financial inclusion at scale — his exact lens), **Hester** (majority of OFWs are women), Cheryl/Daryl (SEA VC), Janet (if framed as AIF — women's economic empowerment).

**Business model:** Freemium (1 recipient free, family-pack paid ~$4–8/mo) + bps on managed recurring payments.
**Moat:** Family-network effect (adding one OFW onboards 4–6 household members) + data flywheel on household financial patterns + trust-once-earned-is-sticky.
**TAM:** 10M+ Filipino OFWs, 30M+ SEA migrant workers globally, $150B+ annual SEA remittance flow.
**Founder-market fit:** Strongest if team has OFW family background or deep SEA migration experience. Category-creating in a massive underserved segment that American fintechs systematically ignore.

**Risk:** Trust + security is existential (people's livelihoods). Mitigation: v1 is read-only (ingest + insights + alerts, no payments); v2 adds bill payment after trust is established and reputation is seeded.

---

### 19. ComplyAI — SG Early-Stage Compliance Agent

**Tackles:** E2 (governance / auditability) inverted — *using* agents to absorb regulatory compliance work + B4 (entry-level work compressed — compliance is exactly the work AI can absorb)
**For:** Hana, 29, solo founder building a fintech out of Antler. Spent 40 hours last month on ACRA / IRAS / CPF / MOM filings instead of product.

**The insight.** SG is famously structured — which means its compliance is *automatable*. Every founder does this dance manually because it's fragmented across 5+ government portals with no unified calendar or state. Incumbents (corp-sec firms) charge $300–800/mo to do it by hand. The novel move: an agent that owns the regulatory calendar end-to-end, fetches documents, prepares filings, submits them, and maintains an audit trail for due diligence.

**AI pipeline:**
1. Company intake (UEN, structure, headcount, share cap)
2. Regulatory calendar generation: ACRA AGM, IRAS ECI/Form C-S, CPF submissions, MOM work-pass renewals, GST
3. Document fetch: pull financials from Xero/QuickBooks; employee data from HR system
4. Preparation: agent drafts each filing; founder reviews
5. Submission via each portal's API (where available) or browser automation where not
6. Confirmation tracking + receipt storage
7. Audit trail: signed record of every filing action for future due diligence

**Panel champions:** **Theresa** (Antler — every solo founder needs this yesterday, and she's investing in solo founders), **Desmond** (ACE.SG — ecosystem viability), **Joshua Lim** (business-model clarity), Heng Xuan (scaling logic to MY/ID/VN), Nishith (multi-step pipeline with real integrations).

**Business model:** B2B SaaS, ~S$80/mo/company (replacing S$300–800 corp-sec fees).
**Moat:** Regulatory-integration depth (every new portal integration is a moat layer); reliability becomes a trust moat; once you're doing someone's filings, they don't switch.
**TAM:** ~60K active SG private companies + ~10K new companies/year. Expand to MY / ID / VN for 5–10x multiplier.
**Founder-market fit:** Strong with SG startup-operator or corp-sec background. Solo-founder-viable (exactly Theresa's Antler lens).

**Risk:** "Boring SaaS" demo risks being a slide deck. Mitigation: live-file one real ACRA AGM during the pitch. Nothing beats a real submission on stage.

---

## Stacking map

Ideas that share primitives and could merge if you want one big swing:

- **Filial Proxy + Next-Visit Briefing** — both mediate between SG healthcare and humans who can't navigate it alone. Elderly parent + overseas child + polyclinic. Strongest Bing Wen + Wanting stack.
- **Fair Share Agent + Remix Club** — both are "agent absorbs invisible coordination work." Class rep + fandom group chat. Pure AIF / Janet stack.
- **Numbers Honestly + Predict-Then-See** — decision support with honest uncertainty and user-in-the-loop calibration. Fertility/career + health/learning. Sandy + Wanting + Janet.
- **Portfolio Passport + Quiet Clients + Brain Gigs** — the full B-theme stack. Tacit knowledge extraction → student-SME projects → signed portfolio. Could be one coherent platform for "SEA opportunity discovery." Gabrielle + Desmond + Bing Wen + Janet (if Portfolio Passport is the anchor AIF challenge).
- **Receipts + Authenticity Letter + Agent Stethoscope** — Sandy's full provenance / trust stack. Could be one "agent accountability OS" with consumer, HR, and infra surfaces.
- **Hawker Inventory Agent + Next-Visit Briefing** — both are "voice-native multilingual SEA agent with real domain vocab, real pipeline, zero hardware." Different user but same primitive. Could be the Nishith-bait mega-pitch.
- **Envelope + Receipts** — Envelope is the rail, Receipts is the UI. Together: the full consumer-facing agent-payments trust stack. Nishith + Sandy double-champion; strongest infrastructure pitch on the panel.
- **Kasih Credit + MigrantMate** — both serve SEA's financially underserved. Kasih profiles you; MigrantMate *uses* your profile to manage your household. Together: "AI financial OS for the next 500M SEA consumers." James + Malavika + AIF possible.
- **Envelope + Kasih Credit + MigrantMate** — the full SEA financial-inclusion trio. Category-creating, triple-VC-friendly. Could pitch as one holding-co play but likely too ambitious for hackathon week — pick one as wedge.
- **ComplyAI + Agent Stethoscope** — both are "boring SaaS with durable moats that founders need." Theresa + Desmond + Joshua pure commercial stack; zero AIF but strong VC panel vote.

---

## Coverage check

Challenges covered: A1 (Receipts, Envelope), A2 (Authenticity Letter, LiveTrust), A3 (Brain Gigs, Hawker Agent, Kasih Credit, LiveTrust, MigrantMate), A4 (Filial Proxy), A5 (Remix Club), B1 (Brain Gigs), B2 (Brain Gigs, Kasih Credit), B3 (Quiet Clients, Portfolio Passport), B4 (Quiet Clients, ComplyAI), B5 (Portfolio Passport), C3 (Fair Share, MigrantMate), C4 (Fair Share), D1 (Next-Visit Briefing), D2 (Protocol Grader), D3 (Next-Visit Briefing), D4 (Filial Proxy, Next-Visit Briefing, MigrantMate), D5 (Predict-Then-See), D6 (Numbers Honestly), E1 (Agent Stethoscope, Envelope), E2 (Filial Proxy, Receipts, Agent Stethoscope, Envelope, ComplyAI), E3 (Hawker Inventory Agent), E4 (Predict-Then-See), E5 (Remix Club).

**Intentionally skipped:** C1 (Priority collapse) and C2 (Decision fatigue) — `challenge-statements.md` flags these as weakest-advocate zones (no dedicated champion + crowded market). Enter only with a very sharp edge, not as default hackathon play.

---

## What I deliberately avoided

Everything on the per-challenge "done to death" lists: fall-detection wearables, AI-content detectors, fertility trackers, unified inboxes, habit-score dashboards, agent-framework SDKs, pink-branded anything.

Pick any card above, paste it into a separate terminal, and ask for: deck outline, tech stack choices, week-by-week build plan, interview script for Evidence-of-Demand, or a de-risking plan.
