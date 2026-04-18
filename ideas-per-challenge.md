# Ideas Per Challenge — Decision Pack

*Generated 2026-04-19. Companion to `ideas.md`, `combo-review.md`, and the judge-panel section of `challenge-statements.md`.*

---

# Part 1 — Decision framework (read this first)

## What the rubric + panel actually reward

- **67% of score = Fit + Tech Execution** (3× each). Narrow target + real system.
- **AIF-tagged challenges (A5, B5, C4, D6, E5) carry a tailwind** — 3 dedicated champions on the panel (Janet, Hester, + 1).
- **Health ideas** face a clinical data scientist (Wanting, NHG) — no wellness fluff.
- **Tech Execution** is judged by a Stripe engineer — no LLM wrappers.
- **Classic productivity (C1–C3)** has no panel advocate + crowded market — enter only with a sharp edge.

## Top picks across all 150 ideas

### Tier 1 — strong demo, white space, panel-aligned *(pick from this list)*

| # | Idea | Challenge | Comp | Feas | Why it's here |
|---|---|---|---|---|---|
| 1 | **Second Shift** — adult-child eldercare co-pilot | A4 + D4 + C4 | 🟡 | H | Bing Wen + Wanting champions; reuses Coord OS worldview; SEA cultural fit |
| 2 | **Agentic Playground (tight anchor)** | A5 + E5 + B5 + C4 + D6 | 🟡 | M | Combo-review #1; 4 AIF champions on panel; real agent-building tech |
| 3 | **Anti-Deepfake Family Word** | A2 | 🟢 | H | Sandy champions; urgent scam context; demo-able instantly |
| 4 | **Receipts** — consumer agent activity feed | A1 + E2 | 🟡 | H | Sandy + Nishith champions; C2PA momentum 2026; white space |
| 5 | **Capability Card** | B1–B5 | 🟡 | H | Gabrielle + VCs; rides portfolio-over-resume trend; no cold-start |
| 6 | **Life Compass / The Numbers Honestly** | D6 | 🟢 | M–H | Janet + Hester + Wanting triple champion; AIF-tagged |
| 7 | **Hawker-Centre Buddy** | A4 | 🟢 | M | Bing Wen + SEA VCs; nobody building this; culturally specific |
| 8 | **Equal AI SMS Tutor** | A3 + D5 | 🟡 | M | Bing Wen + Gabrielle; social-impact wedge; real tech pipeline |
| 9 | **Fair Share for Students** | C4 | 🟡 | H | Janet + Hester; student white space ignored by all 7 household apps |
| 10 | **Socratic-Only Mode** | E4 | 🟢 | H | Sandy champions; trivial to build, powerful demo |

### Tier 2 — solid backups

| # | Idea | Challenge | Comp | Feas |
|---|---|---|---|---|
| 11 | Benefit Finder Agent | A3 | 🟡 | H |
| 12 | Phone-Native Companion (elderly) | A4 | 🟡 | H |
| 13 | Course Dropout Rescue | B3 | 🟢 | H |
| 14 | Reverse-Internship | B4 | 🟢 | H |
| 15 | Fandom Agents (teen girls) | A5 | 🟢 | H |
| 16 | Clinic-Ready Briefings | D1 | 🟢 | H |
| 17 | Teen-Safe Body Literacy Chat | D5 | 🟡 | H |
| 18 | Policy Finder for Families | D6 | 🟡 | H |
| 19 | Remix-Any-Agent | E5 | 🟢 | M |
| 20 | Hawker Inventory Agent | E3 | 🟢 | M |

### Tier 3 — interesting but hackathon-dangerous

Infrastructure plays (Agent Firewall, MCP Registry, Agent-Native Auth), data-heavy (Port Waiting, Construction CCTV), institutional-sale (Professor-as-PM, Doctor-in-the-Loop).

### Tier 4 — crowded, no panel advocate

Everything under **C1** and most of **C3** (inbox zero, unified inbox) — Superhuman, Shortwave, Motion, Notion AI, Gmail+Gemini own it. Enter only with invisible-labor framing or a non-executive price point.

## Cross-cutting primitives that repeat across challenges

1. **Ledger / receipts / dashboards of invisible work** — coordination (C4), agent actions (A1/E2), caregiving (D4), skill-building (B5). Strongest demo primitive.
2. **Scenario simulators** — life paths (D6), health trajectory (D5), career pauses. Tech-heavy, narrative-friendly.
3. **Cross-generational SEA coordination** — adult child ↔ parent (A4/D4), mom ↔ daughter (A5), teen ↔ parent (D5). Culturally specific wedge.
4. **Socratic / agency-preserving AI** — tutoring (A3), agent building (E5), health (D5), work (E4). Cheap to build, hard to market.

Ideas that hit multiple challenges (**good sign — real root cause**):
- **Second Shift** → A4, D4, C4
- **Capability Card** → B1, B2, B3, B5
- **Agentic Playground** → A5, E5, B5, C4, D6
- **Socratic tutor pattern** → A3, D5, E4

## If you had to pick today

- **Safest rubric score + differentiated from team's current work** → **Second Shift** or **Capability Card**
- **Highest ceiling + strongest panel alignment** → **Agentic Playground (tight anchor)** or **Life Compass**
- **Stay with Coordination OS worldview but move to open market** → **Fair Share for Students** (same tech, ignored user, AIF tailwind)

---

# Part 2 — How to read each idea card

```
**[CC.N] — Name** · competition · feasibility
One-line description of what it does.
- ✅ Why it's good (pro)
- ⚠️ Why it's risky (con)
```

- **Competition**: 🟢 white space · 🟡 moderate · 🔴 crowded
- **Feasibility (hackathon weekend)**: **H** high · **M** medium · **L** low
- Within each challenge, ideas are **ranked best-first** for this panel + rubric.

---

# Part 3 — The 25 challenges

*Each challenge is numbered 1–25 for navigation. The theme code (A1, B2, etc.) is preserved.*

---

## Challenge 1 · A1 — Ambient AI agents and trust
> *How might we build trust, permissions, and fail-safes into ambient personal AI agents before they become default interfaces to daily life?*
> **Panel champion**: Sandy (OpenAI policy) · **Secondary**: Nishith (infra)

### A1.1 — Receipts *(consumer activity feed for all your agents)* · 🟡 · H
One timeline of what every one of your AI agents did today; one-tap revert; anomaly flags.
- ✅ Plugs into the 2026 C2PA moment (Pixel 10 ships signed photos by default)
- ✅ Demo-friendly: scripted "agent tries mass-email → blocked" lands in 30 seconds
- ⚠️ Demand is early — most users don't yet have 3+ autonomous agents
- ⚠️ Requires integration with closed ecosystems (ChatGPT connectors) — brittle

### A1.2 — Guardian Mode for Teens · 🟢 · H
Parent dashboard showing what AI agents a teen uses, what they ask, what agents did, spend.
- ✅ Rare consumer white space; parents actively worried in 2026
- ✅ Natural distribution via concerned-parent network
- ⚠️ Teen pushback / privacy debate can overshadow demo
- ⚠️ Surveillance optics — frame carefully

### A1.3 — Trust Budgets · 🟡 · M
Give each agent a daily "budget" (spend, messages, file writes); exceed → human in loop.
- ✅ Clean mental model; judges immediately grok it
- ⚠️ "Rate limit" is a thin primitive alone — needs a product wrapper
- ⚠️ Enterprise-flavored; less emotional for consumer judges

### A1.4 — Agent Firewall *(browser extension)* · 🟢 · M
Intercepts any agent's outbound action inside the browser; shows a "why" before fire.
- ✅ Installs anywhere ChatGPT/Claude/Gemini runs
- ⚠️ Browser-extension demos are fiddly and feel tech-y
- ⚠️ Extension sprawl — competes for attention with real product

### A1.5 — Kill Switch Network · 🟢 · M
One button revokes every agent's credentials across every service.
- ✅ Memorable "break glass" demo moment
- ⚠️ Once the moment is over, there's no recurring use
- ⚠️ OAuth revocation is per-service and painful to genuinely build

### A1.6 — AI Action Insurance · 🟢 · L
Micro-insurance wrapping agent actions (wrong flight, mistaken send).
- ✅ Genuinely novel primitive; no competitors
- ⚠️ Not a demo — it's a business model; hackathon-hostile
- ⚠️ Underwriting logic impossible in a weekend

### A1.7 — Agent Escrow · 🟢 · L
Two agents propose, third signs off for financial actions.
- ✅ Conceptually elegant
- ⚠️ Requires a plausible multi-agent ecosystem to demo
- ⚠️ "Two LLMs argue" makes engineers (Nishith) roll eyes

---

## Challenge 2 · A2 — Fragile authenticity in a synthetic world
> *How might we design lightweight authenticity and provenance systems that help people verify what is real, human, and trustworthy in everyday interactions?*
> **Panel champion**: Sandy

### A2.1 — Anti-Deepfake Family Word · 🟢 · H
Per-contact "safe words" shown in a trusted UI before any voice/video call; blocks impersonation scams.
- ✅ Extremely current: 2026 voice-clone scam wave; judges will know stories
- ✅ Demo-able with two phones in 60 seconds
- ✅ Bing Wen + CPF resonance (elderly scam-protection)
- ⚠️ Only useful when the bad thing happens; retention story is thin

### A2.2 — Real-Friend Directory · 🟢 · H
Social graph where every edge is a signed in-person meet-up (NFC handshake).
- ✅ Inverts "prove you're human" to "prove we've met" — genuine reframing
- ✅ Feels fresh + memorable to judges
- ⚠️ Network-effect product; cold-start obvious
- ⚠️ NFC demo needs physical props — plan prop list

### A2.3 — Live Interview Integrity · 🟡 · M
C2PA-style signing for Zoom recordings; receiver verifies "this person was live, unedited."
- ✅ Rides hiring-fraud zeitgeist (AI-generated interviewees surge 2025–26)
- ⚠️ Requires Zoom integration to feel real
- ⚠️ Enterprise sale — panel's VCs may see slow GTM

### A2.4 — Content Provenance Inbox · 🟡 · M
Email client that surfaces C2PA manifests on attachments; flags synthesized content by default.
- ✅ Aligned with Outlook/Gmail 2026 provenance roadmaps
- ⚠️ Looks like a plug-in, not a product
- ⚠️ C2PA adoption still patchy → limited signal to display

### A2.5 — Real Review Badge · 🟡 · M
Platform plugin proving reviewer is a human who actually used the product (receipt + liveness).
- ✅ Clear problem; Amazon-review fatigue is universal
- ⚠️ Platform-dependent; requires buy-in from marketplaces
- ⚠️ Fake-review ecosystem is adversarial — hackathon version looks naive

### A2.6 — Human Stamp for Messaging · 🟢 · M
Signs outgoing emails/DMs with human-presence proof (typing cadence + liveness).
- ✅ Differentiated primitive; good engineering story
- ⚠️ Biometric concerns; privacy story has to be airtight
- ⚠️ Deliverability — receiving side needs to understand the signature

### A2.7 — Hiring Authenticity Layer · 🟡 · L
ATS plugin verifying candidate identity + work samples pipeline-wide.
- ✅ Real pain; companies scared of AI-generated candidates
- ⚠️ Enterprise sale + ATS integration = nearly impossible in a weekend
- ⚠️ No consumer angle for emotional demo

---

## Challenge 3 · A3 — Unequal outcomes from AI personalisation
> *How might we ensure AI personalisation improves outcomes for underserved users, not just efficiency for those already advantaged?*
> **Panel champion**: Bing Wen (CPF inclusion), Gabrielle (student equity) · **Secondary**: James (scale)

### A3.1 — Benefit Finder Agent · 🟡 · H
Asks 10 questions, tells you which SEA welfare/subsidy/scholarship schemes you qualify for, applies for you.
- ✅ CPF/government judges (Bing Wen, Desmond) are *perfect* champions
- ✅ Real, demonstrable economic impact — not "productivity"
- ⚠️ Data acquisition (scheme criteria) is tedious; scope carefully
- ⚠️ Crowded with government-built portals that underperform — your edge must be UX, not coverage

### A3.2 — Equal AI SMS Tutor · 🟡 · M
Low-bandwidth, curriculum-pinned, Socratic tutor over SMS for SEA secondary students.
- ✅ Equity framing matches A3 perfectly; Gabrielle + Bing Wen champions
- ✅ SMS is non-trivial eng (rate limits, state, short messages) — Tech 4/5
- ⚠️ "3/5" tech risk unless the misconception classifier is real
- ⚠️ Harder to demo visually; judge expects interactive screen

### A3.3 — Prompt Translator · 🟢 · H
Rewrites a user's raw question into the prompt a power user would've written, before hitting the LLM.
- ✅ Subtle but powerful primitive; free + open-source positioning
- ⚠️ Looks like a feature, not a product; need a wrapper use case

### A3.4 — Bank-Teller AI *(voice financial literacy)* · 🟢 · M
Explains a loan, a contract, a term in local dialect/Bahasa/Tamil; no jargon.
- ✅ James (Ant International inclusion) + Bing Wen natural fit
- ⚠️ Voice in dialects is legitimately hard; scope to one language
- ⚠️ Fintech compliance — frame as education not advice

### A3.5 — Public-Clinic Nurse Agent · 🟢 · M
Preps lower-income patients for 5-minute public-clinic appointments (symptoms → best questions).
- ✅ Wanting (NHG) + Bing Wen double champion
- ⚠️ Health-adjacent liability; careful framing
- ⚠️ Harder to recruit interviews remotely

### A3.6 — Second-Chance Coach · 🟢 · M
AI career coach for people without networks: ex-offenders, returners, switchers.
- ✅ Strong equity story
- ⚠️ Sensitive user population; interview access is hard
- ⚠️ Demo with a persona is less compelling than a real user

### A3.7 — Legal Aid Co-pilot · 🟡 · M
Walks tenant/worker through a complaint or notice with plain-language templates.
- ✅ Clear economic stakes; demo-able
- ⚠️ Legal liability; scope to one jurisdiction + one case type

---

## Challenge 4 · A4 — Ageing, isolation, and independent living
> *How might we support safe, dignified independent living for ageing populations without making care feel invasive or dehumanising?*
> **Panel champion**: Bing Wen (CPF ageing), Wanting (NHG)

### A4.1 — Second Shift · 🟡 · H  ⭐
Co-pilot for the *adult child* of an aging parent — extracts daily check-in signals, redistributes load across siblings.
- ✅ No competitor targets the caregiver-not-senior; all incumbents (ElliQ, Meela, inTouch) aim at the senior
- ✅ Reuses the Coordination OS invisible-labor worldview — team already fluent
- ✅ WhatsApp-native → no hardware, no onboarding (vs ElliQ's $1.5k moat)
- ⚠️ Liability around health escalation — frame as "communication tool"
- ⚠️ Recording a parent requires careful consent UX (can't be an afterthought)

### A4.2 — Phone-Native Companion · 🟡 · H
Daily phone call to senior (no app, no device); summarizes to family.
- ✅ Zero onboarding for the senior; inTouch proves concept
- ⚠️ Competitor pattern — differentiate with SEA language/dialect
- ⚠️ Telephony costs at scale; hackathon fine

### A4.3 — Grandparent-to-Grandchild Audio Letters · 🟢 · H
AI-mediated voice notes with prompts; builds a legacy archive, reduces isolation.
- ✅ Emotionally memorable demo
- ✅ Low technical risk; high UX polish possible
- ⚠️ "Nice-to-have" framing — needs urgency story to score Fit

### A4.4 — Hawker-Centre Buddy · 🟢 · M  ⭐
Books group meals for lonely elderly in the same neighborhood, by dialect/dietary needs.
- ✅ Extremely SEA-specific; SG VCs + Bing Wen reward cultural grounding
- ✅ No competitor; real loneliness data in SG
- ⚠️ Two-sided (who runs the other end?) — solve with community-center partner
- ⚠️ Physical-world logistics = demo-day risk

### A4.5 — Medication Story · 🟢 · M
Instead of pill reminders, a narrative agent weaves meds into daily ritual ("after your morning kopi…").
- ✅ Human-dignity framing matches the challenge language
- ⚠️ Medication adherence is a crowded pharma-funded space
- ⚠️ Clinical validation needed — Wanting will probe

### A4.6 — Dignity-First Care Logging · 🟢 · M
Carers log mood/meals in natural language; AI summarizes for doctors.
- ✅ Non-invasive framing maps 1:1 to challenge prompt
- ⚠️ Looks like a note-taker until the summarization quality shows

### A4.7 — Passive-Sound Home Monitor · 🟢 · L
Smart-speaker microphone detects falls/silence/confusion; zero wearables.
- ✅ Elegant "no-device" story
- ⚠️ Hardware + audio ML = heavy; can't demo in a weekend
- ⚠️ Privacy framing is a minefield

---

## Challenge 5 · A5 — AI Adoption Gap Becomes Power Gap *(AIF)*
> *How might we design AI learning environments that increase experimentation confidence among teenage girls before self-selection away from tech begins?*
> **Panel champions**: Janet (AIF sponsor), Hester (Epic Angels), Gabrielle (SMU)

### A5.1 — Agentic Playground for Teen Girls · 🟡 · M  ⭐
Template-based agent composer; build-a-bot for problems in a girl's own life. *Combo-review #1.*
- ✅ Three AIF-panel champions ready to advocate
- ✅ Real tech (templates + natural-language config + deploy) → scores Tech 5/5
- ⚠️ Agent-builder space has incumbents (Replit Agent, Lovable, Gumloop) — differentiate via audience, not mechanics
- ⚠️ Sprawl risk; tight-anchor discipline needed

### A5.2 — Fandom Agents · 🟢 · H
Agent-builder positioned around K-pop/Swift/BookTok fandoms (spoiler blockers, lyric bots).
- ✅ Meets teen girls where they already are
- ✅ Viral distribution mechanic built into the user culture
- ⚠️ "Fandom" framing can read as un-serious to VCs — balance the pitch

### A5.3 — Anti-Imposter Agent Gallery · 🟢 · H
Public gallery of *messy, in-progress* girl-built agents (not polished) — normalizes "my thing doesn't work yet."
- ✅ Psychologically on-point for the A5 root cause
- ✅ Shippable in a weekend; strong visuals
- ⚠️ Needs a seed of real agents; organic content is hard in remote week

### A5.4 — Mom-Daughter AI Nights · 🟢 · H
Kit + guided flow for mother + teen daughter to build an agent together.
- ✅ Reverses "dad teaches son to code" cultural default
- ✅ Hester (Epic Angels) will love this
- ⚠️ Two-user-at-once demo is tricky on stage

### A5.5 — Claude-Club-in-a-Box · 🟢 · H
Teacher-ready curriculum + sandbox for all-girls secondary schools; plug-and-play 6-week AI unit.
- ✅ Distribution through schools = built-in scale
- ✅ Gabrielle (SMU) natural ally
- ⚠️ Institutional sale friction; hackathon ships to one school at most

### A5.6 — AI Pen Pal · 🟢 · M
Two teen girls in different countries co-build an agent that translates + moderates their chat.
- ✅ Cross-cultural + collaborative = warm story
- ⚠️ Two-sided matching; cold-start in a weekend

### A5.7 — AI Confidence Coach · 🟡 · M
Tracks prompt-to-build ratio over time; celebrates wins; peer-shares experiments.
- ✅ Confidence-centric framing directly maps to challenge
- ⚠️ Measurement without an underlying build tool is hollow — pair with A5.1

---

## Challenge 6 · B1 — Slow conversion from skills to income
> *How might we help people convert newly learned skills into real income within weeks instead of years?*
> **Panel champion**: Gabrielle · SEA VCs secondary

### B1.1 — Practice Client Agent · 🟢 · H
A simulated "client" the learner works with for 2 weeks — real-feeling brief, feedback, revisions; output becomes portfolio piece.
- ✅ No marketplace cold-start — it's software
- ✅ Great demo: judge becomes the learner; client agent argues back
- ⚠️ "AI pretends to be a client" can feel gimmicky without a pedagogy story

### B1.2 — Course-to-Case-Study · 🟡 · M
Every course completion ships a deployable mini-product (not a cert) the learner can sell.
- ✅ Real artifact, not credential
- ⚠️ Requires course-platform integration or scraping
- ⚠️ "Ship" is overloaded — define precisely

### B1.3 — Micro-Agency in a Box · 🟡 · H
New grad fronts an AI-run agency; AI does the work, grad manages clients.
- ✅ Business-model clarity; VCs like it
- ⚠️ Quality liability if AI delivers poorly
- ⚠️ Near-identical to current AI-agency startups flooding SEA

### B1.4 — First-Gig Engine · 🟡 · M
Generates 5 plausible paid projects from a student's completed course; AI pitches them to real local businesses.
- ✅ Closes the "learn → earn" loop directly
- ⚠️ Cold outreach at scale is the whole product; hackathon demo is a mock
- ⚠️ Risk of looking like spam to real SMEs

### B1.5 — Local Client Scouting Bot · 🟡 · M
Scans local FB groups / Telegram / Reddit for "need a freelancer who can X"; routes to learners.
- ✅ Zero-friction demand discovery
- ⚠️ ToS issues on scraping
- ⚠️ Crowded category — Upwork/Contra adjacents exist

### B1.6 — Skill Stack Mapper · 🟢 · M
"Your React + Figma + Mandarin gets you these 8 Taobao-dropshipper gigs"; cross-lists skills into niche markets.
- ✅ Genuinely novel lens on the same underlying gig data
- ⚠️ Sparse data in niche markets; demo is data-heavy

### B1.7 — Pay-on-Proof Learning · 🟢 · L
Learn free; pay a small fee only when first paid gig materializes.
- ✅ Strong business-model story
- ⚠️ Not a hackathon demo — it's a pricing page
- ⚠️ Attribution mechanics are thorny

---

## Challenge 7 · B2 — Lack of low-friction entry points to earning
> *How might we create legitimate, low-friction ways for people to start earning without relying on resumes, formal credentials, or prior job history?*
> **Panel champion**: Gabrielle · SEA VCs

### B2.1 — Karaoke Resume · 🟡 · H
Replace resume with 90-second video + live skills challenge; AI assembles a capability card.
- ✅ Demo-ready in 2 minutes with any judge
- ✅ Rides portfolio-over-resume 2026 trend
- ⚠️ "Video resume" has graveyards — your twist is the live challenge, emphasize it

### B2.2 — Intern for a Day · 🟡 · H
Companies list 1-day paid shadowing; students apply via one AI-screened question.
- ✅ Low-stakes for both sides; real earning
- ⚠️ Two-sided; needs real company partner in remote week
- ⚠️ Legal/intern-classification risk in some jurisdictions

### B2.3 — Task-Bite Marketplace · 🟡 · M
30-min AI-assisted tasks posted by real businesses; AI grades, pays per quality bucket.
- ✅ Hits B2 dead-center
- ⚠️ Marketplace cold start; demo must fake the supply side
- ⚠️ Crowded (Fiverr, Upwork adjacencies)

### B2.4 — Local Errand + Brain Mix · 🟢 · M
Platform mixes physical errands and micro-knowledge tasks for same client (deliver groceries + digitize menu).
- ✅ Novel combination; SEA-flavored
- ⚠️ Two dispatch systems to build; scope creep obvious

### B2.5 — Tip-Jar Learning · 🟢 · M
Learn by answering questions in niche Discord/Telegram communities; community tips = income.
- ✅ Zero formal entry; community-native
- ⚠️ Payment rails in unregulated chat spaces are friction
- ⚠️ AI vouching for answers is where the tech actually lives — keep that central

### B2.6 — Paid Open-Source Onboarding · 🟡 · M
AI scouts beginner-friendly bounties across OSS; walks you through first PR.
- ✅ Real, prestigious output
- ⚠️ OSS-bounty ecosystem is thin outside crypto
- ⚠️ Developer-only — limits audience

### B2.7 — First-Paycheck Guarantee · 🟢 · L
App pays you $20 for your first real task attempt; recoups from client on completion.
- ✅ Psychological unlock is real
- ⚠️ Capital + fraud risk; hackathon can't demo
- ⚠️ Unit economics need a real marketplace — chicken-and-egg

---

## Challenge 8 · B3 — Weak connection between learning and real work
> *How might we connect learning directly to projects, clients, and measurable outputs so capability is built through real work?*
> **Panel champion**: Gabrielle

### B3.1 — Course Dropout Rescue · 🟢 · H  ⭐
When a user abandons a course, AI generates one real-world application of what they already learned, so they ship something.
- ✅ Unique, under-served moment — nobody builds for the dropout
- ✅ Easy to demo with any learner + any abandoned course
- ⚠️ User acquisition depends on being in the dropout moment — requires distribution partner

### B3.2 — Retrospective Portfolio · 🟢 · M
Scans your phone/laptop history; auto-drafts a portfolio of what you *actually* did last year.
- ✅ Novel primitive; no competitor
- ⚠️ Privacy-sensitive — consent UX is the whole product
- ⚠️ Messy real data → messy output; polishing is hard in weekend

### B3.3 — Receipt for Learning · 🟡 · H
Every hour of learning emits a verifiable artifact (code, doc, Loom); portfolio auto-accretes.
- ✅ Pairs cleanly with Capability Card (B5.1)
- ⚠️ "Receipt" metaphor overlaps Coordination OS — distinguish clearly

### B3.4 — Syllabus Mirror · 🟡 · H
Mirrors the user's syllabus with "here's how a working pro does this each week."
- ✅ Simple, relatable; direct challenge fit
- ⚠️ Content curation is the product — at scale, a data problem

### B3.5 — Real-Brief Every Lecture · 🟢 · M
Every lecture auto-generates a mini-brief from a real local company; students compete; winner paid.
- ✅ Institutional buy-in possible via SMU (Gabrielle)
- ⚠️ Requires real company briefs weekly — logistics heavy

### B3.6 — Graded-by-Client · 🟢 · M
After each project, the actual client grades the work; replaces GPA with client-NPS.
- ✅ Direct mapping to "measurable outputs"
- ⚠️ Client participation unreliable; gaming is easy
- ⚠️ Sits on top of a marketplace you don't have

### B3.7 — Professor-as-PM · 🟡 · L
Turns syllabi into sprint plans with NGO/startup clients as PMs.
- ✅ Structurally reshapes learning
- ⚠️ Institutional sale; entirely out of a weekend's reach

---

## Challenge 9 · B4 — Entry-level work is being compressed by AI
> *How might we create new AI-leveraged pathways for early-career workers to build proof of ability and income in a labor market with fewer traditional entry roles?*
> **Panel champions**: Gabrielle · VCs

### B4.1 — Reverse-Internship · 🟢 · H  ⭐
Students *teach* companies how to use AI while the company teaches them the business — paid reverse mentoring.
- ✅ Fresh reframing; memorable pitch line
- ✅ Real pain: SMEs want AI help, students have no job — direct match
- ⚠️ Matching is two-sided; demo needs mock company
- ⚠️ Quality control on junior-led advice — frame as "pair learning"

### B4.2 — Quality Council · 🟡 · H
Early-career workers as paid human-in-loop reviewers for AI output at scale.
- ✅ Real jobs exist today (Mercor, Scale AI); direct expansion
- ⚠️ Crowded; your edge is SEA-first and a skill-building loop
- ⚠️ Commoditized labor at $3/hour is not the story you want

### B4.3 — Ops-for-Solopreneurs Agency · 🟡 · H
Early-career workers as ops managers for one-person AI-native businesses (newsletters, indie SaaS).
- ✅ Creator economy → 2026 reality; real demand
- ⚠️ Marketplace dynamics; demo must show a real solopreneur
- ⚠️ Business model overlaps with Virtual Assistant agencies

### B4.4 — Model Auditor Certification · 🟢 · M
Short training + first gigs as model-bias/red-team auditors for SEA SMEs adopting AI.
- ✅ Sandy (OpenAI policy) bonus; real compliance market emerging
- ⚠️ Buyer education is half the battle
- ⚠️ Certification credibility takes years — frame as "first steps"

### B4.5 — Agent-Handler Role · 🟡 · M
Train workers to "shepherd" 3–5 AI agents each; charge employers per agent supervised.
- ✅ Clean positioning — "you don't lose your job, you get 5"
- ⚠️ Depends on agent-dense workplaces that are still rare
- ⚠️ Role name doesn't exist yet — have to invent the category

### B4.6 — Synthetic-to-Real Gradient · 🟡 · M
Learner completes AI-generated "fake" briefs; top performers get real paid work. *(≈ Career Launchpad)*
- ✅ Covered in combo-review #3
- ⚠️ Marketplace cold-start is the trap

### B4.7 — AI Apprentice Pipeline · 🟡 · L
Company hires junior + AI agent as a pair; junior directs, AI learns the company.
- ✅ Elegant framing of future of work
- ⚠️ Enterprise sale; hackathon can't demo
- ⚠️ Unclear what you *build* vs. what you *propose*

---

## Challenge 10 · B5 — Opportunity access is socially gated *(AIF)*
> *How might we redesign opportunity discovery so access is driven less by social capital and pedigree, and more by demonstrated potential and readiness?*
> **Panel champions**: Janet (AIF), Hester, Gabrielle

### B5.1 — Capability Card · 🟡 · H  ⭐
Signed, replayable proof-of-work card; multi-agent graded. *(See `ideas.md` #5.)*
- ✅ Rides portfolio-over-resume trend (Microsoft, Velocity, Indicio all shipping 2026)
- ✅ Multi-agent review = real Tech Execution story for Nishith
- ✅ Avoids marketplace cold-start — primitive-first
- ⚠️ "AI graded" triggers trust questions — lean into the disagreement trace

### B5.2 — Portfolio-over-Pedigree Leaderboard · 🟡 · H
Public leaderboard per skill, ranked by signed capability cards; anyone can rise.
- ✅ Pair with B5.1 for one coherent product
- ⚠️ Leaderboards invite gaming; anti-fraud is where the work lives

### B5.3 — Blind Opportunity Matcher · 🟡 · M
Employers post requirements; candidates submit only signed artifacts; name/school revealed post-shortlist.
- ✅ Direct B5 fit; AIF-aligned
- ⚠️ Two-sided; hackathon fakes one side
- ⚠️ Employer buy-in is the real GTM battle

### B5.4 — Mentor Hours Market · 🟢 · M
Mentors earn tokens per hour given; candidates earn tokens via open challenges; redeemed for face time.
- ✅ Token primitive is neat
- ⚠️ Crypto-adjacent vibe can spook non-crypto VCs
- ⚠️ Supply side (mentors) hard to activate in a weekend

### B5.5 — Anti-Bro Pipeline · 🟢 · M
Companies opt-in to sourcing from overlooked communities (polytechnics, returners, rural unis); AI surfaces top signal.
- ✅ Direct AIF-D6 framing
- ⚠️ Enterprise sale; relies on company-side DEI commitment
- ⚠️ Demo is a sourcing pipeline, not a UI moment

### B5.6 — Network Simulator · 🟢 · M
AI assembles a warm-intro path to any person from your existing graph.
- ✅ Clean demo ("how do I get to X?")
- ⚠️ LinkedIn ToS; privacy questions from Sandy
- ⚠️ Feels tactical rather than foundational

### B5.7 — Hidden-Role Radar · 🟡 · L
Scrapes unposted jobs from founder tweets/Discord/LinkedIn posts; routes to matched candidates.
- ✅ Real behavior — jobs do live on social
- ⚠️ Scraping ToS; legal uncertainty
- ⚠️ Sales-ey vibe — frame as candidate advocate

---

## Challenge 11 · C1 — Priority collapse in high-noise environments
> *How might we help people identify and act on their highest-priority work in environments where everything competes for attention?*
> **No dedicated champion** · crowded space (Motion, Superhuman, Shortwave, Notion AI, Gmail+Gemini). Enter only with a sharp edge.

### C1.1 — Priority Sniff Test · 🟡 · H
Forwarding address: paste anything in, get "urgent / important / noise" verdict with reasoning.
- ✅ Zero-install; minimal scope
- ⚠️ Feature, not product — pair with something else
- ⚠️ Core prompt is Claude-in-a-wrapper — push tech depth

### C1.2 — Priority Peer Review · 🟢 · H
Pairs two friends who see each other's top-3; can challenge "why is this on your list?"
- ✅ Genuine white space; social twist incumbents won't copy
- ⚠️ Two-sided from day 1
- ⚠️ Vulnerability required — adoption is cultural

### C1.3 — One-Tap Triage · 🔴 · H
Deal now / schedule / ignore; weekly replay trains a personal model.
- ✅ Memorable simplicity
- ⚠️ Every competitor ships this now
- ⚠️ Edge is the personal-model replay — make that the headline

### C1.4 — Top 3 Cards · 🔴 · H
Single screen, three things that matter, recomputed every 30 min.
- ✅ Clean product; fast demo
- ⚠️ Exactly what Superhuman ships; you lose unless something is radically different

### C1.5 — Calendar Ghostwriter · 🔴 · H
Scans the week's meetings; tells you which to skip with a draft decline.
- ✅ Visceral pain point
- ⚠️ Motion + Reclaim directly compete

### C1.6 — Spotlight Mode · 🔴 · M
Deadline-aware day rewriter based on what's actually due.
- ⚠️ Motion already does this
- ⚠️ Fit score will be "derivative"

### C1.7 — Deep Work Lock · 🔴 · M
Detects flow, silences surfaces, escalates only rule-matched events.
- ⚠️ Brick-and-mortar productivity; unless framing is fresh, skip

---

## Challenge 12 · C2 — Decision fatigue from overlapping responsibilities
> *How might we reduce cognitive overload for people juggling multiple responsibilities, deadlines, and roles at the same time?*
> **No dedicated champion**; Janet/Hester if C4 framing is foregrounded.

### C2.1 — Worry Parking · 🟡 · H
Voice-dump worries; AI categorizes (controllable now / later / not yours); schedules the controllable ones.
- ✅ Emotionally resonant demo
- ✅ Real tech: intent classifier + scheduler
- ⚠️ "Journaling app" adjacency; differentiate with action

### C2.2 — One-Question Morning · 🟡 · H
One question you actually need to answer today. No lists.
- ✅ Poetic, memorable; interview-friendly
- ⚠️ Behind the simplicity must be real context aggregation

### C2.3 — Say-No Assistant · 🟡 · H
Drafts a polite, in-your-voice decline to any request that doesn't fit current top-3.
- ✅ Universal pain; demo hits in 30 seconds
- ⚠️ Must integrate with inbox to be real

### C2.4 — Default-Choice Engine · 🟡 · H
Proposes a default action; you veto if needed. Most days you won't.
- ✅ Inverts the UX of productivity tools
- ⚠️ Defaults wrong → catastrophic trust break; demo carefully

### C2.5 — Role Switcher · 🟡 · M
Explicit "Student mode / Daughter mode / Intern mode" UI; surfaces only that role's signals.
- ✅ Direct C2 framing; under-built
- ⚠️ Switching manually is friction; nail the triggers

### C2.6 — Decision Log · 🟢 · M
Captures your micro-decisions; pattern-matches to propose auto-decisions later.
- ✅ Novel behavioral data
- ⚠️ Privacy; long runway before value

### C2.7 — Responsibility Map · 🟡 · M
Graph of open responsibilities; shows which are blocking most others.
- ✅ Visually striking
- ⚠️ Graph apps are a known productivity-tooling graveyard

---

## Challenge 13 · C3 — Fragmented communication across platforms
> *How might we unify fragmented communication into clear, actionable next steps without requiring users to constantly monitor every platform?*
> **No dedicated champion** · crowded

### C3.1 — Conversation Resurrection · 🟢 · H
Finds threads you abandoned 3+ weeks ago; asks if you want to close them.
- ✅ Novel angle; fills the "other direction" nobody covers
- ⚠️ Low-frequency use — may not feel daily
- ⚠️ Requires multi-platform read access

### C3.2 — Deadline Harvester · 🟡 · H
Scans all messages for implicit deadlines ("by Friday"); converts to calendar holds.
- ✅ Clear demo; obvious value
- ⚠️ Motion/Reclaim adjacency; edge is cross-platform coverage

### C3.3 — Voice-First Inbox · 🟡 · H
Reads messages to you on commute; you reply by voice; AI formats per platform.
- ✅ Demo-able with Airpods; differentiated surface
- ⚠️ Voice-first has many graveyards

### C3.4 — Follow-up Scoreboard · 🟡 · M
Every person waiting on you, every person you're waiting on, across platforms.
- ✅ Alfred_-style wedge, but broader
- ⚠️ Close to Coordination OS core — may collapse into that

### C3.5 — Channel Consolidator · 🟢 · M
Proposes "these three Slacks could be one" based on who-talks-to-whom.
- ✅ Novel; real pain for team ops
- ⚠️ Enterprise-flavored; consumer appeal thin

### C3.6 — Unified Thread View · 🔴 · M
Same conversation across Slack + email + WhatsApp stitched into one thread.
- ⚠️ Everyone attempts this; execution is brutal
- ⚠️ Platform ToS make it hard to ship for real

### C3.7 — Cross-Platform Action Inbox · 🔴 · M
Every "reply-expected" message in one queue; one-click reply back to source.
- ⚠️ Incumbent territory; no obvious edge

---

## Challenge 14 · C4 — Invisible cognitive labor *(AIF)*
> *How might we reduce invisible coordination labor, stop it from defaulting to women disproportionately, and overall preserving the human quality of relationships and collaboration?*
> **Panel champions**: Janet (AIF), Hester · **Secondary**: Bing Wen if framed as caregiver labor

### C4.1 — Fair Share for Students · 🟡 · H  ⭐
WhatsApp bot for student flats; infers who's doing what from group chat; surfaces imbalance.
- ✅ All 7 household-ops apps target married-with-kids — students are white space
- ✅ Zero install (group-chat-native); Janet + Hester champion
- ✅ Chat history = unfair data moat vs. quiz-based competitors (Dame, FairChore)
- ⚠️ Consent UX for ingesting chats must be the demo centerpiece
- ⚠️ WhatsApp Business API edge cases — test early

### C4.2 — Event Ops Agent · 🟡 · H
For group events: "who's bringing what, who's been reminded, who hasn't RSVP'd."
- ✅ Demo-able at any birthday; universal pain
- ⚠️ Narrow use case alone — pair with C4.5

### C4.3 — Family Birthday Butler · 🟢 · H
Plans every family birthday (gift shortlist, card draft, venue options).
- ✅ Emotional demo; Hester will love
- ⚠️ Seasonal / low-frequency; retention story thin

### C4.4 — Group Chat Ghostwriter · 🟡 · H
Drafts the "just checking in" messages one person always ends up sending.
- ✅ Micro-moment everyone recognizes
- ⚠️ Feature-size, not product — wrap with C4.1 ledger

### C4.5 — Auto-RSVP Agent · 🟡 · H
Replies on your behalf to "who's free on X?" messages via calendar + preferences.
- ✅ Clear demo; shared with Coordination OS
- ⚠️ Edge cases (which "X" nights count as free?) — need guardrails

### C4.6 — Coordination Labor Dashboard · 🟡 · M
Measures reminders sent / nudges absorbed per week. *(Existing Coordination OS direction.)*
- ✅ Team already building; detailed plan exists
- ⚠️ No dedicated panel champion; crowded around the edges

### C4.7 — Mental Load Diff · 🟡 · M
Compare invisible-labor receipts with partner/roommate/sibling; visualize gap, not blame.
- ✅ AIF-aligned; visually striking
- ⚠️ Requires two-person opt-in — friction

---

## Challenge 15 · D1 — Preventive health feels inaccessible
> *How might we make preventive health and longevity actionable, affordable, and embedded into everyday routines?*
> **Panel champions**: Wanting (NHG), James (scale)

### D1.1 — Morning 3-Minute Check · 🟡 · H
Daily 3-min scan (sleep + mood + symptom); builds a year-long trendline; flags drift.
- ✅ Demo-able in 3 minutes; Wanting-friendly if trendline has real model
- ⚠️ Habit-tracker adjacency (Oura, Whoop) — edge must be in the inference

### D1.2 — Hawker Longevity · 🟡 · M
SEA-contextualized longevity coach built around hawker food + public-transit movement. *(Combo-review #5.)*
- ✅ Strong SEA-judge fit; culturally specific
- ⚠️ Wellness-app pattern; push Tech up via a real pipeline

### D1.3 — Clinic-Ready Briefings · 🟢 · H
Before a check-up, assembles a 1-page "here's what I've noticed in 6 months" for the doctor.
- ✅ Wanting (NHG) is the exact persona to love this
- ✅ No competitor pushes this direction
- ⚠️ Requires some health data — HealthKit or mocked

### D1.4 — Habit Cost Calculator · 🟡 · H
"Your 5 bubble teas/week = 1.8 kg fat/year" — emotional math, not finger-wagging.
- ✅ Viral-friendly, demo-friendly
- ⚠️ Thin on its own; wrap with a program

### D1.5 — $5 Longevity Stack · 🟢 · H
Concierge for cheapest evidence-grade interventions (walking, sleep, cheap protein); rejects supplement noise.
- ✅ Anti-Bryan-Johnson positioning stands out
- ⚠️ "Just walk" is a hard sell as a product

### D1.6 — Boring Health OS · 🟢 · H
Shows the 5 things that actually move the needle; hides the 500 that don't.
- ✅ Minimalist pitch works well on stage
- ⚠️ Opinionated content curation is the product

### D1.7 — Neighbourhood Walking Challenge · 🟡 · H
HDB-block-level step competition; AI creates routes around local MRT.
- ✅ Social layer + SG-specific
- ⚠️ Social-fitness graveyard is vast

---

## Challenge 16 · D2 — Unsafe experimentation in health optimisation
> *How might we support safe, evidence-aware health experimentation without pushing users into misinformation or over-optimisation?*
> **Panel champion**: Wanting · **Secondary**: Sandy (if framed as safety infra)

### D2.1 — Claim Lookup · 🟡 · H
Paste any TikTok/IG health claim → 3-sentence verdict with citation quality.
- ✅ Viral potential; demo hits in 10 seconds
- ⚠️ Arms race with new claims; evidence base must be real
- ⚠️ Liability if wrong — frame as literacy

### D2.2 — Evidence-Grade Chat · 🟡 · H
Biohacking chatbot that *always* shows evidence level (meta-analysis vs. tweet).
- ✅ Wanting-perfect; Tech story = real ranking pipeline
- ⚠️ Data-heavy; scope to one domain (e.g. supplements)

### D2.3 — Supplement Interaction Agent · 🟡 · M
Log what you take; AI flags stack interactions + evidence strength.
- ✅ Direct, useful, testable
- ⚠️ DrugBank ingestion is a weekend killer — use hardcoded top 20

### D2.4 — Self-Experiment Log · 🟢 · M
N=1 trial framework: hypothesis, baseline, variable, duration.
- ✅ Genuinely novel for consumer health
- ⚠️ Requires scientific literacy to use; onboarding matters

### D2.5 — Red-Flag Radar · 🟢 · M
Watches purchase + search + social; flags when you're going down a dangerous rabbit hole.
- ✅ Unique intervention moment
- ⚠️ Deep permissions needed; privacy story heavy

### D2.6 — Rollback Protocol · 🟢 · M
"Revert all my health experiments to baseline"; generates taper/wean plan.
- ✅ Novel primitive
- ⚠️ Medical caution; must route to professional for anything serious

### D2.7 — Doctor-in-the-Loop · 🟡 · L
Subscribe to a real doctor who reviews self-experiments monthly for $20.
- ✅ Trust moat
- ⚠️ Marketplace + licensing — hackathon-hostile

---

## Challenge 17 · D3 — Poor fit of Western health defaults in Asian contexts
> *How might we build health and longevity systems that are adapted to Asian genetics, diets, climates, and work cultures?*
> **Panel champion**: Wanting

### D3.1 — Asian-Context Nutrition Coach · 🟢 · H
Every recommendation in rice/noodle/hawker terms, not quinoa.
- ✅ Extremely on-challenge; SEA VCs instantly get it
- ⚠️ "Context" alone can feel like a skin over existing apps — deepen the pipeline

### D3.2 — Monsoon Exercise Planner · 🟢 · H
Schedules outdoor movement around humidity/haze/PSI; swaps indoor alternatives dynamically.
- ✅ Hyper-local; no one outside SEA ships this
- ⚠️ Weather-API demo risk if no live feed; mock for stage

### D3.3 — Chopsticks Portion Control · 🟡 · H
Computer vision on your phone photo of a hawker tray → portion vs. target.
- ✅ Visually wow demo
- ⚠️ CV accuracy in cluttered scenes — stage with controlled photos

### D3.4 — Rice-Glycemic Optimizer · 🟢 · M
Real-time glycemic predictor based on rice type + sides + eating order.
- ✅ Grounded, research-backed angle (Spector-style)
- ⚠️ CGM adoption gates this for consumer use

### D3.5 — ALDH2 Alcohol Warning · 🟢 · M
Cheap genetic test + lifetime flushing-risk tracker; culturally tuned nudges.
- ✅ Only makes sense in Asia — pure D3 fit
- ⚠️ Genetic test logistics; demo with mock result

### D3.6 — Chinese Medicine Translator · 🟢 · M
Maps TCM diagnoses to Western-medicine equivalents; bridges cross-generational conversations.
- ✅ Novel, warm story
- ⚠️ Wanting may probe TCM evidence bridging — handle carefully

### D3.7 — Shift-Worker Sleep Coach · 🟡 · M
Circadian guidance for hawker aunties, nurses, security; non-9-to-5 Asian work.
- ✅ Real, ignored user segment
- ⚠️ Interviews in remote week are doable via labor unions

---

## Challenge 18 · D4 — Hidden burnout among caregivers
> *How might we better support caregivers' energy, resilience, and mental health before burnout becomes chronic?*
> **Panel champions**: Wanting, Bing Wen · **Secondary**: Hester

### D4.1 — Second Shift · 🟡 · H  ⭐
*(See A4.1.)* Adult-child eldercare co-pilot + sibling load redistribution.
- ✅ Same idea, different primary challenge — it's a 3-challenge hit
- ✅ SG-specific ageing realities; Bing Wen + Wanting champions
- ⚠–⚠️ Same risks as A4.1 — liability framing, consent UX

### D4.2 — One Sentence a Day · 🟢 · H
Caregiver voices one sentence about their day; AI builds a resilience journal they re-read.
- ✅ Emotional; low-friction; visually simple
- ⚠️ Retention risk; needs a why-come-back loop

### D4.3 — Inherited-Task Handoff Tool · 🟢 · H
When siblings rotate duty, generates a "here's everything you need to know" brief.
- ✅ Direct cross-sibling pain; pairs with D4.1
- ⚠️ Feature-size; wrap with Second Shift

### D4.4 — Caregiver Peer Circles · 🟡 · H
AI-matched 5-person groups of caregivers in similar situations; async support with summaries.
- ✅ Community product; warm demo
- ⚠️ Supply side (real caregivers) — interview recruiting is possible via churches / elder-care orgs

### D4.5 — Respite Agent · 🟢 · M
Books 2-hour respite windows; arranges backup care; handles the caregiver's "guilt script."
- ✅ Direct D4 fit
- ⚠️ Backup-care marketplace is real GTM cost

### D4.6 — Admin Inbox Absorber · 🟡 · M
Takes over admin side of caregiving (claims, appointments, insurance).
- ✅ Clear labor absorption
- ⚠️ MediSave/insurance API access is not casual

### D4.7 — Burnout Early Warning · 🟢 · M
Passively watches phone usage + texts tone; flags drift toward burnout.
- ✅ Novel intervention moment
- ⚠️ Surveillance optics — frame as self-chosen

---

## Challenge 19 · D5 — Health literacy starts too late
> *How might we help young people make informed long-term health decisions earlier, using empowering rather than fear-based systems?*
> **Panel champions**: Wanting, Gabrielle

### D5.1 — Teen-Safe Body Literacy Chat · 🟡 · H  ⭐
Answers the awkward questions (sleep, reproductive, skin, mental health) teens won't ask adults.
- ✅ Universal pain; genuine demand
- ✅ AIF-adjacent (teen girls especially benefit)
- ⚠️ Safeguarding — must have guardrails against self-harm / abuse topics
- ⚠️ Health liability; frame as education

### D5.2 — School Canteen Hero · 🟢 · H
Shows which canteen items move which longevity metrics, in teen-relevant language.
- ✅ Hyper-SG specific; Wanting-compatible
- ⚠️ Menu data acquisition per school — scope to one

### D5.3 — TikTok Nutrition Translator · 🟢 · M
Plugin that overlays evidence-grading on health TikToks as teens scroll.
- ✅ Native to teen habitat
- ⚠️ Browser/OS extension reach on TikTok is limited
- ⚠️ Arms race with new content

### D5.4 — Compound Health Bank · 🟡 · H
"Interest" metaphor showing today's choices compounding 20 years out; gamified.
- ✅ Strong pitch visual
- ⚠️ Borderline fear-framing — tone is whole game

### D5.5 — Peer-Audit Health Buddy · 🟢 · H
Pairs two teens; grade each other's habits weekly; AI moderates.
- ✅ Social accountability layer
- ⚠️ Matching dynamics; privacy among minors

### D5.6 — Future-Me Simulator · 🟡 · M
Shows your future self at 40 based on current habits; updates weekly.
- ✅ Viral visual
- ⚠️ Gimmick risk unless the model is real
- ⚠️ Shades into fear-based narrative if not careful

### D5.7 — Parent-Teen Health Compact · 🟢 · M
Both opt in; AI brokers shared goals without surveillance.
- ✅ Dignified framing
- ⚠️ Two-user product; demo complexity

---

## Challenge 20 · D6 — Fertility window vs career acceleration *(AIF)*
> *How might we build decision-support tools that give young women realistic, empowering data about long-term life planning — without fear-based narratives?*
> **Panel champions**: Janet, Hester, Wanting

### D6.1 — The Numbers, Honestly · 🟢 · H  ⭐
Data dashboard stripped of marketing: real AMH curves, IVF outcomes, egg-freezing by age.
- ✅ Closest literal match to the challenge wording
- ✅ Demo-ready with public data; 3 AIF champions + Wanting
- ⚠️ Presentation tone is the product — UX design is 90% of success
- ⚠️ Liability: frame as information tool, not medical advice

### D6.2 — Policy Finder for Families · 🟡 · H
Every maternity/paternity/elder-care benefit in SG/MY by employer; applies for you.
- ✅ Bing Wen (CPF) + Janet double-champion
- ✅ Concrete economic value
- ⚠️ Policy data maintenance; scope to SG first

### D6.3 — Career Pause Calculator · 🟢 · H
Models the career impact of taking 6/12/24 months off — by industry, seniority, country.
- ✅ Directly addresses the D6 trade-off
- ⚠️ Requires credible salary-curve data — use Glassdoor-adjacent

### D6.4 — Real Stories Library · 🟡 · H
Curated, searchable library of actual women's paths; AI matches your profile.
- ✅ Warm, non-datafied counterweight
- ⚠️ Content sourcing is the product; hard in a weekend

### D6.5 — Life Compass · 🟢 · M
Scenario simulator across 5 life paths with probability bands. *(See `ideas.md` #6.)*
- ✅ Most ambitious; simulator = real Tech
- ⚠️ Monte Carlo + LLM narrative = significant weekend scope

### D6.6 — Couple Alignment Tool · 🟢 · M
He-and-she joint simulator; surfaces misaligned expectations.
- ✅ Novel social product
- ⚠️ Two-user UX; sensitive conversations

### D6.7 — Fertility-Aware Career Coach · 🟢 · M
Career advice that factors fertility goals without making it the centerpiece.
- ✅ Integrative framing
- ⚠️ Dual-domain expertise hard to build in prompts alone

---

## Challenge 21 · E1 — AI-native infrastructure for agent systems
> *How might we build infrastructure designed for AI-to-AI interaction, rather than retrofitting human-centered software for agent workflows?*
> **Panel champion**: Nishith

### E1.1 — MCP Discovery Registry · 🟢 · M
Yellow pages for MCP servers; ranked, reviewed by other agents.
- ✅ Real gap in 2026 MCP ecosystem
- ⚠️ Infra demo is hard; looks like a directory

### E1.2 — Eval-as-a-Service for Agents · 🟡 · M
Real-time evaluation middleware grading every agent response before it reaches the user.
- ✅ Pairs with Receipts (A1.1) philosophically
- ⚠️ Benchmarks-as-a-product is well-trodden (LangSmith, Braintrust)

### E1.3 — Semantic Webhooks · 🟢 · M
Webhook payloads in natural language + structure; any agent comprehends.
- ✅ Elegant; Nishith will grok immediately
- ⚠️ Needs a receiver ecosystem to feel real

### E1.4 — Shared Memory Bus · 🟢 · M
Cross-agent memory layer — agents on same user's behalf read each other's context.
- ✅ Foundational primitive
- ⚠️ Privacy story is heavy; security review in a weekend impossible

### E1.5 — Agent Rate-Limit Negotiator · 🟢 · M
Two agents negotiate API windows instead of hammering endpoints.
- ✅ Cute, novel
- ⚠️ Demo is niche; value requires scale

### E1.6 — Agent Conflict Mediator · 🟢 · L
Third agent arbitrates when two agents take opposing actions.
- ✅ Interesting multi-agent story
- ⚠️ Multi-LLM demos feel contrived on stage

### E1.7 — Agent-Native Auth · 🟢 · L
OAuth replacement designed for agent principals — scoped, revocable, delegable.
- ✅ Real whitespace
- ⚠️ Standards-body product; not a weekend win

---

## Challenge 22 · E2 — Governance, permissions, auditability for autonomous systems
> *How might we design agent systems with safety, permissions, and auditability built in by default rather than added later?*
> **Panel champions**: Sandy, Nishith

### E2.1 — Agent Policy DSL · 🟡 · M
Natural-language policy editor: "My shopping agent can spend $50/day, never on subscriptions."
- ✅ Direct Sandy alignment
- ⚠️ Shades toward "Guardrails AI" turf — differentiate with NL UX

### E2.2 — Replay Debugger for Agents · 🟢 · M
Step-through debugger for what an agent did and why, usable by non-developers.
- ✅ Judges who code will love it
- ⚠️ Consumer-readability is the whole design challenge

### E2.3 — Agent Fire Drill · 🟢 · H
Monthly scheduled incident — agent pretends to misbehave; team's kill-switch scored.
- ✅ Unique take; memorable demo
- ⚠️ Novelty ages fast; retention unclear

### E2.4 — Time-Boxed Superpowers · 🟢 · M
Agent requests elevated access for 30 min with reason; auto-expires.
- ✅ Clean primitive; enterprise-ready framing
- ⚠️ Fits into Receipts / Trust Layer — may not stand alone

### E2.5 — Simulated Harm Testing · 🟢 · M
Sandbox provokes your agent with 100 edge cases before prod.
- ✅ Real engineering story
- ⚠️ Dev-facing; narrow audience

### E2.6 — Consent Ledger · 🟡 · M
Every time an agent accesses a new data source, it asks; log is tamper-evident.
- ✅ Pairs with A1.1 Receipts
- ⚠️ Heavy lift if hash-chain is the demo centerpiece

### E2.7 — Cross-Org Agent Access Review · 🟡 · L
Shows every agent running across a team + access + last action.
- ✅ Enterprise compliance fit
- ⚠️ Weekend-hostile; enterprise UX demands detail

---

## Challenge 23 · E3 — AI applied to physical systems, not just software
> *How might we apply AI directly to physical-world systems where coordination, efficiency, and safety improvements have real economic impact?*
> **Panel champions**: Nishith, James

### E3.1 — Hawker Inventory Agent · 🟢 · M  ⭐
Predicts tomorrow's ingredient needs for a hawker stall from weather + events + sales.
- ✅ Deeply SEA; James (Ant Intl) + SEA VCs
- ✅ Real physical-world payoff with tiny ML
- ⚠️ Needs a real stall partner — doable in remote week

### E3.2 — HDB Lift Queue Agent · 🟢 · M
Predicts lift wait times across HDB blocks at peak hours; nudges residents to stagger.
- ✅ Uniquely SG; novel data source
- ⚠️ Real lift data is hard to access; mock for demo

### E3.3 — Factory Floor Anomaly Voicebot · 🟢 · M
Operator voices "machine 4 making a weird noise"; AI logs + matches past tickets.
- ✅ Real industrial-SME pain
- ⚠️ Factory interview access tricky

### E3.4 — Solar-Panel Yield Agent · 🟡 · M
Residential solar owners get "your system underperformed X% because Y" alerts.
- ✅ James (sustainability) fit
- ⚠️ Niche hardware/user base

### E3.5 — Small-Fleet Route Optimizer · 🟡 · M
Dispatch for 5-person logistics SMEs that can't afford enterprise TMS.
- ✅ Clear ROI
- ⚠️ Routing is table-stakes; your edge is SEA context + price

### E3.6 — Construction Site Schedule Resolver · 🟢 · L
AI watches CCTV, re-optimizes crew schedules when trades block each other.
- ✅ Real pain
- ⚠️ CCTV access + CV = impossible in a weekend

### E3.7 — Port Waiting Time Predictor · 🟡 · L
Open API for SEA port congestion; truckers save hours.
- ✅ Real B2B value
- ⚠️ Data access is the whole product

---

## Challenge 24 · E4 — Preserving human agency in AI-mediated environments
> *How might we design human-facing AI systems that increase human capability, judgment, and agency instead of making people more passive or dependent?*
> **Panel champions**: Sandy, Gabrielle

### E4.1 — Socratic-Only Mode · 🟢 · H  ⭐
Any LLM app toggled into a mode that *only* asks questions back; never answers.
- ✅ Trivial to build; powerful demo
- ✅ Directly maps to E4 + A3 equity framing
- ⚠️ Feature, not product — wrap with a learner use case

### E4.2 — Stretch Zone Assistant · 🟢 · H
For learners, refuses to answer questions you're almost-able-to-answer yourself.
- ✅ Cognitive-science-flavored; Sandy + Gabrielle will engage
- ⚠️ Detecting "almost-able" is a real ML problem, not a prompt

### E4.3 — AI Training Wheels Off · 🟢 · H
Weekly challenges: do your normal tasks without AI; score re-acquired skills.
- ✅ Unusual framing, memorable
- ⚠️ Self-report honesty; gaming is trivial

### E4.4 — Decision Receipts · 🟢 · H
For every AI-assisted decision, you write a 1-line "why you chose this."
- ✅ Tiny primitive, real behavioral change
- ⚠️ Feature-size

### E4.5 — Dual-Author Drafting · 🟢 · H
Forces alternation — AI odd paragraphs, human evens; no full-delegation possible.
- ✅ Genuinely novel UX
- ⚠️ Annoying if forced on serious work; tone it right

### E4.6 — Dependency Meter · 🟢 · M
Tracks % of your outputs that are AI-authored vs. human-authored; alerts on drift.
- ✅ Honest mirror; Sandy will like the policy implications
- ⚠️ Attribution is the hard problem

### E4.7 — Skill Atrophy Detector · 🟢 · M
Tracks your pre-AI vs. post-AI quality curves on specific skills; flags fading ones.
- ✅ Novel primitive
- ⚠️ Needs pre-AI baseline data — tough to retrofit

---

## Challenge 25 · E5 — From Prompt User to System Architect *(AIF)*
> *How might we build AI-native development tools or "agentic playgrounds" that move young women from prompt-engineering to building and directing system architecture?*
> **Panel champions**: Janet, Hester, Gabrielle · **Secondary**: Sandy

### E5.1 — Agentic Playground · 🟡 · M  ⭐
Template-based agent composer with natural-language config; deploy-to-URL. *(Combo-review #1.)*
- ✅ Four AIF-panel champions
- ✅ Real engineering — scores Tech 5/5
- ⚠️ Incumbents (Replit Agent, Lovable, Gumloop) — audience + pedagogy are your edge
- ⚠️ Tight-anchor discipline or it sprawls

### E5.2 — Remix-Any-Agent · 🟢 · M
Every public agent is view-source / fork like CodePen; edit prompts + tools live.
- ✅ Builds culture of sharing and learning by example
- ⚠️ Originality collapses if Replit or Lovable ships it

### E5.3 — Explain-This-Prompt Agent · 🟢 · H
Paste any power-user prompt; AI explains design choices so you learn the craft.
- ✅ Tiny to build; teaches meta-skill directly
- ⚠️ Depends on good examples; curate a library

### E5.4 — "Show Me the Plumbing" Mode · 🟢 · M
Every AI tool toggles a mode revealing full prompt chain + retrieval + tool-call graph.
- ✅ Teaches architecture by exposure
- ⚠️ Needs host-tool adoption to show real value

### E5.5 — Agent-Building Bootcamp (Girls-Only) · 🟡 · H
6-week async program with cohort of teenage girls; outputs 3 deployed agents.
- ✅ Real-world shipping artifact
- ⚠️ Program > product; hackathon demo shows curriculum, not software

### E5.6 — Architecture Review for Agents · 🟢 · M
Submit your agent; get a principled review from an AI "staff engineer."
- ✅ Lifts builder → architect
- ⚠️ Review quality is the product; prompt-engineering-heavy

### E5.7 — Non-Code Agent IDE · 🟡 · L
Full visual IDE for agents — triggers, memory, tools, schedules — no code.
- ✅ Ambitious; AIF-aligned
- ⚠️ Incumbents already own this layer; weekend can't differentiate

---

# Part 4 — Decision prompts

Use these when you're narrowing:

1. **Do you want Janet and Hester as advocates?** → Pick from A5, B5, C4, D6, E5 (AIF-tagged).
2. **Do you want Wanting as an advocate?** → Pick a health idea with a real pipeline (D1.3, D2.2, D3.3, D5.1) or eldercare (A4.1).
3. **Do you want Sandy as an advocate?** → Pick from A1, A2, E2, E4.
4. **Are you SEA-marketable?** → Lean into A4 (ageing), D1/D3 (hawker), E3 (physical), C4 (students); avoid globally generic C1–C3.
5. **Is the team engineering-heavy?** → Second Shift, Capability Card, Receipts, Life Compass reward you.
6. **Is the team design-heavy?** → Anti-Deepfake Family Word, Agentic Playground, Fair Share for Students let design drive.

---

# Recommended reading order

1. `challenge-statements.md` — the 25 challenges + the panel section
2. `combo-review.md` — the 5 pre-analyzed combos (scored 33–39)
3. `ideas.md` — 6 fresh combos with deep competitor analysis
4. **This doc** — breadth across all 25 challenges, ranked per-challenge
5. `coordination-OS/` — current build plan for reference

If you want the fastest route to a decision: **start with Part 1 of this doc + the Tier-1 table, then read the top idea in each challenge you're drawn to.**
