# Ideas — Wavesparks Challenge Exploration

*Generated 2026-04-18. Complements `combo-review.md` (which already scored the 5 obvious combos) by exploring **the challenges those combos under-served**: A2, A3, A4, D4, D6.*

---

## Scope of this doc

`combo-review.md` already analyzed and ranked five combos:

| Rank | Combo | Score |
|---|---|---|
| #1 | Women-in-AI agentic playground (A5+B5+C4+D6+E5) | 39/45 |
| #2 | Coordination OS (C1+C2+C3+C4+A1) | 36/45 |
| #3 | Career Launchpad (B1–B5) | 35/45 |
| #4 | Trust Layer for Agents (A1+E2+E4+A2) | 34/45 |
| #5 | Longevity for Young Asians (D1+D2+D3+D5) | 33/45 |

Those five cover themes B, C, E densely, and touch A1/A5/D1/D2/D3/D5. **Untouched whitespace**: A2 (authenticity), A3 (AI personalization inequality), A4 (ageing/independent living), D4 (caregiver burnout), D6 (fertility-career).

This doc proposes **6 new ideas** targeted at those gaps, each with a market scan and a defensible edge. Ranked at the end against the same 5-criterion rubric.

---

## Idea 1 — Second Shift: Elder-care co-pilot for adult children

### Challenges (A4 + D4 + C4)
- **A4** Ageing, isolation, independent living
- **D4** Hidden caregiver burnout
- **C4** Invisible cognitive labor *(the "sandwich generation" lens)*

### The unifying insight
Every existing elder-tech product targets **the senior** (ElliQ, Meela, inTouch, SeniorTalk). None seriously target **the adult child doing the coordinating** — tracking doctor appointments, medication, groceries, confusion episodes, cross-sibling logistics. That coordination burden is the exact C4 invisible-labor pattern, one generation up, and it silently lands on one adult child (usually a daughter).

### Proposed solution
A co-pilot that sits in the **adult child's** pocket:
1. Parent has a simple voice endpoint (phone call, WhatsApp number, or existing ElliQ-like device) they talk to daily.
2. The co-pilot extracts: "Mum said her knee hurt again, she skipped lunch, the aircon repair guy hasn't come." → structured log.
3. Siblings share one dashboard: who checked in, what's pending, whose turn it is for the next doctor visit.
4. Escalation layer: anomaly detection on speech pattern, missed meds, missed calls.

### Target user
**Adult children (25–45) in SEA caring for parents 65+ who still live independently.** Singapore is a perfect wedge — fastest-ageing society in SE Asia, strong filial expectations, smartphone-saturated.

### Hackathon-scoped MVP
- WhatsApp bot for the parent (no new hardware, no install).
- Claude extracts structured events + flags anomalies.
- Sibling-shared dashboard (Next.js) with a shared task board and a weekly "load per sibling" chart.
- One scripted escalation: parent mentions chest pain → dashboard red + SMS to all siblings.

### Tech depth
- Multi-step agent: transcript → entity extraction → health/logistics classifier → anomaly detector → routing.
- Real WhatsApp Business API integration (not a wrapper).
- Memory layer — the agent remembers the parent's baseline over time.

### Competitive landscape

| Product | What they do | Gap we fill |
|---|---|---|
| **ElliQ** | $1.5k robot for senior's home; 95% loneliness reduction per NYSOFA | Targets senior, not caregiver; hardware dependency |
| **Meela** | Voice AI companion for older adults | Senior-facing; no sibling coordination |
| **inTouch** | Warm AI phone calls to parents | One-way; doesn't produce a coordination ledger |
| **SeniorTalk / QuikTok** | Chatbot companionship | No family-ops surface |
| **Papa** (US) | On-demand companions for seniors | Human labor, not AI; no SEA presence |
| **CareYaya** | Caregiver marketplace + AI guide | US-only; marketplace play, not coordination |

### Our edge
- **Caregiver-first positioning** — nobody frames the product around the invisible-labor gap between siblings.
- **WhatsApp-native for the senior** — no hardware, no app install, zero onboarding friction (the competitor moat for ElliQ is bought with $1.5k hardware we avoid).
- **SEA demographic wedge** — Asian multi-sibling coordination is culturally more load-bearing than the Western "one primary caregiver" assumption.
- **Coordination-labor dashboard** (shared DNA with Coordination OS) — reuse of the same primitive shows judges a coherent point of view.

### Risks
- Liability around health escalation — frame as "communication tool," not medical.
- Privacy around recording a parent — consent UX must be tight.

---

## Idea 2 — Receipts: a consumer activity feed for personal AI agents

### Challenges (A1 + E2 + A2)
- **A1** Ambient AI agents and trust
- **E2** Governance, permissions, auditability
- **A2** Fragile authenticity — signs outbound agent actions with provenance

### The unifying insight
`combo-review.md` covered the **developer-facing** trust layer ("Clerk for agents"). The consumer version is different and under-explored: most people will soon have 3–5 agents acting on their behalf (inbox agent, shopping agent, calendar agent), with **no single feed** of what any of them did. It's the "credit-card statement for AI" — but for all your agents, not one.

### Proposed solution
A consumer app / browser extension that:
1. Installs shims into the user's major agents (ChatGPT connectors, Claude, Gemini in Gmail, any MCP-aware agent).
2. Renders a single **activity feed**: "Your inbox agent sent 4 replies, your calendar agent booked 1 meeting, your shopping agent added 2 items to cart."
3. Every action is revertible (where the underlying API supports it) and one-tap-reportable.
4. Anomaly layer: "Your shopping agent spent 3× your 30-day average — approve?"

### Target user
**Early-adopter consumers** (US + SG, 25–40, already use 2+ AI tools daily). Secondary: parents worried about teen AI usage.

### Hackathon-scoped MVP
- Proxy + dashboard around **one** agent (Claude with Gmail + Calendar MCP).
- Activity feed with human-readable "why this happened."
- Scripted anomaly demo: agent tries to send a mass email → blocked with reason.

### Tech depth
- Real MCP interception layer.
- Policy DSL with LLM-assisted anomaly classification (not just JSON rules).
- Tamper-evident ledger (hash-chained log).

### Competitive landscape

| Product | What they do | Gap we fill |
|---|---|---|
| **Guardrails AI / NeMo Guardrails** | Dev-facing policy engines | Not consumer; no activity feed |
| **LangSmith / Langfuse** | Agent tracing for devs | Dev-only; engineering UX |
| **Anthropic Claude Audit API** | Native logging | Per-provider; no cross-agent view |
| **C2PA / Content Credentials** (Pixel 10, Leica M11-P) | Signs captured content | Content-focused, not action-focused |
| **Apple Intelligence "Private Cloud Compute"** | Trust via architecture | No user-facing log |

### Our edge
- **Cross-agent aggregation** is the primitive nobody ships. Every vendor has their own log; no neutral feed across them.
- **Anomaly-first UX** — "flag 10 weird things" beats "read 300 logs."
- **Consumer framing** gets around the infra-tool demo trap (judges see a product, not a middleware config).
- Plugs into the **C2PA moment** (Pixel 10 ships content credentials by default in 2026) — extend provenance from content to actions.

### Risks
- Demand is early; consumer agents aren't yet ubiquitous.
- Real integration with closed agents (ChatGPT) is limited to what the provider exposes.
- Originality is strong (5/5 in combo-review's #4); Fit is the weak link — tighten the user definition.

---

## Idea 3 — Equal AI: a tutor that matches elite prompting for public-school students

### Challenges (A3 + D5 + B3)
- **A3** Unequal outcomes from AI personalization
- **D5** Health literacy starts too late *(extends to life-skill literacy)*
- **B3** Weak connection between learning and real work

### The unifying insight
The AI-tutor market has converged on **Khanmigo, MagicSchool, Khan Academy with GPT-4o, Alpha School**. All assume a student who can articulate what they want, has home broadband, and is coached by an engaged adult. **1 in 5 low-income families still lack reliable home broadband** (2026). The equity gap isn't *access to ChatGPT* — it's that *using it well is a prompting skill already stratified by class.* An AI tutor that works over SMS / low-bandwidth and **asks the student the right questions** (so bad prompts never become bad outcomes) closes that gap.

### Proposed solution
A tutor that:
1. Works on **SMS / low-bandwidth web** (no app, no login hell).
2. Curriculum-pinned — agrees with the student's actual Singapore / SEA syllabus, not a generic "help me with math."
3. Active-questioning agent — the student never has to prompt well; the tutor probes to find the real confusion.
4. **Caregiver view** (in Singapore, often grandparents) — weekly plain-text SMS summary of what the child worked on.

### Target user
Lower-income secondary students in SG/MY/ID on national curricula, grades 7–10.

### Hackathon-scoped MVP
- Twilio SMS endpoint.
- RAG over one subject's syllabus (e.g. Sec 2 Math, MOE).
- Socratic-prompting agent (multi-step — identify misconception, not "give answer").
- Caregiver SMS summary (weekly cron).

### Tech depth
- Real multi-step: misconception classifier → curriculum retriever → Socratic step → outcome logger.
- SMS is technically non-trivial (rate limits, thread state, short message design).
- Evaluation loop — grade the *pedagogy*, not the answer.

### Competitive landscape

| Product | What they do | Gap we fill |
|---|---|---|
| **Khanmigo** | GPT-4-based tutor in Khan Academy | US-curriculum; requires broadband + account; English-first |
| **MagicSchool.ai** | Teacher-side AI | School-system sale, not student-direct |
| **Alpha School** | AI-tutor private school, $40k/yr | Elite pricing; proves the ceiling |
| **Duolingo Max** | AI language tutor | Single-subject; subscription |
| **Cikgu.AI / Ruangguru (ID)** | SEA edtech with AI | Android app + data plan required; no curriculum-pinned Socratic mode |
| **UNICEF Learning Passport** | Offline low-bandwidth learning | Content, not live tutoring |

### Our edge
- **SMS-first wins the last-mile equity wedge** — every competitor assumes broadband.
- **Socratic-by-default** turns "prompt engineering literacy" from a prerequisite into a non-issue.
- **Curriculum-pinned** beats generic ChatGPT for trust with parents and teachers.
- **Caregiver loop** (grandparent gets an SMS) is a culturally specific SEA hook that unlocks adoption.

### Risks
- SMS unit economics are rough at scale (hackathon-fine).
- Needs a school partner for credibility; cold outreach in remote week is hard but doable.
- Tech (3/5 risk) — push to 4+ by making the misconception classifier a real thing, not "Claude reads answer."

---

## Idea 4 — Fair Share: a mental-load redistribution app for student households

### Challenges (C4 standalone + C2 + A3)
- **C4** Invisible cognitive labor
- **C2** Decision fatigue from overlapping responsibilities
- **A3** Unequal outcomes *(the poorer the household, the less mental-load slack)*

### The unifying insight
There's a crop of 2026 household-mental-load apps (**Dame, Tody FairShare, MOLO, FairChore, Ohai.ai, Maple, Persist**) — all targeting **married couples with children**. None target the **pre-household** version of the problem: student flats, hostels, young adult roommates. That population is larger, easier to reach (campus), and forms the habits that show up in later households. If this app wins in Year-3 undergrad flats, it inherits the household market in 10 years.

### Proposed solution
A roommate/housemate coordination app that:
1. Auto-generates the "invisible task list" from a 5-minute intake (who shops, takes out trash, handles landlord, manages group chat logistics).
2. **Load-per-person dashboard** with weekly balance.
3. **Trade market** — "I'll handle the WiFi issue if you cover bins this week." Claude mediates.
4. One agent-run: "nag-on-your-behalf" — the app sends the reminder so the coordinator doesn't have to.

### Target user
Uni-age roommate groups in SEA (hostels, off-campus flats). Pitch-pivot secondary: couples pre-children.

### Hackathon-scoped MVP
- WhatsApp group bot (join group → infer tasks from chat history → surface load chart).
- Consent-gated chat ingestion; structured task extraction with Claude.
- Weekly "who did what" digest.

### Tech depth
- Real chat-log parsing + role attribution (non-trivial NLP).
- Load-quantification rubric (time × cognitive weight × recurrence).
- Multi-agent: extractor → classifier → mediator → nag-drafter.

### Competitive landscape

| Product | What they do | Gap we fill |
|---|---|---|
| **Dame** | Household mental-load visibility | Couples-with-kids; paid; not chat-native |
| **Tody + FairShare 2025** | Chore fairness via points | Couples; requires app install per user |
| **MOLO** | AI assistant for the "mother load" | Parenting-framed; excludes students |
| **FairChore** | Points-based chore tracking | Same space; paid; not SEA-aware |
| **Ohai.ai** | Family ops, Sheila Marcelo-backed | Well-funded adult market; not student |
| **Maple** | Mental-load calculator quiz | Assessment only; no ongoing tool |

### Our edge
- **Student-roommate positioning** is white space — every competitor chose married-with-kids.
- **WhatsApp-native** — zero-install matters for students; competitors ship apps.
- **Consent-gated chat ingestion** is the "unfair advantage" primitive — once you have weeks of group-chat history, your task graph is better than a quiz-based competitor can ever build.
- Shares the **invisible-labor framing** with the team's existing Coordination OS direction — two products, one worldview.

### Risks
- Chat ingestion is a privacy minefield. Consent UX has to be the core of the demo, not a footnote.
- WhatsApp Business API has gotchas for bots in groups; test early.
- Overlap with C4 framing in Coordination OS means team needs to pick one.

---

## Idea 5 — Capability Card: verifiable proof-of-work, without the marketplace

### Challenges (B1 + B3 + B5 distilled)
- **B1** Slow conversion from skills to income
- **B3** Weak link between learning and real work
- **B5** Opportunity access gated by pedigree

### The unifying insight
Combo #3 (Career Launchpad) bundled all of B into one product and paid for it with **two-sided-marketplace cold-start risk**. The pivot: drop the marketplace, ship just the **primitive** — a verifiable "capability card" that works like a GitHub contribution graph but across any skill (design, writing, code, ops). Monetize the primitive, let marketplaces embed it. 2026 hiring context: "skills-based hiring" is replacing degrees, verifiable credentials (Microsoft, Velocity Network, Indicio) are launching, but all are enterprise-sold. Consumer-first capability cards are open.

### Proposed solution
A tool that:
1. Ingests any piece of work (PR, Figma file, doc, Loom, deliverable).
2. Multi-agent review grades it on a rubric *appropriate to the claimed skill*.
3. Emits a **signed, replayable card** showing the work + the reviewing agents' reasoning + time spent.
4. Portfolio is a clean public URL. Recruiters can filter by signal.

### Target user
SEA final-year students + career-switchers who want proof beyond a resume. Single-vertical demo (e.g. frontend dev).

### Hackathon-scoped MVP
- Submit a GitHub repo URL → 3-agent review (code review, UX review, architecture review) → rubric-graded card.
- Signed URL with process recording.
- Lightweight search across cards.

### Tech depth
- Multi-agent grading pipeline with explicit rubric per skill.
- Hash-chained signing (cheap, credible).
- Embeddings search over the cards.

### Competitive landscape

| Product | What they do | Gap we fill |
|---|---|---|
| **GitHub** | Code portfolio | Code-only; no reasoning trace; no rubric |
| **Mercor** | AI-interview + talent marketplace | Marketplace gatekeeper; one-shot test, not portfolio |
| **Pallet / Contra / Upwork** | Marketplaces with work history | Not portable; marketplace-locked |
| **Microsoft Credentials / Velocity Network** | Verifiable enterprise credentials | Not consumer-first; credentialing != capability |
| **RepVue / LevelsFYI** | Employer signal | Not candidate-side proof |
| **Read.cv** | Nice resume pages | Not *verified*; no grading primitive |

### Our edge
- **Primitive over marketplace** — avoids cold-start entirely; let marketplaces adopt the card.
- **Multi-agent review is an actual system** — unlike "AI scored this," three reasoning agents with disagreement is a defensible tech play.
- **Signed + replayable** — the card itself is a C2PA-style artifact; judges can literally inspect it.
- Piggybacks on the 2026 **"portfolio resume"** trend — aligned with Microsoft, Google Skill Badges, Velocity Network momentum, but consumer-first.

### Risks
- "AI graded" raises trust questions — own this by showing the disagreement trace.
- Overlaps Career Launchpad; decision is whether to ship the primitive alone or wrap it in a marketplace demo.

---

## Idea 6 — Life Compass: data-driven long-term planning for young women (without the fear)

### Challenges (D6 + D5 + A3)
- **D6** Fertility window vs career acceleration
- **D5** Health literacy starts too late
- **A3** Unequal outcomes from AI personalization *(elite fertility concierge vs nothing)*

### The unifying insight
Fertility tech in 2026 (Ovia, Clue, Premom, Flo, Babytree) is split between **cycle trackers** and **IVF concierges**. Nothing exists for a 24-year-old woman asking: "If I want 2 kids, a PhD, and a VP title, what order actually works, and what are my realistic windows?" The decision is currently made under fear-based narratives ("freeze eggs by 30!") or pure social inheritance. Empowering data + scenario simulation is whitespace, and it aligns exactly with the D6 challenge framing ("realistic, empowering data — without fear-based narratives").

### Proposed solution
A **life-scenario simulator**:
1. Onboarding captures goals (career, kids, health, geographic) + current state (age, income trajectory, heritage/genetics priors).
2. Simulator runs 5 life paths: "career-first," "family-first," "parallel," "freeze + accelerate," "pivot at 30."
3. Each path shows realistic probability bands (fertility likelihood by age from real cohort data, not single-number panic stats) + financial trajectory + career impact.
4. **No recommendation.** The tool helps her see, not decide.

### Target user
Women 22–32 in SEA who are career-ambitious and quietly anxious about timing, but turned off by IVF-marketing-style content.

### Hackathon-scoped MVP
- 10-question intake.
- Simulation engine: pre-built cohort curves (fertility by age, income growth by career-track, childcare cost tables) + Monte Carlo.
- Narrative rendering via Claude ("here's what path 3 looks like month-by-month").
- One "smallest nudge" output: "if you did X this year, path 3 becomes 2× more likely."

### Tech depth
- Real cohort data ingestion.
- Monte Carlo simulator (not an LLM doing stats badly).
- Narrative agent layered on top.
- *Not* a wrapper — the simulator is the product.

### Competitive landscape

| Product | What they do | Gap we fill |
|---|---|---|
| **Ovia / Clue / Flo / Premom** | Cycle + fertility tracking | Present-tense; no life-scenario layer |
| **Modern Fertility** | At-home hormone testing | Medical data; no planning |
| **Kindbody / Extend Fertility** | Egg-freezing concierge | Elite pricing; sales funnel |
| **Origin (Bumble's)** | Wellness + fertility coach | Content-heavy; not simulation |
| **Hello Alma / Allara** | Women's health concierge | Care navigation, not life modelling |
| **Financial planning apps (Empower, YNAB)** | Money simulation | No biology layer |

### Our edge
- **Scenario-simulator primitive** — not another tracker, not another concierge. The category of "long-horizon life simulator" is genuinely empty for this user.
- **Empowerment framing is mandated by the challenge itself** (D6 explicitly says "without fear-based narratives") — judges will reward it.
- **AIF-sponsored challenge** — the Asia Institute for Foresight judges will recognize the exact framing.
- **Asian cohort data** — Western fertility data doesn't transfer cleanly (aligns with D3). Using SEA-specific curves is a moat.

### Risks
- Medical-claim liability — must frame as "planning tool," not advice.
- Sensitive topic — UX tone is the whole product.
- Overlap with Women-in-AI combo's D6 template — if the team is also building combo #1, this collapses into it.

---

# Ranking — new ideas against the rubric

Same weights as `combo-review.md`: Fit ×3, Tech ×3, UX ×1, Originality ×1, Demand ×1. Max 45.

| Rank | Idea | Fit (×3) | Tech (×3) | UX | Orig | Demand | **Total** |
|---|---|---|---|---|---|---|---|
| **#1** | Second Shift (elder-care co-pilot) | 5 | 4 | 4 | 4 | 4 | **39** |
| **#2** | Capability Card | 4 | 4 | 4 | 4 | 4 | **36** |
| **#3** | Fair Share (student households) | 4 | 4 | 4 | 3 | 5 | **36** |
| **#4** | Life Compass | 4 | 4 | 4 | 5 | 3 | **36** |
| **#5** | Equal AI (SMS tutor) | 4 | 3 | 3 | 4 | 4 | **31** |
| **#6** | Receipts (consumer agent feed) | 3 | 5 | 3 | 5 | 2 | **31** |

### How the new ideas compare to the combo-review top 5
- **Second Shift at 39 ties combo #1 (Women-in-AI tight anchor)** and beats combo #2 (Coordination OS, 36). It's the strongest whitespace pick.
- **Capability Card / Fair Share / Life Compass at 36** match Coordination OS — viable alternates if the team is split.
- **Receipts at 31** is dominated by combo #4 Trust Layer — skip unless the team wants the consumer wedge specifically.
- **Equal AI at 31** is lower, but rubric undersells it; social-impact judges may score Fit/Demand higher than the weights suggest.

---

# Recommendations for remote week

1. **Don't pick from this doc in isolation.** Compare head-to-head with the 5 combos in `combo-review.md`. The team's current direction (Coordination OS → StraightUp in `coordination-OS/`) scores 36; Second Shift at 39 is the only new idea that clearly beats it.
2. **If the team is looking for a pivot that reuses the Coordination OS worldview**: **Second Shift** is the answer — same invisible-labor framing, different user (adult child caring for parent), softer market (ageing is accelerating in SEA, fewer incumbents than productivity tools).
3. **Validation scripts to write this week** (pick the idea first, then):
   - Second Shift: 8 interviews with 25–45 yo with a parent 65+ in SG/MY; ask about sibling coordination, not tech.
   - Fair Share: 10 student-flat interviews; request access to the group chat for 1 week.
   - Capability Card: 10 career-switchers who finished a course; ask what proof they wish they had.
   - Life Compass: 10 women 22–32; ask *what scenarios they've run in their head* — the tool builds the one they already started.
4. **Tech-depth check before day 1.** For any idea scoring Tech 4, write out the 5–7 pipeline steps explicitly. If any step is "Claude does it," redesign that step.

---

# Sources

- [The State of Content Authenticity in 2026 — Content Authenticity Initiative](https://contentauthenticity.org/blog/the-state-of-content-authenticity-in-2026)
- [C2PA Adoption in 2026 — SoftwareSeni](https://www.softwareseni.com/c2pa-adoption-in-2026-hardware-platforms-and-verification-reality/)
- [ElliQ Companion Robot](https://elliq.com/)
- [Meela AI Companion](https://www.meela.ai/)
- [inTouch Family](https://intouch.family/en)
- [CareYaya AI for Caregivers Guide 2026](https://www.careyaya.org/resources/blog/ai-for-caregivers)
- [Washington Post — Abi, AI-powered robot companion for senior care (2026-04-09)](https://www.washingtonpost.com/opinions/2026/04/09/ai-robot-senior-care-abi/)
- [AI Tutoring Equity Gap — Valere](https://www.valere.io/ai-tutoring-equity-gap/)
- [Harvard ALI — Generative AI and the Achievement Gap](https://www.sir.advancedleadership.harvard.edu/articles/harnessing-power-generative-ai-close-achievement-gap)
- [OECD Digital Education Outlook 2026 discussion — Gray DI](https://www.graydi.us/blog/gray-insights/why-your-ai-tutor-might-be-widening-the-achievement-gap)
- [Dame — Household mental-load app](https://dame-app.damedigital.ca/blog/best-household-management-apps-2026)
- [MOLO app](https://www.moloapp.io)
- [Ohai.ai — Mental load checklist](https://www.ohai.ai/blog/mental-load-checklist/)
- [Maple — Measuring the mental load](https://www.growmaple.com/blog-posts/what-is-the-mental-load-and-how-to-actually-measure-it)
- [FairChore](https://www.fairchore.com/en/blog/mental-health-2026-sharing-chores-home)
- [Microsoft Credentials — verified skills 2026](https://techcommunity.microsoft.com/blog/skills-hub-blog/verified-skills-real-impact-microsoft-credentials-help-you-get-ai-ready/4137356)
- [Velocity Network — Verifiable credentials in AI hiring](https://www.velocitynetwork.foundation/verifiable-credentials-trust-and-truth-in-an-ai-enabled-talent-acquisition-market)
- [Indicio — Why verifiable credentials will power AI 2026](https://indicio.tech/blog/why-verifiable-credentials-will-power-ai-in-2026/)
- [Converge — "Portfolio resume" trend 2026](https://www.convergeresources.com/the-portfolio-resume-why-proof-of-work-trumps-the-cv-in-2026/)
- [Top 10 fertility apps 2026](https://www.top10.com/fertility-apps)
- [iMedia — 2026 Recommended fertility apps](https://min.news/en/news/69c7b0fdac2c15d6abd8d286d2159b56.html)
- [Ovia Health](https://www.oviahealth.com/)
- [Clue](https://helloclue.com/)
- [Fertility apps & holistic health tracking — PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC7940095/)
