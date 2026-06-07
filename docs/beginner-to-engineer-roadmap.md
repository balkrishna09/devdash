# From Zero → Engineer: A Self-Paced Learning Plan

A complete, hands-on path from "I'm new to coding and IT" to junior-level **full-stack → data engineer** (with an applied AI/ML finish). Built to be done on your own, slowly, over months.

---

## How this plan actually works

Three ideas hold the whole thing together. Read these once before anything else.

**1. You don't need a bootcamp — you need the *right* free courses + a tutor + accountability.**
The best beginner material in the world is already free and battle-tested. This plan *anchors* on those courses (CS50, Full Stack Open, the Data Engineering Zoomcamp). I (Claude) am not trying to out-teach Harvard. My job is the layer those courses don't give you: explaining the "why" when you're stuck, debugging your code with you, connecting concepts to real work, and keeping you on track.

**2. Go slow. Mastery beats speed.**
This is a marathon — realistically **10–14 months part-time** (see timeline). You will *not* cram. The rule is: small chunks, every week, with your hands on a keyboard. If a week needs to be two weeks, take two weeks. Skipping fundamentals to feel fast is the #1 way self-taught people get stuck later.

**3. Learn by building, in public.**
Every phase ends in a real project that goes on your GitHub. By the end you have a portfolio, not just certificates. You'll also run your *own* tickets (more on that below) — which is how you learn agile and Jira-style tracking by *doing* it, not reading about it.

> **The weekly loop (use this every single study session):**
> **(a) Learn** — watch/read the anchor course module. → **(b) Build** — do the exercise / build the thing yourself. → **(c) Ask** — bring what confused you, or your broken code, to a Claude chat and ask *"why"* until it clicks. → **(d) Log** — move your ticket to Done and write one line about what you learned.

---

## The stack I chose for you (and why)

You said "any one stack or multi — depends on you." Here's the call:

- **Python** as your main language. It's the friendliest to learn, and it's the backbone of data engineering, data science, and ML — exactly where you said you're headed.
- **JavaScript + HTML + CSS** for the web/full-stack slice, so the web is never a black box to you. (This is also the most-taught beginner web stack, with the best free material.)
- **SQL** throughout — the single most important language for anyone touching data.
- **Docker, Git, a cloud free-tier, dbt, an orchestrator** — the "how real systems run" tools, introduced when you're ready for them, not before.

This gives a clean story: *learn to program → learn how web software is built → learn to move and transform data (your target role) → apply ML on top.*

---

## Timeline (honest version)

Assuming **~10 hours/week**. Adjust everything if your real number is different — tell Claude your weekly hours and it will re-time the plan.

| Phase | Focus | Rough time @ 10 hrs/wk |
|---|---|---|
| **0** | Setup, terminal, Git, how-to-learn | 1–2 weeks |
| **1** | Programming + CS foundations | 8–12 weeks |
| **2** | Full-stack web fundamentals | 10–14 weeks |
| **3** | Data engineering (your target) | 10–14 weeks |
| **4** | Applied ML / AI | 6–10 weeks |
| | **Total** | **~10–14 months** |

More hours/week → faster. Fewer → slower. Both are fine. The plan doesn't expire.

---

## Did we cover *everything* you asked about?

You listed a lot. Here's where each topic lives so nothing falls through:

| You asked about… | Covered in |
|---|---|
| How Git versioning works | **Phase 0** (then used every day after) |
| How to develop / dev workflow | **Phase 0–1** |
| Agile / Scrum | Woven throughout; introduced **Phase 0** |
| Jira / ticketing systems | Woven throughout — you'll run your *own* board from **Phase 0** |
| Frontend | **Phase 2** |
| Backend | **Phase 2** (+ data services in Phase 3) |
| Cloud | **Phase 3** (intro), first taste deploying in **Phase 2** |
| CI, staging (stg), prod (prd) environments | **Phase 2** (concept + deploy) → **Phase 3** (real CI/CD, multi-env) |
| Load balancer | **Phase 2–3** (concept + a hands-on nginx reverse-proxy taste) |
| Docker | **Phase 2** (intro) → **Phase 3** (mastery) |
| RPS (requests/sec, throughput, scaling) | **Phase 2–3** (you'll actually measure it with a load-test tool) |
| Full-stack / Data / AI-ML career paths | The whole arc, Phases 1→4 |

---

## Your "map" reference: roadmap.sh

Before or during any phase, open the matching visual roadmap on **https://roadmap.sh** to see the whole landscape and where you are. The ones you'll use most:

- **Git and GitHub – Beginner** → https://roadmap.sh/git-github
- **Computer Science** → https://roadmap.sh/computer-science
- **Full Stack** → https://roadmap.sh/full-stack
- **Backend – Beginner** → https://roadmap.sh/backend
- **SQL** → https://roadmap.sh/sql · **Docker** → https://roadmap.sh/docker · **DevOps** → https://roadmap.sh/devops
- **Data Engineer** → https://roadmap.sh/data-engineer
- **AI and Data Scientist** → https://roadmap.sh/ai-data-scientist · **AI Engineer** → https://roadmap.sh/ai-engineer

These are maps, not courses — use them to orient, not to study from.

---

# The Phases

## Phase 0 — Setup & how to learn (1–2 weeks)

**Goal:** A working dev environment, Git/GitHub muscle memory, and your own ticket board running. This is the foundation everything sits on.

**What you'll learn / do:**
- Get comfortable with the **terminal / command line** (navigating folders, running commands).
- Install a code editor (**VS Code**), Python, Node.js, and Git.
- Learn **Git versioning** properly: what a commit/branch/merge is, why version control exists, `clone / add / commit / push / pull`, and basic branching. Make a GitHub account and push your first repo.
- Set up your **own ticket board** (this *is* your agile + Jira practice — see "Run your own tickets" below).
- Learn the **3-step loop** above and set your weekly cadence.

**Anchor resources:**
- roadmap.sh "Git and GitHub – Beginner" (link above) as a checklist.
- GitHub's own "Hello World" intro: https://docs.github.com/get-started
- Lean on Claude heavily here — ask it to explain every Git concept with a tiny concrete example, and to walk you through your first commit step by step.

**Phase 0 milestone:** A GitHub repo named `learning-journey` with a README that lists your goals, pushed from your own machine using Git from the terminal. First ticket moved to Done.

---

## Phase 1 — Programming + CS foundations (8–12 weeks)

**Goal:** Think like a programmer. Understand how computers and code actually work — variables, logic, data structures, functions, and a mental model of memory, files, and the web.

**Anchor course: Harvard CS50x (free, 2026 edition).**
- https://cs50.harvard.edu/x/ — free, and the 2026 edition added a section on AI. It teaches problem-solving in C, then Python, then SQL, plus HTML/CSS/JS basics at the end. It's challenging and *worth it* — it builds the foundation most self-taught people skip.
- CS50 has its own free AI helper (cs50.ai). Use it for course-specific help; use Claude for deeper "why does this work" questions and for everything outside CS50.

**Supplement (optional, hands-on Python):** freeCodeCamp's Python / Scientific Computing track (free) → https://www.freecodecamp.org

**What you'll learn:** computational thinking, data types, conditionals, loops, functions, arrays/lists, dictionaries, basic algorithms (search/sort), how memory works, intro to SQL, and your first taste of web languages.

**Phase 1 milestone:** Complete several CS50 problem sets + the CS50 final project (your own small program), pushed to GitHub with a clear README. *(Bonus: a free CS50 certificate if you score 70%+.)*

> ⚠️ Don't rush Phase 1. This is the phase that makes everything after it easier. If CS50's C section feels brutal, that's normal — push through the first few weeks; it clicks.

---

## Phase 2 — Full-stack web fundamentals (10–14 weeks)

**Goal:** Understand and build a complete web application — frontend, backend, database, and deploy it. This is where "frontend vs backend," REST APIs, environments, and Docker stop being words and become things you've done.

**Anchor course: Full Stack Open (University of Helsinki — free, and local to you!).**
- https://fullstackopen.com/en/ — free, world-class, hands-on. It expects basic programming + basic web + Git basics first, which Phases 0–1 give you. Core is Parts 0–7 (web fundamentals, React, Node/Express backend, REST, databases, testing). Later parts add TypeScript, GraphQL, React Native, and CI/CD.
- **Bonus for you specifically:** Finnish residents who complete the courses *with* the project at maximum credits are promised a job interview by partner companies, and free University of Helsinki credits are available. Worth knowing as a target.

**Concepts to deliberately nail this phase (ask Claude to explain each with a diagram):**
- **Frontend vs backend vs database** — who does what.
- **HTTP & REST APIs** — requests, responses, status codes, JSON.
- **Environments: dev → staging (stg) → prod (prd)** — why the same app runs in multiple places, and what "deploy" means.
- **Docker (intro)** — what a container is and why "works on my machine" is a problem it solves.
- **Load balancer / RPS (intro)** — what happens when one server isn't enough; what "requests per second" measures. (You'll go deeper in Phase 3.)
- **Git collaboration** — branches, pull requests, code review.

**Phase 2 milestone:** Build and **deploy** a full-stack app (React frontend + Node/Express backend + a database) to a free host. Put it on GitHub with a live link in the README. This is portfolio piece #1.

---

## Phase 3 — Data engineering (your target role) (10–14 weeks)

**Goal:** Build production-style data pipelines. This phase is the center of gravity for your stated goal — and it's where cloud, Docker mastery, orchestration, and real CI/CD come together.

**Anchor course: Data Engineering Zoomcamp by DataTalks.Club (free).**
- https://github.com/DataTalksClub/data-engineering-zoomcamp — a free 9-week course (do it at ~half speed = ~3–4 months part-time). All materials/videos stay free and self-paced anytime.
- It follows a clear build: **infrastructure setup (Docker + Terraform) → workflow orchestration → data warehouse (BigQuery) → analytics engineering (dbt) → batch processing (Spark) → streaming (Kafka) → capstone project.**
- **Cohorts:** the live cohort runs roughly once a year (the most recent started January 2026). Off-cohort you can't submit homework for a certificate, but everything is available to learn from now. If a certificate matters to you, you can plan to join the next live cohort (~early 2027) and use the months before to get ahead.

**Concepts to nail this phase:**
- **SQL, deeper** — joins, aggregations, window functions, query performance.
- **Data modeling & warehousing** — how analytical data is structured.
- **Docker, for real** — multi-container setups (e.g., a database + your app).
- **Cloud** — a free-tier cloud account (GCP in the Zoomcamp; the concepts transfer to AWS/Azure).
- **CI/CD + multi-environment** — automating tests and deploys; promoting code dev → stg → prd safely.
- **Load balancing & throughput (hands-on taste)** — run an **nginx reverse proxy** in front of two app containers with Docker, then use a load-test tool (e.g., `k6` or `hey`) to measure **RPS** and watch the load spread. Ask Claude to set this mini-lab up with you.

**Phase 3 milestone:** An end-to-end data pipeline (ingest → store → transform → a dashboard or query layer), containerized, on GitHub with a clear architecture diagram. Portfolio piece #2 — and the one most relevant to data-engineer roles.

---

## Phase 4 — Applied ML / AI (6–10 weeks)

**Goal:** Touch the "AI/ML" side you mentioned — enough to build one real ML thing and one AI-powered app, and to know where you'd go deeper later.

**Anchor options (free):**
- **Machine Learning Zoomcamp (DataTalks.Club)** → https://github.com/DataTalksClub/machine-learning-zoomcamp — practical ML end-to-end (data → model → deploy).
- roadmap.sh **AI and Data Scientist** / **AI Engineer** roadmaps as your map (links above).

**What you'll do:**
- Data handling with **pandas**, then your first models with **scikit-learn** (regression/classification), and how to evaluate them.
- Build **one ML project** (predict something on a real dataset) and deploy it as a small API.
- Build **one AI-powered app** — e.g., something that calls the Claude API. (Tip: Claude can help you build "AI-powered Artifacts" right here in chat — apps that themselves call an LLM. Great way to learn AI engineering hands-on.)

**Phase 4 milestone:** One ML project + one LLM-powered app on GitHub. Portfolio piece #3.

---

## Run your own tickets (your agile + Jira learning, by doing)

You wanted to learn agile and ticketing. The best way is to *manage your own learning* like a real project:

- **Set up a board.** Use **GitHub Projects** (free, lives next to your code) or **Trello**, or a free **Jira** personal project if you want the exact industry tool. Columns: `Backlog → This Week → In Progress → Done`.
- **Make each module a ticket.** e.g., *"CS50 — Problem Set 2"*, *"Full Stack Open — Part 3."* Give it a short description and a "definition of done."
- **Work in weekly sprints.** Every Monday (or your chosen day), pull a realistic set of tickets into `This Week`. Friday, review what got done and what slipped — that's a sprint retro.
- **You're now doing Scrum/Kanban for real.** When you later read the formal terms (sprint, backlog, standup, velocity, WIP limits), they'll map onto something you've already lived. Ask Claude to explain each agile term against your own board.

---

## How to use Claude as your tutor (the setup)

You asked how to set Claude up so you can follow this over months. Here's the practical workflow:

**1. Create one Claude Project — call it "Tech Learning."**
A Project is a workspace where chats share the same context and files.
- **Add this roadmap file to the Project's knowledge.** Now every chat inside the Project knows your plan.
- Add a `progress.md` you keep updated (current phase, current module, recent wins, current blockers). Update it as you go and Claude always has your latest state.
- Keep all your learning chats *inside* this Project so context carries across sessions.

**2. Use normal chats as your tutor (the daily driver).**
- Bring concepts you don't understand: *"Explain HTTP requests like I'm new, with a diagram."*
- Bring broken code: paste it and the error, ask *"why is this failing and what's the mental model I'm missing?"*
- Always push for the **why**, not just the fix. Ask for analogies, then a tiny example you type yourself.
- Ask for **visuals** — Claude can draw diagrams of how the web works, how Git branches flow, how a pipeline moves data.

**3. Use Artifacts to build and to study.**
- Have Claude build small interactive things: a Git-commands cheat-sheet, a flashcard quiz on SQL, a diagram of dev→stg→prd. These render right in the chat and you can iterate on them.
- Later, build **AI-powered Artifacts** (mini-apps that call an LLM) — your Phase 4 AI practice.

**4. Use Claude Code once you're past the basics (Phase 2 onward).**
- Claude Code is a coding tool that works in your terminal/editor and can write and edit real files with you. It needs Node.js installed (you'll have it from Phase 0). Use it to pair-program on your projects — but in early phases, *type things yourself* so the fundamentals stick. Let Claude Code take more of the wheel only after you understand what it's doing.

**5. Routines (optional, later — paid plans only).**
- Claude has a **Routines** feature (a saved prompt + repo + tools that runs automatically on a schedule), launched in 2026 as a research preview on paid plans (Pro/Max/Team/Enterprise), with small daily run limits. Once you're coding regularly, you *could* set a routine like a weekly "review my practice repo and suggest one thing to improve." Totally optional — the core plan needs nothing more than chat + a Project.

---

## Weekly cadence template (adjust to your life)

A simple rhythm that fits ~10 hrs/week:

- **4 short weekday sessions (~1.5 hrs each):** run the loop — Learn → Build → Ask → Log.
- **1 longer weekend session (~4 hrs):** tackle the bigger exercise/project work for the week.
- **Friday 15 min — sprint review:** what got done, what slipped, update `progress.md`, pull next week's tickets.
- **Once a month — zoom out:** open the matching roadmap.sh map, see how far you've come, adjust the plan with Claude if needed.

Two real sessions a week beats seven imaginary ones. Consistency > intensity.

---

## Your first 7 days (start here)

You can begin right now, today:

1. **Day 1:** Make a GitHub account. Install VS Code, Git, Python, Node.js. (Ask Claude to walk you through each install for your OS, step by step.)
2. **Day 2:** Learn the terminal basics + your first Git commands. Create a local folder, `git init`, make a file, commit it.
3. **Day 3:** Create a repo on GitHub called `learning-journey`, push your local folder to it. Write a README listing your goals.
4. **Day 4:** Set up your ticket board (GitHub Projects / Trello / Jira). Create columns and your first 5 tickets for Phase 1.
5. **Day 5:** Read this whole roadmap once more. Set your weekly cadence (which days, which hours).
6. **Day 6:** Open CS50x, watch Lecture 0, start it.
7. **Day 7:** Sprint review — what worked, what didn't, what's next week.

---

## A few honest notes

- **It will feel hard and slow sometimes. That's the work, not a sign you're failing.** Everyone hits walls; the ones who make it just keep showing up.
- **Certificates are nice; projects on GitHub matter more.** Build things you can show.
- **Don't course-hop.** Finish the anchor for each phase before chasing shiny alternatives.
- **This document is alive.** As you learn what you actually enjoy (maybe you fall for ML, maybe for backend), tell Claude and we'll bend the plan toward it.

*You've got a real, complete path here. One week at a time.*
