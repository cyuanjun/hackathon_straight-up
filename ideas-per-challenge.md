# Ideas Per Challenge — Wavesparks Brainstorm

*Generated 2026-04-19. Companion to `ideas.md` and `combo-review.md`.*

**Scope**: 5–7 ideas per challenge statement, ~150 ideas total. Each idea has a one-line description, a competition flag, and a feasibility note for a hackathon weekend. Bottom of the doc ranks the best cross-challenge picks.

---

## How to read this doc

**Competition flag** — how crowded the space is today:
- 🟢 **White space** — few or no direct competitors shipping this
- 🟡 **Moderate** — adjacent tools exist, clear wedge open
- 🔴 **Crowded** — strong incumbents own this space; need a sharp edge

**Feasibility (hackathon)** — can a small team demo this in a weekend:
- **H** (High) — demo-able with mocked data + 1–2 API integrations
- **M** (Medium) — requires multiple integrations or novel pipeline
- **L** (Low) — infra-heavy, data-heavy, or hard-to-reach user

---

# Theme A — Structural Shifts (Macro)

## A1. Ambient AI agents and trust
*How might we build trust, permissions, and fail-safes into ambient personal AI agents before they become default interfaces to daily life?*

1. **Receipts** — Consumer activity feed across all your AI agents (inbox, calendar, shopping). One tamper-evident timeline; one-tap revert. 🟡 · H
2. **Agent Firewall** — Browser extension that intercepts any agent's outbound action and shows "why" before it fires. Policy editor in plain English. 🟢 · M
3. **Guardian Mode for Teens** — Parental-dashboard view of a teenager's AI agent usage: what they asked, what agents did for them, spending. 🟢 · H
4. **Agent Escrow** — For financial actions, agent proposes, a second agent verifies against a rule set, third-party "notary" signs. Release on double-approval. 🟢 · L
5. **Trust Budgets** — Give your agent a daily "trust budget" (spend, messages sent, files modified). Exceed it → human in the loop. 🟡 · M
6. **Kill Switch Network** — One tap revokes every agent's credentials across every connected service. A global log-out-from-AI button. 🟢 · M
7. **AI Action Insurance** — Micro-insurance on agent actions (wrong flight booking, mistaken send). Wraps the action with underwriting. 🟢 · L

## A2. Fragile authenticity in a synthetic world
*How might we design lightweight authenticity and provenance systems that help people verify what is real, human, and trustworthy in everyday interactions?*

1. **Human Stamp for Messaging** — A lightweight browser extension that signs outgoing emails/DMs with a human-presence proof (keystroke cadence + biometric challenge). 🟢 · M
2. **Live Interview Integrity** — C2PA-style signing for Zoom/Meet recordings; receiver can verify "this video is unedited, this person was live." 🟡 · M
3. **Real Review Badge** — Amazon/Google-style review platform plugin that verifies the reviewer is a human who actually used the product (purchase receipt + liveness check). 🟡 · M
4. **Anti-Deepfake Family Word** — Consumer app that generates per-contact "safe words" shown in a trusted UI before any voice/video call; blocks impersonation scams. 🟢 · H
5. **Content Provenance Inbox** — Email client that surfaces C2PA manifests from attachments and flags synthesized content by default. 🟡 · M
6. **Hiring Authenticity Layer** — Plugin for ATS systems that verifies candidates' work samples and identity across the pipeline without intrusive surveillance. 🟡 · L
7. **Real-Friend Directory** — A social graph where every edge is a signed, in-person meet-up (NFC handshake). Inverts the default of "prove you're human" to "prove we've met." 🟢 · H

## A3. Unequal outcomes from AI personalisation
*How might we ensure AI personalisation improves outcomes for underserved users, not just efficiency for those already advantaged?*

1. **Equal AI Tutor** — SMS/low-bandwidth tutor pinned to the student's national syllabus, Socratic-by-default so bad prompting doesn't produce bad outcomes. 🟡 · M
2. **Prompt Translator** — Before hitting an LLM, a layer that rewrites a user's raw question into the kind of prompt a power user would have written. Open-source and free. 🟢 · H
3. **Benefit Finder Agent** — Knows every SEA welfare/subsidy/scholarship scheme; asks 10 questions, tells users exactly what they qualify for and how to apply. 🟡 · H
4. **Bank-Teller AI** — Voice-first financial literacy agent in Bahasa/Tamil/dialect; explains a loan, a term, a contract to anyone, no jargon. 🟢 · M
5. **Public-Clinic Nurse Agent** — AI that helps lower-income patients prepare for a 5-minute public-clinic slot: translates symptoms, writes the best question to ask. 🟢 · M
6. **Second-Chance Coach** — AI career coach for people *without* a network — ex-offenders, stay-at-home returners, career-switchers. 🟢 · M
7. **Legal Aid Co-pilot** — Walks a tenant/worker through filing a complaint or responding to a notice, in plain language with template letters. 🟡 · M

## A4. Ageing, isolation, and independent living
*How might we support safe, dignified independent living for ageing populations without making care feel invasive or dehumanising?*

1. **Second Shift** — Co-pilot for adult children of aging parents; extracts events from daily parent check-ins, redistributes load across siblings. 🟡 · H
2. **Phone-Native Companion** — Works over a regular phone call (no app, no device); calls the senior daily, summarizes to family. 🟡 · H
3. **Passive-Sound Home Monitor** — Uses existing smart-speaker microphone to detect falls, prolonged silence, confusion signs — zero wearables. 🟢 · L
4. **Medication Story** — Instead of pill reminders, a narrative agent that weaves meds into daily ritual ("after your morning kopi, take the white one"). 🟢 · M
5. **Dignity-First Care Logging** — Carers log mood/meals in natural language; AI summarizes for doctors. Removes the "stigma of being tracked." 🟢 · M
6. **Grandparent-to-Grandchild Audio Letters** — AI-mediated voice notes with prompts; builds a legacy archive while reducing isolation. 🟢 · H
7. **Hawker-Center Buddy** — Books group meals for lonely elderly in the same neighborhood, based on shared dietary needs/dialects. 🟢 · M

## A5. AI Adoption Gap Becomes Power Gap *(Powered by AIF)*
*How might we design AI learning environments that increase experimentation confidence among teenage girls before self-selection away from tech begins?*

1. **Agentic Playground for Teen Girls** — Build-a-bot playground with templates from their own life (covered in combo-review #1). 🟡 · M
2. **Claude-Club-in-a-Box** — Teacher-ready curriculum + sandbox for all-girls secondary schools; everything a STEM teacher needs for a 6-week AI unit. 🟢 · H
3. **AI Pen Pal** — Two teen girls in different countries co-build an agent that translates + moderates their chat; learning by doing. 🟢 · M
4. **Fandom Agents** — Agent-builder positioned around K-pop/Taylor Swift/BookTok fandom mechanics (spoiler blockers, lyric bots). Meets the user where she is. 🟢 · H
5. **Mom-Daughter AI Nights** — Kit + guided flow for a mother and teenage daughter to build an agent together. Reverses the "dad teaches son to code" cultural default. 🟢 · H
6. **AI Confidence Coach** — Tracks a girl's prompt-to-agent-build ratio over time; celebrates wins; peer-shares low-stakes experiments. 🟡 · M
7. **Anti-Imposter Agent Gallery** — A public gallery of messy, in-progress girl-built agents (not polished portfolios) — normalizing "my thing doesn't work yet." 🟢 · H

---

# Theme B — Work, Income & Capability

## B1. Slow conversion from skills to income
*How might we help people convert newly learned skills into real income within weeks instead of years?*

1. **First-Gig Engine** — Takes a student's course completion → generates 5 plausible paid projects, pitches them into real local businesses via AI outreach. 🟡 · M
2. **Course-to-Case-Study** — Every course completion ships a deployable mini-product the learner can sell; not a cert, a thing. 🟡 · M
3. **Micro-Agency in a Box** — New grad fronts an AI-run agency (design/writing/ops); the AI does the work, grad learns by owning client relationship. 🟡 · H
4. **Pay-on-Proof Learning** — Learn free, pay a small fee only when your first paid gig comes in. AI matches and tracks. 🟢 · L
5. **Local Client Scouting Bot** — Scans local Facebook groups, Telegram channels, Reddit for "any freelancer who can X" → routes to newly skilled learners. 🟡 · M
6. **Practice Client Agent** — Simulated "client" the learner works with for 2 weeks; real-feeling brief, feedback, change requests; output becomes portfolio piece. 🟢 · H
7. **Skill Stack Mapper** — "Your React + Figma + Mandarin gets you these 8 specific Taobao dropshipper gigs"; cross-lists skills into niche markets. 🟢 · M

## B2. Lack of low-friction entry points to earning
*How might we create legitimate, low-friction ways for people to start earning without relying on resumes, formal credentials, or prior job history?*

1. **Task-Bite Marketplace** — Real businesses post 30-min AI-assisted tasks; any student can attempt; AI grades + clients pay per quality bucket. 🟡 · M
2. **Karaoke Resume** — Replace a resume with a 90-second video + live skills challenge; AI assembles a "capability card." 🟡 · H
3. **Local Errand+Brain Mix** — Platform where students do physical errands *plus* micro-knowledge-work for the same client (e.g. deliver groceries + digitize a menu). 🟢 · M
4. **Intern for a Day** — Companies list a 1-day paid shadowing slot; students apply by answering one AI-screened question. 🟡 · H
5. **Tip-Jar Learning** — Learn by answering questions in niche Discord/Telegram communities; community tips = income; AI vouches for answers. 🟢 · M
6. **First-Paycheck Guarantee** — App pays you $20 for your first attempt at a real paid task; recoups from the client on completion. 🟢 · L
7. **Paid Open-Source Onboarding** — AI scouts beginner-friendly bounties across OSS projects; guides student through the first PR. 🟡 · M

## B3. Weak connection between learning and real work
*How might we connect learning directly to projects, clients, and measurable outputs so capability is built through real work?*

1. **Real-Brief Every Lecture** — Every university lecture auto-generates a live mini-brief from a real local company; students compete; winner gets paid. 🟢 · M
2. **Professor-as-PM** — AI turns course syllabi into project sprints with real-world stakeholders (NGOs, startups) as clients. 🟡 · L
3. **Receipt for Learning** — Every hour of learning emits a verifiable artifact (code, doc, Loom); portfolio auto-accretes. 🟡 · H
4. **Graded-by-Client** — After each project, the actual client grades the work; replaces GPA with client-NPS-over-time. 🟢 · M
5. **Course Dropout Rescue** — When a user abandons a course, AI generates one real-world application of what they already learned so they ship something. 🟢 · H
6. **Syllabus Mirror** — Mirror of the user's syllabus that shows "here's how a working pro does this each week in the wild." 🟡 · H
7. **Retrospective Portfolio** — Looks through your phone/laptop history, auto-drafts a portfolio of what you *actually* did last year. 🟢 · M

## B4. Entry-level work is being compressed by AI
*How might we create new AI-leveraged pathways for early-career workers to build proof of ability and income in a labor market with fewer traditional entry roles?*

1. **Agent-Handler Role** — Train early-career workers to be "shepherds" of 3–5 AI agents each; charge employers per agent supervised. 🟡 · M
2. **AI Apprentice Pipeline** — Company hires a junior + their AI agent as a pair; junior learns by directing the agent, AI learns the company. 🟡 · L
3. **Quality Council** — Platform for early-career workers to be the human-in-the-loop reviewers for AI output at scale, paid per review. 🟡 · H
4. **Reverse-Internship** — Students teach companies *how to use AI* while the company teaches them the business. Paid reverse mentoring. 🟢 · H
5. **Synthetic-to-Real Gradient** — Learner completes AI-generated "fake" client briefs; top performers get real paid work (this is Career Launchpad). 🟡 · M
6. **Model Auditor Certification** — Short training + first gigs as model-bias / red-team auditors for local companies adopting AI. 🟢 · M
7. **Ops-for-Solopreneurs Agency** — Early-career workers as ops-managers for one-person AI-native businesses (newsletter creators, indie SaaS). 🟡 · H

## B5. Opportunity access is socially gated *(Powered by AIF)*
*How might we redesign opportunity discovery so access is driven less by social capital and pedigree, and more by demonstrated potential and readiness?*

1. **Capability Card** — Signed, replayable proof-of-work card (multi-agent graded) as the atomic unit of opportunity. 🟡 · H
2. **Blind Opportunity Matcher** — Employers post requirements; candidates submit only their signed work artifacts; name/school revealed only post-shortlist. 🟡 · M
3. **Network Simulator** — AI assembles a "warm intro path" to any person from your existing graph — turns who-you-know into an open API. 🟢 · M
4. **Mentor Hours Market** — Mentors get tokens for every hour given; candidates earn tokens by completing open challenges. Democratizes access to face time. 🟢 · M
5. **Hidden-Role Radar** — Scrapes all the unposted jobs mentioned in founder tweets, Discord, LinkedIn posts; routes to candidates who match signal. 🟡 · L
6. **Anti-Bro Pipeline** — Companies opt-in to sourcing from communities they'd never reach (polytechnic students, returners, rural universities); AI surfaces top signal. 🟢 · M
7. **Portfolio-over-Pedigree Leaderboard** — Public leaderboard per skill, ranked by signed capability cards. Anyone can rise. 🟡 · H

---

# Theme C — Attention, Agency & Coordination

## C1. Priority collapse in high-noise environments
*How might we help people identify and act on their highest-priority work in environments where everything competes for attention?*

1. **Top 3 Cards** — A single screen with the three things that matter right now, recomputed every 30 minutes with plain-English reasoning. 🔴 · H
2. **Calendar Ghostwriter** — Looks at every meeting on your week and tells you which ones to skip, with a draft "can't make it" reply. 🔴 · H
3. **Deep Work Lock** — Detects when you're in flow and auto-silences all surfaces; escalates only what matches a prior rule. 🔴 · M
4. **Priority Sniff Test** — Forwarding address: paste anything in, get a one-sentence "this is urgent / important / noise" judgement. 🟡 · H
5. **One-Tap Triage** — Inbox card with three buttons (deal now / schedule / ignore); weekly replay of your own triage builds a personal model. 🔴 · H
6. **Priority Peer Review** — Pairs two friends; each sees the other's "top 3" and can challenge, "why is this on your list?" 🟢 · H
7. **Spotlight Mode** — Deadline-aware mode that rewrites your day hour-by-hour based on what's actually due. 🔴 · M

## C2. Decision fatigue from overlapping responsibilities
*How might we reduce cognitive overload for people juggling multiple responsibilities, deadlines, and roles at the same time?*

1. **Role Switcher** — Explicit UI for "I am now in Student mode / Daughter mode / Intern mode"; surfaces only that role's surface. 🟡 · M
2. **Decision Log** — Captures every micro-decision you make in a day; pattern-matches to suggest auto-decisions next time. 🟢 · M
3. **Default-Choice Engine** — Rather than ask what you want, proposes a default and lets you veto; most days you won't veto. 🟡 · H
4. **Worry Parking** — Voice-dump worries; AI categorizes ("controllable now / controllable later / not yours"); schedules the controllable ones. 🟡 · H
5. **One-Question Morning** — Every day, the one question you actually need to answer today. No lists, no notifications. 🟡 · H
6. **Responsibility Map** — Visualizes all your open responsibilities as a graph; shows which ones are blocking the most others. 🟡 · M
7. **Say-No Assistant** — Drafts a polite, in-your-voice decline to any new request that doesn't fit your current 3 priorities. 🟡 · H

## C3. Fragmented communication across platforms
*How might we unify fragmented communication into clear, actionable next steps without requiring users to constantly monitor every platform?*

1. **Unified Thread View** — Sees the same conversation across Slack + email + WhatsApp and shows it as one thread. 🔴 · M
2. **Cross-Platform Action Inbox** — Pulls every "you-ought-to-reply" message into one queue with one-click draft-and-send back to source. 🔴 · M
3. **Channel Consolidator** — Proposes a weekly "these three Slacks could be one Slack" based on who-talks-to-whom. 🟢 · M
4. **Follow-up Scoreboard** — Shows every person waiting on you across all platforms; shows every person you're waiting on. 🟡 · M
5. **Voice-First Inbox** — Read me my messages during my commute; I reply with voice; AI formats per platform. 🟡 · H
6. **Deadline Harvester** — Scans all your messages for implicit deadlines ("by Friday") and turns them into calendar holds. 🟡 · H
7. **Conversation Resurrection** — Finds threads you abandoned 3+ weeks ago and asks if you want to close them out. 🟢 · H

## C4. Invisible cognitive labor *(Powered by AIF)*
*How might we reduce invisible coordination labor, stop it from defaulting to women disproportionately, and overall preserving the human quality of relationships and collaboration?*

1. **Coordination Labor Dashboard** — Measures "how many reminders you sent / how many nudges you absorbed" per week (this is Coordination OS). 🟡 · M
2. **Fair Share for Students** — WhatsApp bot for student flats that infers who's doing what from group chat, surfaces imbalance. 🟡 · H
3. **Event Ops Agent** — For group events, takes over the "who's bringing what, who's been reminded, who hasn't RSVP'd." 🟡 · H
4. **Family Birthday Butler** — Plans every family birthday for you (gift shortlist, card draft, venue options); redistributes the "remembering" burden. 🟢 · H
5. **Group Chat Ghostwriter** — Drafts the "hey team, just checking in" messages that one person always ends up sending. 🟡 · H
6. **Mental Load Diff** — Compare your invisible-labor receipts with a partner/roommate/sibling; visualizes the gap, not the blame. 🟡 · M
7. **Auto-RSVP Agent** — Replies on your behalf to every "who's free on X?" message based on your calendar and stated preferences. 🟡 · H

---

# Theme D — Health, Longevity & Sustainability

## D1. Preventive health feels inaccessible
*How might we make preventive health and longevity actionable, affordable, and embedded into everyday routines?*

1. **Hawker Longevity** — SEA-contextualized health coach built around hawker food + public-transit movement (covered in combo-review #5). 🟡 · M
2. **$5 Longevity Stack** — A concierge for the cheapest evidence-grade interventions (walking, sleep, cheap protein); dismisses supplement noise. 🟢 · H
3. **Boring Health OS** — Anti-Bryan-Johnson. Shows only the 5 things that actually move the needle, hides the 500 that don't. 🟢 · H
4. **Morning 3-Minute Check** — Daily 3-minute scan (sleep + mood + symptom), builds a year-long trendline, flags drift. 🟡 · H
5. **Clinic-Ready Briefings** — Before a check-up, AI assembles a 1-page "here's what I've noticed in the last 6 months" for the doctor. 🟢 · H
6. **Neighbourhood Walking Challenge** — Social layer where your HDB block competes on daily steps; AI creates routes around local MRT. 🟡 · H
7. **Habit Cost Calculator** — "Your 5 bubble teas/week = 1.8 kg of fat per year" → emotional math, not finger-wagging. 🟡 · H

## D2. Unsafe experimentation in health optimisation
*How might we support safe, evidence-aware health experimentation without pushing users into misinformation or over-optimisation?*

1. **Supplement Interaction Agent** — Log what you take, AI flags stack interactions, cites evidence strength. 🟡 · M
2. **Claim Lookup** — Paste any health claim (from TikTok/IG); get a 3-sentence verdict with citation quality. 🟡 · H
3. **Self-Experiment Log** — N=1 trial framework: define hypothesis, baseline, variable, duration; AI keeps you honest. 🟢 · M
4. **Red-Flag Radar** — Watches your purchase history + search + social; flags the moment you're going down a dangerous rabbit hole. 🟢 · M
5. **Evidence-Grade Chat** — ChatGPT-for-biohacking that *always* shows the evidence level (meta-analysis vs. tweet). 🟡 · H
6. **Doctor-in-the-Loop** — Subscribe to a real doctor who reviews your self-experiments once a month for $20. 🟡 · L
7. **Rollback Protocol** — One-tap "revert all my health experiments back to baseline"; generates tapering/weaning plan. 🟢 · M

## D3. Poor fit of Western health defaults in Asian contexts
*How might we build health and longevity systems that are adapted to Asian genetics, diets, climates, and work cultures?*

1. **Asian-Context Nutrition Coach** — Every recommendation is in rice/noodle/hawker terms, not quinoa. 🟢 · H
2. **ALDH2 Alcohol Warning** — Cheap genetic test + lifetime flushing-risk tracker; culturally tuned intervention messages. 🟢 · M
3. **Monsoon Exercise Planner** — Schedules outdoor movement around humidity/haze/PSI; swaps indoor alternatives dynamically. 🟢 · H
4. **Rice-Glycemic Optimizer** — Real-time glycemic-response predictor based on the specific rice + sides + order of eating. 🟢 · M
5. **Shift-Worker Sleep Coach** — For hawker aunties, nurses, security; circadian guidance for non-9-to-5 Asian work. 🟡 · M
6. **Chinese Medicine Translator** — Maps TCM diagnoses to Western-medicine equivalents; helps cross-generational families communicate. 🟢 · M
7. **Chopsticks Portion Control** — Computer vision on your own phone photo of a hawker tray → shows portion vs. your target. 🟡 · H

## D4. Hidden burnout among caregivers
*How might we better support caregivers' energy, resilience, and mental health before burnout becomes chronic?*

1. **Second Shift** — Adult-child caregiver co-pilot with sibling load redistribution (covered in ideas.md). 🟡 · H
2. **Respite Agent** — Books 2-hour respite windows; arranges backup care; handles the "guilt script" for the caregiver. 🟢 · M
3. **Burnout Early Warning** — Passively watches caregiver's phone usage patterns, texts tone; flags drift toward burnout. 🟢 · M
4. **Caregiver Peer Circles** — AI-matched 5-person groups of caregivers in similar situations; async support threads with AI summaries. 🟡 · H
5. **Admin Inbox Absorber** — Takes over the admin (claims, appointments, insurance) side of caregiving. 🟡 · M
6. **One Sentence a Day** — Caregiver voices one sentence about their day; AI builds a resilience journal they can re-read. 🟢 · H
7. **Inherited-Task Handoff Tool** — When siblings rotate caregiving duty, generates the "here's everything you need to know" brief. 🟢 · H

## D5. Health literacy starts too late
*How might we help young people make informed long-term health decisions earlier, using empowering rather than fear-based systems?*

1. **Future-Me Simulator** — Shows your future self at 40 based on current sleep/food/exercise patterns; updates weekly. 🟡 · M
2. **TikTok Nutrition Translator** — Plugin that overlays evidence-grading on health TikToks as teens scroll. 🟢 · M
3. **Teen-Safe Body Literacy Chat** — Answers the awkward questions (sleep, reproductive, skin, mental health) young people won't ask adults. 🟡 · H
4. **School Canteen Hero** — Shows which canteen items move which longevity metrics, in teenager-relevant language. 🟢 · H
5. **Compound Health Bank** — "Interest" metaphor: show how today's choices compound 20 years out; gamified. 🟡 · H
6. **Parent-Teen Health Compact** — Both parent and teen sign up; AI brokers shared goals without surveillance. 🟢 · M
7. **Peer-Audit Health Buddy** — Pairs two teens; they grade each other's habits weekly; AI moderates. 🟢 · H

## D6. Fertility window vs career acceleration *(Powered by AIF)*
*How might we build decision-support tools that give young women realistic, empowering data about long-term life planning — without fear-based narratives?*

1. **Life Compass** — Scenario simulator across 5 life paths with real-cohort probability bands (covered in ideas.md). 🟢 · M
2. **The Numbers, Honestly** — A data dashboard stripped of marketing: real AMH curves, real IVF success rates, real egg-freezing outcomes by age. 🟢 · H
3. **Couple Alignment Tool** — A he-and-she joint simulator; surfaces misaligned expectations before they blow up. 🟢 · M
4. **Career Pause Calculator** — Models the career impact of taking 6/12/24 months off — by industry, by seniority, by SEA country. 🟢 · H
5. **Fertility-Aware Career Coach** — Career advice that factors in fertility goals without making it the centerpiece. 🟢 · M
6. **Policy Finder for Families** — Every maternity/paternity/elder-care benefit available in SG/MY, given your employer; applies for you. 🟡 · H
7. **Real Stories Library** — Curated, searchable library of actual women's paths; AI matches your profile to closest real paths. 🟡 · H

---

# Theme E — Emerging AI Opportunity Space

## E1. AI-native infrastructure for agent systems
*How might we build infrastructure designed for AI-to-AI interaction, rather than retrofitting human-centered software for agent workflows?*

1. **MCP Discovery Registry** — Yellow pages for MCP servers: searchable, ranked, reviewed by other agents. 🟢 · M
2. **Agent-Native Auth** — OAuth replacement designed for agent principals, not human principals: scoped, revocable, delegable. 🟢 · L
3. **Agent Rate-Limit Negotiator** — Middleware where two agents negotiate API access windows instead of hammering endpoints. 🟢 · M
4. **Shared Memory Bus** — Cross-agent memory layer — agents on the same user's behalf can read each other's context. 🟢 · M
5. **Agent Conflict Mediator** — When two agents act on the same user try to do opposing things, a third agent arbitrates via rules + LLM. 🟢 · L
6. **Eval-as-a-Service for Agents** — Real-time evaluation middleware that grades every agent response before it reaches the user. 🟡 · M
7. **Semantic Webhooks** — Webhook payloads in natural language + structure; any agent on either side can comprehend. 🟢 · M

## E2. Governance, permissions, and auditability for autonomous systems
*How might we design agent systems with safety, permissions, and auditability built in by default rather than added later?*

1. **Agent Policy DSL** — Natural-language policy editor: "My shopping agent can spend $50/day, never on subscriptions." 🟡 · M
2. **Replay Debugger for Agents** — Step-through debugger for what an agent did and why, usable by non-developers. 🟢 · M
3. **Consent Ledger** — Every time an agent accesses a new data source, it asks; log is tamper-evident. 🟡 · M
4. **Cross-Org Agent Access Review** — For teams, shows every agent running + who gave it access + last time it acted. 🟡 · L
5. **Simulated Harm Testing** — Before prod, spins up a sandbox and provokes your agent with 100 edge cases. 🟢 · M
6. **Agent Fire Drill** — Monthly scheduled incident: agent pretends to misbehave; team's kill-switch drill scored. 🟢 · H
7. **Time-Boxed Superpowers** — Agents can request elevated access for 30 minutes with reason; auto-expires. 🟢 · M

## E3. AI applied to physical systems, not just software
*How might we apply AI directly to physical-world systems where coordination, efficiency, and safety improvements have real economic impact?*

1. **Hawker Inventory Agent** — Predicts tomorrow's ingredient needs for a hawker stall from weather + event calendar + sales. 🟢 · M
2. **Construction Site Schedule Resolver** — AI that watches construction CCTV, re-optimizes crew schedules when one trade is blocking another. 🟢 · L
3. **Port Waiting Time Predictor** — Open API for SEA port congestion; truckers save hours. 🟡 · L
4. **HDB Lift Queue Agent** — Predicts lift wait times across HDB blocks at peak hours; nudges residents to stagger. 🟢 · M
5. **Small-Fleet Route Optimizer** — Delivers dispatch for the 5-person logistics SME that can't afford enterprise TMS. 🟡 · M
6. **Factory Floor Anomaly Voicebot** — Operator voices "machine 4 is making a weird noise" → AI logs, matches to past tickets, escalates. 🟢 · M
7. **Solar-Panel Yield Agent** — Residential solar owners get daily "your system underperformed by X% because Y" alerts. 🟡 · M

## E4. Preserving human agency in AI-mediated environments
*How might we design human-facing AI systems that increase human capability, judgment, and agency instead of making people more passive or dependent?*

1. **Socratic-Only Mode** — Any LLM app toggled into a mode that *only* asks questions back, never answers. 🟢 · H
2. **Stretch Zone Assistant** — For learners, refuses to answer questions you're almost-able-to-answer yourself; nudges you to try first. 🟢 · H
3. **AI Training Wheels Off** — Weekly challenges to do your normal tasks *without* AI; scores you on re-acquired skills. 🟢 · H
4. **Dependency Meter** — Tracks what % of your outputs are AI-authored vs. human-authored; alerts on drift. 🟢 · M
5. **Skill Atrophy Detector** — Watches your pre-AI vs. post-AI quality curves on specific skills; flags which ones are fading. 🟢 · M
6. **Decision Receipts** — For every AI-assisted decision, saves a 1-line "why you chose this" you have to author yourself. 🟢 · H
7. **Dual-Author Drafting** — Forces alternation — AI drafts odd paragraphs, you draft evens; no full-delegation possible. 🟢 · H

## E5. From Prompt User to System Architect *(Powered by AIF)*
*How might we build AI-native development tools or "agentic playgrounds" that move young women from prompt-engineering to building and directing system architecture?*

1. **Agentic Playground** — Template-based agent composer with natural-language configuration (covered in combo-review #1). 🟡 · M
2. **"Show Me the Plumbing" Mode** — Every AI tool has a toggle that reveals the full prompt chain / retrieval / tool-call graph. 🟢 · M
3. **Remix-Any-Agent** — Any public agent can be "view-source / fork" like CodePen; you edit its prompts/tools live. 🟢 · M
4. **Agent-Building Bootcamp (Girls-Only)** — 6-week async program with cohort of teenage girls; outputs 3 deployed agents. 🟡 · H
5. **Explain-This-Prompt Agent** — Paste any prompt a power user wrote; AI explains the design choices so you can learn the craft. 🟢 · H
6. **Non-Code Agent IDE** — Full visual IDE for agents: triggers, memory, tools, schedules — no code. 🟡 · L
7. **Architecture Review for Agents** — Submit your agent, get a principled review from an AI "staff engineer." 🟢 · M

---

# General overview & cross-cutting themes

Across ~150 ideas, four primitives repeat with different clothing:

1. **Ledger / receipts / dashboards of invisible work** — whether coordination (C4), agent actions (A1/E2), caregiving (D4), or skill-building (B5). Strongest demo primitive; defensibly under-built.
2. **Scenario simulators** — life paths (D6), health trajectory (D5), career pauses, longevity shifts (D1/D3). Tech-heavy, narrative-friendly, demo-ready.
3. **Cross-generational coordination** — adult children ↔ parents (A4/D4), mom ↔ daughter (A5), teen ↔ parent (D5), sibling load (D4). Culturally specific SEA wedge.
4. **Socratic / agency-preserving AI** — in tutoring (A3), agent building (E5), health literacy (D5), work (E4). Cheap to prototype, hard to market.

Single-idea recurrences across multiple challenges (good signs — indicates a real root cause):
- **Second Shift / eldercare co-pilot** hits A4, D4, C4
- **Capability Card** hits B1, B2, B3, B5
- **Agentic Playground** hits A5, E5, (B5)
- **Socratic Tutor / Equal AI** hits A3, D5, E4

---

# Ranking — top picks by feasibility × market opportunity

Criteria: **Competition** (how much white space), **Feasibility** (hackathon-demoable), **Rubric fit** (what `combo-review.md` weights).

### Tier 1 — strong demo, real whitespace, rubric-aligned

| # | Idea | Challenge(s) | Comp | Feas | Why it's here |
|---|---|---|---|---|---|
| 1 | **Second Shift** — eldercare co-pilot | A4, D4, C4 | 🟡 | H | No competitor targets the adult child; reuses Coordination OS worldview |
| 2 | **Anti-Deepfake Family Word** | A2 | 🟢 | H | Scam-adjacent urgency; genuinely empty category; immediately demo-able |
| 3 | **Receipts / Consumer agent feed** | A1, E2 | 🟡 | H | C2PA momentum + no consumer cross-agent view exists |
| 4 | **Capability Card** | B1–B5 | 🟡 | H | Rides portfolio-over-resume trend; avoids marketplace cold-start |
| 5 | **Life Compass** | D6, D5 | 🟢 | M | AIF-sponsored; challenge statement mandates the exact framing |
| 6 | **Hawker-Centre Buddy** | A4 | 🟢 | M | Community-ops angle; nobody's building this |
| 7 | **Agentic Playground (tight anchor)** | A5, E5 | 🟡 | M | Already the combo-review #1 |
| 8 | **Equal AI SMS Tutor** | A3, D5 | 🟡 | M | Equity wedge + real tech; lower demo-flair is the risk |

### Tier 2 — solid ideas, moderate demo complexity, edge exists

| # | Idea | Challenge(s) | Comp | Feas |
|---|---|---|---|---|
| 9 | Coordination Labor Dashboard (existing Coordination OS) | C1–C4 | 🔴 | M |
| 10 | Fair Share for Students | C4 | 🟡 | H |
| 11 | Supplement Interaction Agent | D2 | 🟡 | M |
| 12 | Hawker Longevity | D1, D3, D5 | 🟡 | M |
| 13 | The Numbers, Honestly (fertility dashboard) | D6 | 🟢 | H |
| 14 | Course Dropout Rescue | B3 | 🟢 | H |
| 15 | Reverse-Internship | B4 | 🟢 | H |
| 16 | Grandparent-to-Grandchild Audio Letters | A4 | 🟢 | H |
| 17 | Role Switcher | C2 | 🟡 | M |
| 18 | Policy Finder for Families | D6 | 🟡 | H |
| 19 | Phone-Native Companion | A4 | 🟡 | H |
| 20 | Remix-Any-Agent | E5 | 🟢 | M |

### Tier 3 — interesting but hackathon-dangerous

Infrastructure plays that are hard to demo (**Agent Firewall**, **Agent-Native Auth**, **MCP Registry**), data-heavy plays (**Cohort-data fertility tool**), adoption-heavy plays (**Professor-as-PM**), liability-heavy plays (**Doctor-in-the-loop**, **Medication Story**).

### Tier 4 — crowded spaces, don't enter without a sharp edge

Everything under C1 and C3 (inbox zero, unified inbox) is **🔴 crowded**. Standard productivity tooling (Motion, Superhuman, Shortwave, Notion AI, Gemini in Gmail) dominates. Enter only if the wedge is invisible-labor measurement or a non-executive price point.

---

# If you had to pick today

If you want the **safest score under the rubric** while differentiating from the team's existing work:
→ **Second Shift** (ideas.md #1) or **Capability Card** (ideas.md #5).

If you want the **highest potential ceiling** with strong rubric alignment:
→ **Life Compass** or the **Agentic Playground tight-anchor**.

If you want to **stay with Coordination OS** but reframe toward the untapped white space:
→ Pivot it to the **Fair Share for Students** wedge; same tech, different user, way less competition than the professional inbox category.
