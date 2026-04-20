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

### If the goal is starting a company (top 5 for the VC bloc)

6 of 15 judges are VCs (Cheryl, Daryl, Malavika, Theresa, Joshua, Heng Xuan) plus Hester (angel) and James (corporate). What they reward: **SEA-first GTM, defensibility, business-model clarity, founder-market fit, durable moats, regional TAM**. What they punish: US-coastal copycats, hackathon-only defensibility, unclear monetization.

1. **[Carbon Invoice](#26-carbon-invoice--sme-scope-3-emissions-agent)** — E3 + A3. James (his literal job: Head of Sustainability at Ant) + SEA VCs + Heng Xuan. SME Scope-3 emissions reporting → unlocks green finance. Massive regulatory tailwind (CSRD, SG CID); James is pre-sold.
2. **[AgenticAg](#30-agenticag--smallholder-farmer-ai-agent)** — E3 + A3. James + Malavika + SEA VCs. Voice-native AI agent for 200M+ SEA smallholder farmers. The biggest underserved agent-TAM on earth; 30–70% middleman margin to capture.
3. **[Envelope](#16-envelope--agent-native-payment-rail)** — A1 + E1 + E2. Nishith (Stripe!) + Sandy + James. "Stripe for agents." Infrastructure moat + two-sided network effect. Category-creating.
4. **[Kasih Credit](#15-kasih-credit--sea-alt-credit-agent)** — A3 + B2 (+ AIF if framed for women). James + Janet + SEA VCs + Heng Xuan. Alt-credit for SEA's 300M thin/no-file adults. Classic SEA fintech — massive TAM, regulatory moat, data flywheel.
5. **[MigrantMate](#18-migrantmate--ofw-remittance--household-agent)** — A3 + C3 + D4. Malavika + James + Hester. Household agent for OFWs managing family finances from 2,000km away. $150B+ remittance flow, family-network effect.

Strong backups: [Claims](#27-claims--sea-micro-insurance-agent) (insurance inclusion), [Working Capital](#28-working-capital--invoice-factoring-agent-for-sea-smes) (SME cashflow), [SME Counsel](#29-sme-counsel--ai-lawyer-for-sea-smes) (legal for the underserved), [LiveTrust](#17-livetrust--indonesian-social-commerce-trust-agent) (social commerce trust), [ComplyAI](#19-complyai--sg-early-stage-compliance-agent) (SG compliance SaaS).

### If the goal is "everyone would use this" (universal consumer hits)

These solve problems every single person in the room has — judges, audience, teammates. They lean on universality over niche specificity, and almost all can be demoed with a problem the user is *personally* dealing with that week.

1. **[Rehearse](#23-rehearse)** — C4 (AIF) + E4. Janet + Hester + Sandy + Gabrielle. Roleplay partner for hard conversations (raises, breakups, boundaries, feedback). Universal anxiety, no existing product.
2. **[Aftermath](#25-aftermath)** — A4 + D4 + C4. Janet/Hester + Bing Wen + Wanting. Logistics agent for life ruptures (grief, divorce, new baby, job loss). Everyone goes through 3–5 of these.
3. **[PaperMate](#20-papermate--consumer-bureaucracy-agent)** — A3 + E2. James + Janet + Sandy + Nishith. Full consumer-bureaucracy agent: taxes, rebates, insurance claims, form-filling, subscription cancellation. Boring but valuable; concrete demo.

### The bridge ideas (score well in panel *and* VC lenses)

If you want hackathon-win-plus-investor-conversation in one swing, these are the overlap: **[Hawker Inventory Agent](#14-hawker-inventory-agent)**, **[Portfolio Passport](#10-portfolio-passport)**, **[Agent Stethoscope](#13-agent-stethoscope)**, **[Filial Proxy](#1-filial-proxy)**.

---

## Pain points solved + value delivered

Quick-reference for "what problem am I solving" and "what value do I bring" per idea. **Pain** = what's broken today. **Value** = what changes when this exists. This is pitch-slide framing — the problem/solution slide writes itself from the two lines below.

### Panel-optimised ideas (1–14)

**1. Filial Proxy**
- *Pain:* Adult children abroad can't manage elderly parents' SG healthcare admin across timezones; parents forget things but won't say; admin falls through the cracks.
- *Value:* Overseas filial duty becomes structurally possible — parent stays independent with dignity, child stays informed without invasion, admin actually gets done.

**2. Numbers Honestly**
- *Pain:* Young professional women face fertility-career trade-offs with only platitudes or fear narratives for guidance; no honest probabilistic model of the actual pathways.
- *Value:* A data-grounded decision surface showing real outcome distributions per pathway — decide from evidence, not from pressure.

**3. Fair Share Agent**
- *Pain:* One person (usually the woman) carries invisible coordination labor for the whole group; resentment builds; others don't see the work.
- *Value:* Coordination labor gets *absorbed* by the agent (not just measured) — she stops being the chaser while the work still happens.

**4. Remix Club for Teen Girls**
- *Pain:* Teen girls use AI consumptively (homework) but never build with it; male peers ship Discord bots at 14; adoption gap compounds into capability gap.
- *Value:* Low-bar entry into AI *building* via fandom/social contexts they already care about — confidence comes from remixing friends, not bootcamp pedagogy.

**5. Next-Visit Briefing**
- *Pain:* 2-minute polyclinic visits → generic advice → no between-visit adherence support → patient drifts; clinician has no real data at the next visit.
- *Value:* Between-visit support in patient's language + a structured briefing that makes the next 2 minutes data-rich instead of generic.

**6. Brain Gigs**
- *Pain:* Young people with tacit knowledge (delivery routes, multilingual, local expertise) can't monetize it because gig platforms require resumes; brains idle while they bike.
- *Value:* Tacit knowledge becomes sellable micro-service + proof-of-work + pathway to higher-value gigs — no resume needed.

**7. Predict-Then-See**
- *Pain:* Students use Claude for every question and lose track of what they actually know; can't tell if they understand or if Claude does.
- *Value:* Each query becomes a self-assessment + gap diagnosis — learning accelerates because blindspots become visible.

**8. Receipts**
- *Pain:* Agents act invisibly; users find out what happened only when something goes wrong; no rollback; phishing goes unnoticed.
- *Value:* Signed receipt feed + one-tap rollback per action — consumers can trust agents because they can *see* and *undo* what they did.

**9. Authenticity Letter**
- *Pain:* HR can't tell which candidates are AI-fabricated; interviews are gameable; hires arrive unable to do what they "proved."
- *Value:* Candidates produce portable signed live artefacts — positive proof-of-human replaces losing detection games.

**10. Portfolio Passport**
- *Pain:* Opportunity access is gated by school brand and networks, not by what you've built; capable people outside the ACS-SMU pipeline never get surfaced.
- *Value:* Signed real-world proof-of-work replaces pedigree — employers retrieve by capability signal, not lineage.

**11. Quiet Clients**
- *Pain:* SEA SMEs have real AI problems but can't articulate them; students want real work but can't access enterprise; both sides sit idle.
- *Value:* AI scopes the SME's problem + matches a student + supervises the handoff — both sides get paid work neither could get alone.

**12. Protocol Grader**
- *Pain:* Biohackers stack supplements from podcasts; no safety oversight; dangerous interactions unflagged; health decisions rest on marketing.
- *Value:* Evidence-graded + interaction-flagged + N-of-1 experiment designed — rigor delivered as a product, not a lecture.

**13. Agent Stethoscope**
- *Pain:* Multi-agent systems fail silently (loops, missed messages, misreads); no debugger exists; devs debug by prayer.
- *Value:* Cross-agent reasoning trace + narrated mismatches + rewind/replay — agent debugging becomes possible at all.

**14. Hawker Inventory Agent**
- *Pain:* Hawkers over- or under-order ingredients, waste 15% of prep, don't know per-dish profitability — no tool fits their actual workflow (WhatsApp, voice, Mandarin/Hokkien/Malay).
- *Value:* Voice-native demand forecasting + auto-ordering + margin analysis in their language — waste drops, profit rises, no hardware.

### VC-friendly ideas (15–19)

**15. Kasih Credit**
- *Pain:* 300M+ SEA adults are thin/no-file; banks can't underwrite them; BNPL preys on them; financial exclusion compounds into poverty traps.
- *Value:* Alt-credit profile from gig earnings, e-wallet flow, utility patterns — bankable where previously invisible to the formal system.

**16. Envelope**
- *Pain:* Payment rails assume human-per-transaction authorization; agents misuse credentials; limits are crude; no budget-envelope concept; mistakes cost real money.
- *Value:* Purpose-built agent payment infrastructure — per-merchant scopes, signed identities, anomaly freezes, one-tap rollback.

**17. LiveTrust**
- *Pain:* SEA social commerce ($80B+) runs on livestream vibes; buyers lose money to fake sellers; no trust infrastructure; platforms won't fix it (volume > trust for them).
- *Value:* Real-time trust score + in-session escrow — buyers protected, good sellers differentiated, fraud becomes unprofitable.

**18. MigrantMate**
- *Pain:* OFWs manage distributed households from 2,000km away through crappy WhatsApp threads + transactional remittance apps; emotional + admin overload daily.
- *Value:* Household agent handles recurring bills, flags anomalies, reports weekly in their language — peace of mind replaces anxiety.

**19. ComplyAI**
- *Pain:* SG solo founders spend 40+ hours/month on ACRA/IRAS/CPF/MOM filings; corp-secs charge $300–800/mo for the same manual work.
- *Value:* Compliance owns itself — agent drives the calendar, files autonomously, audits — founder-time reclaimed for product.

### Universal consumer ideas (20–25)

**20. PaperMate**
- *Pain:* Everyone has a drawer of "paperwork I should do"; cost of figuring out each task > prize; money and rights left on the table.
- *Value:* Paperwork inbox handled end-to-end — unclaimed money comes back, admin stops consuming your time.

**21. Refund Hunter**
- *Pain:* $900+/adult/year in unclaimed refunds (flight delays, warranty, utility, rebates); rules too complex per-claim to be worth bothering.
- *Value:* Every refund you're owed gets filed automatically, success-fee only — money back in your pocket with zero effort.

**22. Fine Print**
- *Pain:* Informed buyers negotiate, uninformed buyers sign; adversarial clauses in leases/loans/insurance/employment cost years of money and rights.
- *Value:* Contract read + benchmarked + flagged + counter-proposal drafted + negotiation rehearsed — the informed-buyer advantage becomes everyone's.

**23. Rehearse**
- *Pain:* Hard conversations (raises, breakups, feedback, boundaries) get avoided; avoidance compounds; nobody has a willing practice partner at 2am.
- *Value:* AI roleplay partner playing the *other person* — you walk into the real conversation ready, phrasing rehearsed, fallbacks lined up.

**24. Real Research**
- *Pain:* Google is worse every year; ChatGPT hallucinates; Perplexity compresses without evaluating; high-stakes decisions rest on bad summaries.
- *Value:* Real research workflow — 20+ sources graded, conflicts surfaced, synthesized, remembered — you see the work, not just the answer.

**25. Aftermath**
- *Pain:* Life ruptures (grief, divorce, new baby, job loss, diagnosis) dump 50 admin tasks on you exactly when capacity is lowest; grief gets buried under paperwork.
- *Value:* Agent owns the rupture's logistics graph — handles what it can, drafts what you need to approve, paces the load — you deal with the life, not the paperwork of the life.

### More VC-focused ideas (26–30)

**26. Carbon Invoice**
- *Pain:* Corporate buyers are pushing Scope-3 reporting downstream; 50M+ SEA SMEs can't calculate or report their emissions; consultants charge $10k+; SMEs risk losing supply-chain contracts.
- *Value:* Auto-generated CDP-compliant emissions reports from ops data + access to preferential green financing — SMEs stay in supply chains and pay less for capital.

**27. Claims**
- *Pain:* 100M+ SEA gig workers pay into micro-insurance but claim rates are under 5%; the process is opaque, the money vanishes into insurer coffers.
- *Value:* Agent detects claimable events, files, and appeals denials automatically — the money paid in actually comes back out when it should.

**28. Working Capital**
- *Pain:* SEA SMEs wait 60–90 days for corporate payments while paying suppliers upfront; invoice factoring is manual, expensive, gatekept; cashflow failure is the #1 SME mortality cause.
- *Value:* AI-built credit case + financier matching + 48-hour disbursement at half the typical factoring fee — SMEs don't die from cashflow.

**29. SME Counsel**
- *Pain:* SEA SMEs can't afford $300–800/hr lawyers; they sign bad contracts or skip legal entirely; US-template downloads don't match local jurisdictions; disputes cost 10x later.
- *Value:* AI lawyer drafts SEA-jurisdiction-specific documents, reviews incoming contracts, negotiates, produces audit trail — first-class legal access where there was none.

**30. AgenticAg**
- *Pain:* 200M+ SEA smallholder farmers make daily crop, pricing, financing decisions with zero information; middlemen capture 30–70% of margin; generations of exploitation compound.
- *Value:* Voice-native AI agent (local languages, WhatsApp, offline-capable) gives agronomy + pricing + direct-buyer access + input credit — farmers keep the margin that was always theirs.

---

## Panel-optimised ideas (1–14)

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

## Universal ideas (everyone has this problem)

These 6 ideas solve universal adult pains — the kind of thing every judge, every teammate, every audience member will recognise from their own week. They're less niche-optimised than the panel-score picks but have the upside of a demo that lands in the gut: the judges *want* this to exist. All still AI-load-bearing and non-trivial.

### 20. PaperMate — Consumer Bureaucracy Agent

**Tackles:** A3 (equity — lower-income households leave more on the table) + E2 (agent audit/trust) + A1 (agent trust)
**For:** Anyone who has ever put off a tax filing, insurance claim, rebate, form renewal, or subscription cancellation. Which is everyone.

**The insight.** We all have a mental drawer of "paperwork I should do." Tax filing, health insurance claims, parking appeals, warranty claims, utility disputes, rebate applications, school forms. Everyone leaves money and rights on the table because the cost of figuring out each one exceeds the prize *on any one item*. The novel move: an agent that owns the entire paperwork inbox end-to-end, so you never have to think about any single filing.

**AI pipeline:**
1. Ingest — email + physical mail (photo) + SMS for anything "action required"
2. Classify — deadline, category, estimated value (refund amount / cost of missing)
3. Triage — urgent / worth it / auto-decline junk
4. Gather — required documents, account info, prior forms
5. Draft — fill the form / write the letter / compose the appeal
6. Submit — via API, email, portal, or print-and-mail service
7. Track + follow up — chase replies, escalate past deadlines

**Panel champions:** James (equity framing — lower-income households hit hardest), Janet (AIF if framed as women carrying household paperwork), Sandy (agent audit), Nishith (multi-step real pipeline).

**Business model:** Freemium + success fee on recovered refunds.
**Moat:** Institutional integrations (every new gov portal = moat); longitudinal household data.
**TAM:** Every adult.

**Risk:** "AI fills out forms" sounds incremental. Mitigation: lead with one specific concrete win ("agent found $1,200 in GST Voucher rebates you didn't know you qualified for, filed them, money lands Friday").

---

### 21. Refund Hunter

**Tackles:** A3 (unequal outcomes — unclaimed money is a regressive tax on attention)
**For:** Anyone who's ever had a flight delayed, a product break within warranty, a utility overcharge, an expired rebate, or a government top-up they forgot to claim. Est. $900+/adult/year in unclaimed refunds in developed markets.

**The insight.** Refund-hunting is a literal free lunch — the money is yours, you just have to file. Nobody does it because the effort of knowing eligibility > expected value *per claim*. The novel move: an agent that continuously monitors your life for refund-triggering events and files automatically. Not a coupon extension — a full-claim agent that knows rules across airlines, utilities, warranties, gov rebates, insurance.

**AI pipeline:**
1. Ingest — email confirmations, credit-card statements, calendar, receipts
2. Event detection — flight delay (via airline data), warranty breakage, utility spike, product recall, gov rebate eligibility
3. Rule match — cross-ref claim rules per provider
4. Evidence gather — auto-pull required docs
5. File — submit via each provider's channel
6. Follow up — chase denials, escalate
7. Payout — deposit to user + keep a success-fee cut

**Panel champions:** James (financial inclusion), Desmond (SG ecosystem), Cheryl/Daryl (SEA VC — clean BM), Janet (if framed as women managing household claims).

**Business model:** Success fee (15–25% of recovered funds); no upfront cost.
**Moat:** Claim-rules library (per provider, grows over time) + payout-outcome data.
**TAM:** Every consumer. $900+/adult/year unclaimed globally.

**Risk:** Sounds scam-adjacent. Mitigation: never charge upfront; show clear audit of every filing attempt; start with one demonstrable win (actual flight-delay EU261 claim demo'd live).

---

### 22. Fine Print

**Tackles:** A3 (sophisticated buyers get better contracts than naive ones) + E4 (preserving agency — you still sign, but informed)
**For:** Anyone signing a lease, loan, insurance, SaaS contract, employment offer, or T&C. Which is everyone, several times a year.

**The insight.** The informed buyer reads + negotiates + gets better terms. The uninformed buyer signs blind and eats the losses. "AI contract summarizer" tools exist but they're ChatGPT with a PDF — one-shot, generic, no benchmarks. The novel move: an agent that reads on your behalf, *benchmarks* the contract against typical-market standards + your specific situation, flags adversarial clauses, drafts the counter-proposal email, and rehearses the negotiation conversation with you.

**AI pipeline:**
1. Ingest — contract PDF, email, or screenshot
2. Parse — clauses → structured contract graph
3. Benchmark — retrieve comparable contracts from corpus (SG tenancy norms, SaaS T&Cs, employment contracts)
4. Flag — deviations, adversarial clauses, ambiguities
5. Personalize — "your situation is X, so clause Y matters more than usual"
6. Draft counter-proposal — specific redlines + email ready to send
7. Rehearse — mock the negotiation conversation (chains into [Rehearse](#23-rehearse))

**Panel champions:** Janet/Hester (women often get worse terms on housing/employment — AIF angle), Sandy (agency), Nishith (real corpus + retrieval pipeline), Desmond (SG rental-market specific).

**Business model:** Per-contract ($10–20) or freemium + pro tier for high-stakes contracts.
**Moat:** Contract corpus + outcome data (which counter-proposals actually get accepted).
**TAM:** Every adult signing a contract; bigger B2B tier for SMEs.

**Risk:** Users don't pay upfront for "what if." Mitigation: free tier reads + summarises; paid tier for redlines + negotiation script. Demo one real rental contract with visible $ savings over the term.

---

### 23. Rehearse

**Tackles:** C4 (invisible cognitive labor — hard conversations disproportionately fall to women, AIF) + E4 (preserving agency — it's still your conversation) + C2 (decision fatigue)
**For:** Anyone putting off a hard conversation. Asking for a raise. Breaking up. Setting a boundary with a parent. Giving tough feedback. Asking a friend for money back. Firing someone. Telling your partner you want / don't want kids.

**The insight.** The anxiety of a hard conversation is (a) not knowing what to say, (b) not knowing how they'll respond, (c) never having practiced the flow. Every therapist/coach says "rehearse it" but nobody has a willing partner at 2am when the anxiety is worst. The novel move: an AI roleplay partner that plays the *other person* (tuned with what you know about them), lets you try multiple openings, shows likely responses, and gives you a script you actually feel ready to use.

**AI pipeline:**
1. Intake — what's the conversation? who's the other person? what do you want? what do you fear?
2. Model them — LLM builds "the other person" agent from what you know (personality, history, triggers)
3. Role-play — you speak, agent responds as them; iterate multiple takes
4. Branch — "what if I open with X vs Y?" replay different paths
5. Identify sticking points — where does it always break down?
6. Coach — tone, pacing, phrasing, bridge lines when they push back
7. Final script — bullet points you can actually use, plus fallback lines for common blow-ups

**Panel champions:** **Janet + Hester** (AIF — women disproportionately carry emotional labor + avoid hard conversations), Sandy (agency-preserving AI — the agent plays the other person, you still speak), Gabrielle (student product: feedback to classmates, profs, team). **Triple-champion AIF** plus Sandy.

**Business model:** Consumer subscription ($5–15/mo); pro tier for career-critical conversations (raise negotiations, job offers).
**Moat:** Conversation data (learns your voice + the people in your life); emotional trust is sticky.
**TAM:** Every adult. Very large, underserved.

**Risk:** Sounds AI-therapy-adjacent → Wanting will flag. Mitigation: strictly frame as rehearsal tool, NOT therapy. Agent plays the other person, never gives life advice. Hard disclaimer on deep distress (route to human resources).

---

### 24. Real Research

**Tackles:** A3 (good research is a privilege) + A2 (authenticity — grounded in sources, not hallucinated) + E4 (agency — see the sources, don't just accept the summary)
**For:** Anyone researching a major decision. Which doctor to see. Which school for your kid. Which car to buy. Which insurance to pick. Which country to move to. Which supplement claim is real. Google gets worse every year; ChatGPT hallucinates; everyone flies blind.

**The insight.** "AI-powered search" (Perplexity, Google SGE) compressed the internet into summaries but *lost the work of actually researching* — evaluating sources, weighing conflicting evidence, flagging sponsored content. The novel move: an agent that works like a good research assistant — reads 20+ sources, grades each for credibility, synthesizes with explicit conflict notes, and shows you the underlying sources ranked by quality. Persistent memory across queries.

**AI pipeline:**
1. Query — user asks a real question
2. Broad search — 20+ sources across types (peer-reviewed, news, forums, gov, blog)
3. Grade — credibility + recency + bias score per source
4. Extract claims — what does each source actually say?
5. Conflict resolution — where sources disagree, *surface* it (don't paper over)
6. Synthesize — structured answer with confidence ranges + sourcing shown
7. Remember — user can save + annotate; future queries build on prior research

**Panel champions:** Sandy (authenticity + governance of AI outputs — her sweet spot), Gabrielle (students + research workflow), Wanting (health-research sub-vertical).

**Business model:** Freemium — 3 free/mo, $10/mo unlimited.
**Moat:** Source-grading model (proprietary) + user's personal research graph + reputation system on queries.
**TAM:** Every knowledge worker, student, patient, parent.

**Risk:** Perplexity is an incumbent. Mitigation: wedge is *research workflow* — conflict-surfacing, credibility-grading, persistent memory — not better search. Demo with a real high-stakes query ("is GLP-1 safe given my family history?") showing the difference from Perplexity's output.

---

### 25. Aftermath

**Tackles:** A4 (independent living, family-applicable) + D4 (caregiver burnout — the "caregiver" here is whoever navigates the rupture) + C4 (invisible coordination labor, AIF possible)
**For:** Anyone navigating the logistics of a life rupture. Grief. Divorce. New baby. Job loss. Diagnosis. Relocation. Separation. An aging parent's decline. Every adult goes through 3–5 of these.

**The insight.** When life ruptures, you suddenly have 50 new admin tasks at the exact moment you have the least capacity. Notify people, cancel services, transfer accounts, handle estate admin, inform schools, change addresses, set up autopay for the other person's bills, figure out what to do with the joint Netflix. The novel move: an agent that owns the full logistics checklist of any major life event, handles what it can autonomously, drafts what needs your approval, and protects you from admin so you can deal with the actual life change.

**AI pipeline:**
1. Event onboarding — "what happened? (bereavement / divorce / new baby / ...)"
2. Generate logistics graph — 40–80 tasks by category, prioritized by urgency
3. Delegate — agent handles what it can autonomously (notify subscription services, cancel utilities)
4. Draft — letters, messages, forms for tasks needing your approval
5. Coordinate — loops in family members / professionals (lawyer, accountant) for their parts
6. Track — status across weeks/months
7. Emotional pacing — some tasks can wait; agent holds the list at *your* pace, doesn't overwhelm

**Panel champions:** **Janet/Hester** (aftermath disproportionately falls on women — AIF-able), Bing Wen (end-of-life CPF nominations + widow admin is his exact lens), Wanting (caregiver support framing), Malavika (universal across SEA).

**Business model:** One-time fee per event ($50–200) or always-ready subscription ($8/mo).
**Moat:** Event playbooks (the library of known workflows per life event) + emotional trust (once someone goes through a rupture with you, they stay).
**TAM:** Every adult; 3–5 events per adult life.

**Risk:** Emotional sensitivity. Mitigation: strictly logistics agent, never emotional companion; always offer human-professional handoff for sensitive decisions (lawyer for divorce, grief counsellor for bereavement); user controls pacing.

---

## More VC-focused ideas (startup-pitch optimised)

These 5 are written for the investor case first, panel-score second. Each targets a specific VC thesis (ESG + supply chain / SEA fintech inclusion / working capital / vertical B2B SaaS / smallholder TAM). They'd still score decently on the rubric, but the reason to pick one is "I want to actually raise money on this."

### 26. Carbon Invoice — SME Scope 3 Emissions Agent

**Tackles:** E3 (AI for physical systems) + A3 (underserved SEA SMEs)
**For:** Aunty Mui's stall and 50M+ other SEA SMEs suddenly being told by their corporate buyers (Grab, Shopee, Unilever, Ant supply-chain partners) to report emissions or be dropped from supply chains. They have zero capacity to calculate this.

**The insight.** Big corporates are pushing Scope-3 requirements downstream (CSRD in force from 2024; SG Climate Impact Disclosures mandatory from 2026). SEA SMEs — the suppliers — can't report and can't improve. Consultants charge $10k+ per report. The novel move: an agent that ingests ops data (invoices, utility bills, fuel receipts, deliveries) and auto-produces CDP-compliant emissions reports in the SME's language — then *unlocks preferential green financing* from lenders who need verified-green borrowers.

**AI pipeline:**
1. Ingest — invoices, utility bills, fuel receipts, delivery logs (voice / photo / WhatsApp)
2. Classify — scope 1/2/3 category per transaction
3. Estimate — emission factors (region + industry specific)
4. Report — CDP / ISSB / SG CID-compliant output
5. Benchmark — vs sector peers
6. Improve — suggest reductions (supplier swap, energy switch)
7. Finance — connect verified-green SMEs to preferential lending rates

**Panel champions:** **James** (Head of Intl Sustainability at Ant — this is his exact job description; he's pre-sold on the thesis), Cheryl/Daryl/Malavika (SEA VC + ESG mandate), Heng Xuan (durable moat), Nishith (real pipeline depth), Desmond (SG SME fit).

**Business model:** SaaS ($30–80/mo per SME) + bps on unlocked green financing.
**Moat:** Emission-factor database (regional/sector-specific — expensive to build) + financier network + regulatory relationships + data flywheel (more SMEs → better benchmarks → better recommendations).
**TAM:** 50M+ SEA SMEs × $50/mo SaaS + $100B+ SEA supply-chain finance market = the entire ESG-reporting wave.
**Founder-market fit:** Strongest with sustainability or supply-chain finance background. Signals "we understand the regulatory wave AND the SEA SME ops reality."

**Risk:** Emission-factor accuracy is a credibility bar. Mitigation: partner with one accredited factor provider (Climatiq, NTU sustainability lab) and make that dependency auditable. Claim "defensible estimates," not "certified."

---

### 27. Claims — SEA Micro-Insurance Agent

**Tackles:** A3 (unequal AI outcomes) + B2 (low-friction earning as low-friction claiming) + A5/B5 (AIF if framed for women who over-represent in gig + domestic work)
**For:** Grab/Gojek drivers, Carousell sellers, delivery riders, hawker assistants, domestic helpers across SEA — all paying into micro-insurance (gig platform insurance, NTUC Income micro plans, Sompo, AXA Go) with <5% claim rates because the process is opaque.

**The insight.** SEA gig workers pay into micro-insurance but almost never claim. Not because claimable events don't happen — they happen constantly (accidents, phone damage, illness, missed shifts). The process is too confusing. The money vanishes into insurer coffers. The novel move: an agent that knows the 15–20 micro-insurance products common among SEA gig workers, monitors your life for claimable events, files for you, and appeals denials.

**AI pipeline:**
1. Policy upload — user photos policy docs or permits pull from e-wallet
2. Policy parse — structured extraction of coverage, exclusions, time-limits
3. Event monitoring — detect claimable events (accident from ride data, device breakage from repair receipt, missed-gig days from platform data)
4. Eligibility match — event vs coverage
5. Evidence auto-gather — required docs from user's existing records
6. File — submit via insurer's channel
7. Follow-up + escalate — chase, appeal denials, escalate to consumer protection

**Panel champions:** **James** (financial inclusion at scale — his exact lens), Cheryl/Daryl/Malavika (SEA fintech), **Janet + Hester** (gig/domestic work skews female in SEA — AIF angle + claim-mgmt is emotional labor), Bing Wen (WIS/CareShield adjacency).

**Business model:** Success fee on claims paid (20–30%). Consumer pays nothing unless they win.
**Moat:** Policy-parsing library + insurer integration map + behavioral payout data (what actually gets paid out vs denied).
**TAM:** 100M+ SEA gig workers × ~$200–400/yr in unclaimed micro-insurance = $20–40B+ unclaimed pool.
**Founder-market fit:** Strongest with insurance-industry or gig-worker operator experience. Defensibility: regulators will increasingly push insurers to cooperate as claim-rate gaps become politicised.

**Risk:** Insurers will resist actively (they profit from the claim gap). Mitigation: start with insurer-friendly products (gig platform-mandated insurance where platforms want higher claim rates); consumer-protection regulatory framing as moat.

---

### 28. Working Capital — Invoice Factoring Agent for SEA SMEs

**Tackles:** A3 (unequal AI outcomes for SMEs) + E3 (physical systems — supply chain)
**For:** SEA SME owners waiting 60–90 days for payment from corporate buyers while paying their own suppliers upfront. Cashflow failure is the #1 SEA SME mortality cause (not product, not competition).

**The insight.** Invoice factoring exists but is manual, expensive (3–5%/mo), and gatekept by relationships. US solutions (Pipe, Capchase) don't translate because they assume predictable SaaS revenue — SEA SMEs have lumpy cashflow. The novel move: an AI agent that analyzes your invoice book + buyer quality (public + history) + supplier payment terms → builds a credit case autonomously → matches to financiers → disburses in 48 hours.

**AI pipeline:**
1. Ingest — SME invoice book (Xero / QuickBooks / photos)
2. Buyer profile — payment-history lookup (ACRA, regulatory filings, past on-time %)
3. Risk model — invoice-level default probability
4. Package — bundle eligible invoices into a financing tranche
5. Match — to financier (bank / non-bank / P2P) with appetite for this risk profile
6. Disburse — funds to SME account within 48 hours
7. Collect — auto-collect on due date; handle disputes

**Panel champions:** **James** (financial inclusion at scale + fintech — his lens), **Heng Xuan** (durable moat via data + financier network), Cheryl/Daryl/Malavika (SEA fintech), Desmond (SG SME), Joshua (BM clarity).

**Business model:** 0.5–2% on financed invoice value (half of typical factoring fees).
**Moat:** Risk model improves with every invoice (flywheel); two-sided financier network; buyer-quality data becomes proprietary.
**TAM:** $100B+ SEA SME working capital gap (IFC / Bain estimates); 50M+ SMEs addressable.
**Founder-market fit:** Strongest with fintech operator or trade-finance background. Signals "I know why Pipe doesn't work in SEA."

**Risk:** Each SEA market has different invoice-financing rules. Mitigation: start in Singapore (MAS sandbox exists), then expand market-by-market. Don't promise pan-SEA day one.

---

### 29. SME Counsel — AI Lawyer for SEA SMEs

**Tackles:** A3 (unequal AI outcomes) + E2 (governance / auditability)
**For:** SEA SME owners who need legal docs (employment, supplier terms, partnership, leases, NDAs) but can't afford $300–800/hr lawyer rates. They either sign bad contracts, skip legal entirely, or download US templates they don't understand.

**The insight.** US AI-legal players (Harvey, Ironclad) target big-firm lawyers — high ARPU, narrow market. The SEA opportunity is the opposite: tens of millions of SMEs who've *never had legal access*. The novel move: an AI lawyer that drafts SEA-jurisdiction-specific documents, reviews incoming contracts against local norms, gives first-line advice in Mandarin / Bahasa / Vietnamese, and produces a signed audit trail.

**AI pipeline:**
1. Intake — conversational interview in user's language
2. Retrieve — jurisdiction-specific legal corpus (SG / MY / ID / VN / TH statutes + case law + standard forms)
3. Draft — contract tailored to SME's specific situation
4. Review incoming — parse contracts the SME receives, flag adversarial clauses vs local norms
5. Negotiate — draft counter-proposal in the SME's voice
6. Sign + store — e-sign integration with audit trail
7. Dispute support — pull relevant clauses + applicable law when issues arise

**Panel champions:** **Theresa (Antler)** — every Antler founder needs this + solo-founder-viable, **Desmond (ACE.SG)** — SG SME fit, Cheryl/Daryl/Malavika (SEA B2B SaaS), Nishith (multi-jurisdiction legal pipeline), James (inclusion).

**Business model:** B2B SaaS ($40–120/mo) + per-doc fees for complex matters.
**Moat:** Jurisdiction-specific legal corpus (expensive to curate); case-outcome data; local legal-system integrations. Geographic moat — US competitors can't clone easily.
**TAM:** ~5M SEA SMEs currently skipping legal; $10B+ underserved legal-services gap.
**Founder-market fit:** Strongest with SEA legal or SME operator background. Defensibility: breadth across SEA jurisdictions is the moat.

**Risk:** "AI lawyer" has regulatory sensitivity (unauthorised-practice-of-law rules vary). Mitigation: frame as "legal document assistant," never "legal advice"; partner with licensed lawyers for complex matters; explicit scope limits.

---

### 30. AgenticAg — Smallholder Farmer AI Agent

**Tackles:** E3 (AI for physical systems) + A3 (underserved) + scales to A5/B5 (AIF if framed for female farmers)
**For:** 200M+ Indonesian / Vietnamese / Thai / Filipino smallholder farmers making daily crop, pricing, and financing decisions with almost no information, systematically exploited by middlemen who capture 30–70% of margin.

**The insight.** Smallholder farmers are the largest underserved agent-addressable population on earth. Decisions daily (what to plant, when to sell, what price to accept) with no data, no benchmarks, no direct-buyer access. Middlemen capture most margin because they have information farmers don't. The novel move: a voice-native (Mandarin / Bahasa / Vietnamese / Thai / Tagalog) AI agent that gives smallholders agronomy, weather, pricing, direct-buyer matching, and input credit — all via WhatsApp, no app install.

**AI pipeline:**
1. Voice ingest — farmer's daily update in their language
2. Agronomy advice — domain-specific (nutrient deficiency, pest pattern) grounded in regional crop data
3. Weather forecast — localized, crop-relevant, actionable
4. Market pricing — real-time nearby mandi / market prices
5. Direct buyer match — connect to corporate buyer (Grab, Unilever, exporters), bypass middlemen
6. Input credit — qualifying farmers get input financing backed by forward-sale contracts
7. Weekly voice report in their language — what to do next week, what the market is doing, what's in their pocket

**Panel champions:** **James** (sustainability + financial inclusion + scale — he will salivate), **Malavika (East Ventures, Indonesia)** — massive smallholder base, Cheryl/Daryl (SEA VC), Hester (women farmers skew majority in some SEA markets — AIF angle).

**Business model:** Take-rate on financed transactions + input-sale margins + marketplace fees on direct-buyer matching.
**Moat:** Ground-truth smallholder operational data (proprietary + hard to replicate) + buyer network + financier relationships + regional language coverage. Data-flywheel moat.
**TAM:** 200M+ SEA smallholders; $200B+ annual SEA ag output; 30–70% middleman capture to redirect.
**Founder-market fit:** Strongest with agritech or financial-inclusion operator experience. The story writes itself: "we fix the biggest economic injustice in SEA."

**Risk:** Smallholders are tool-skeptical + low-connectivity. Mitigation: voice-first + WhatsApp-native (infrastructure they already use); distribution via agri-cooperatives; nail one country (Indonesia likely) before expanding.

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
- **PaperMate + Refund Hunter + Fine Print** — the full adulting OS. Everyone's paperwork + their refunds + their contracts. James + Nishith + Janet if women-framed. Concrete consumer pitch.
- **Rehearse + Fair Share Agent** — emotional labor absorbed on both sides. Siti stops being the chaser AND stops dreading the "we need to talk" with her flatmate. Double-AIF Janet + Hester stack.
- **Aftermath + Filial Proxy** — when Mdm Lim passes, the Filial Proxy becomes Aftermath; same infrastructure, life-transition continuum. Bing Wen + Wanting + Janet if framed around widowhood admin.
- **Real Research + Numbers Honestly + Protocol Grader** — evidence-grounded decision support trio. Sandy + Wanting + Janet. "Honest AI" identity stack.
- **Kasih Credit + Working Capital + Claims** — the SEA financial inclusion OS. Consumer alt-credit + SME cashflow + micro-insurance claiming. James + Heng Xuan + SEA VCs. Triple moat from three data pools that reinforce each other.
- **Carbon Invoice + SME Counsel + ComplyAI** — SEA SME "regulatory OS." ESG reporting + legal docs + compliance filings. Theresa + Desmond + James + Heng Xuan. One SME, three revenue streams.
- **AgenticAg + Hawker Inventory Agent + Quiet Clients** — SEA physical-economy voice-agent stack. Smallholder + hawker + SME-to-student bridge. Same primitive (voice-first multilingual agent with domain vocab), three user segments. Nishith + James + Malavika.
- **Claims + MigrantMate + PaperMate** — household-admin absorption stack for the underserved. The OFW manages her family's insurance claims + household bills + government paperwork via one agent. James + Hester + Malavika.

---

## Coverage check

Challenges covered: A1 (Receipts, Envelope, PaperMate), A2 (Authenticity Letter, LiveTrust, Real Research), A3 (Brain Gigs, Hawker Agent, Kasih Credit, LiveTrust, MigrantMate, PaperMate, Refund Hunter, Fine Print, Real Research, Carbon Invoice, Claims, Working Capital, SME Counsel, AgenticAg), A4 (Filial Proxy, Aftermath), A5 (Remix Club, Claims, AgenticAg via female-farmer framing), B1 (Brain Gigs), B2 (Brain Gigs, Kasih Credit, Claims), B3 (Quiet Clients, Portfolio Passport), B4 (Quiet Clients, ComplyAI), B5 (Portfolio Passport, Claims, AgenticAg via women's framing), C2 (Rehearse), C3 (Fair Share, MigrantMate), C4 (Fair Share, Rehearse, Aftermath), D1 (Next-Visit Briefing), D2 (Protocol Grader), D3 (Next-Visit Briefing), D4 (Filial Proxy, Next-Visit Briefing, MigrantMate, Aftermath), D5 (Predict-Then-See), D6 (Numbers Honestly), E1 (Agent Stethoscope, Envelope), E2 (Filial Proxy, Receipts, Agent Stethoscope, Envelope, ComplyAI, PaperMate, SME Counsel), E3 (Hawker Inventory Agent, Carbon Invoice, Working Capital, AgenticAg), E4 (Predict-Then-See, Fine Print, Rehearse, Real Research), E5 (Remix Club).

**Still intentionally skipped:** C1 (Priority collapse) — `challenge-statements.md` flags this as a weakest-advocate zone (no dedicated champion + crowded market). Enter only with a very sharp edge. C2 is now touched by Rehearse via the "hard decisions you're avoiding" frame.

---

## What I deliberately avoided

Everything on the per-challenge "done to death" lists: fall-detection wearables, AI-content detectors, fertility trackers, unified inboxes, habit-score dashboards, agent-framework SDKs, pink-branded anything.

Pick any card above, paste it into a separate terminal, and ask for: deck outline, tech stack choices, week-by-week build plan, interview script for Evidence-of-Demand, or a de-risking plan.
