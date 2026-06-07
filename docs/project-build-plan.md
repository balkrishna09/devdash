# Your Build Plan: One Project, Grown Across Every Phase

How the building stays in sync with the learning. Pairs with the roadmap (**what** to learn) and the operating system (**how** the loop runs). This one is **what you build, and when**.

---

## One project or many? The honest answer.

**One flagship project + two small support tracks.** Here's why, and what each is for:

1. **The flagship — `DevDash`.** One app you nurture from empty repo to deployed, monitored, secured data product over the whole journey. This is the spine. **It's the only way to learn *maintain*, *refactor*, and *scale*** — those skills don't exist in disposable tutorials; they only show up when you have to keep *the same* codebase alive and growing for months. Everything you said you want to learn — *continuously learn → develop → deploy → maintain → scale → secure* — lives here.
2. **Daily drills (`learning-drills` repo).** Tiny throwaway builds to practice a single concept in isolation before it goes into the flagship (e.g., a 30-line "how does `useEffect` work" sandbox). Not every concept earns a place in DevDash; reps go here.
3. **The course's own project.** The DE Zoomcamp ships with a guided capstone (NYC taxi data). You'll do it *on the course's rails* to learn the tools, then turn around and apply those same tools to DevDash on your own data. That's reinforcement, not double work: **learn the tool guided, then transfer it to something you own.**

So: one thing you build forever, plus reps and course work feeding it. Lead everything with the flagship.

---

## The flagship: `DevDash` — your personal developer + security dashboard

**The concept:** an app that tracks *your* learning and dev activity, ingests the security/tech ecosystem around your stack, and tells you what you've learned, what to learn next, and which vulnerabilities actually matter to you.

**Why this one fits *you* specifically:**
- It's **data-rich and data-*growing*** — the single most important property for data-engineering practice. Your commits, tickets, and live CVE/security feeds accrue over time, so your Phase 3 pipeline has real, messy, growing data to chew on (not a dead static CSV).
- It's **security-native** — Snyk findings on your own code sit right next to relevant public CVEs. That plays straight to your security background and the fact that you work at a security company.
- It's **motivating** — you use it every day, and it visibly tracks your own progress, so you'll actually keep building it for a year.
- It hits **every skill**: frontend, backend, DB, REST, auth, Docker, CI/CD, environments, cloud, orchestration, dbt, ML, LLMs, and DevSecOps.

> The *theme* is swappable (alternatives at the bottom) — but the **skeleton below works for any theme**, and DevDash is the one I'd pick for you. Rename it whatever you like.

---

## The lifecycle it forces you to learn

| Verb you asked for | Where it happens |
|---|---|
| **Learn** | Every phase, every day |
| **Develop** | Phase 2 — build the app |
| **Deploy** | Phase 2 — ship it to a real URL |
| **Maintain** | Phase 2 → ongoing — fix bugs, update deps, refactor, keep `main` green |
| **Scale** | Phase 3 — containerize, reverse-proxy, cache, measure RPS under load |
| **Secure** | Cross-cutting — Snyk from Phase 2 onward, findings → Bug tickets |

---

## The sync map (the part you asked for)

Each phase's *learning* produces a concrete *layer* of DevDash:

| Phase | You're learning | You build into DevDash | Skills exercised |
|---|---|---|---|
| **0–1** (brush-up) | Git, Python, fundamentals | A tiny Python CLI that logs a learning entry to a file. Seeds the repo. | Git, Python basics |
| **2** (full-stack) | React, backend, DB, REST, deploy, CI | The actual app: log entries via a UI, stored in Postgres, served by an API, deployed to a real URL, tests run in CI | frontend, backend, REST, DB, auth, deploy, **dev/prod envs**, CI, **Snyk SCA enters** |
| **3** (data eng — your target) | Docker, SQL, orchestration, warehouse, dbt, cloud | A pipeline that ingests your GitHub commits + Jira tickets + CVE feeds, lands them in a warehouse, transforms with dbt, and powers a real metrics dashboard | Docker mastery, SQL, **ingestion/ELT**, orchestration, dbt, cloud, **CI/CD + stg→prd**, **scaling/RPS**, **Snyk Container + IaC** |
| **4** (applied AI/ML) | pandas, scikit-learn, LLM apps | A model (e.g. "will you hit this week's goal?") served as an API, plus an LLM layer that auto-drafts tomorrow's ticket and your quiz | pandas, ML, model serving, **Claude API / LLM app**, MLOps taste |

**Per phase, in a bit more detail:**

- **Phase 2** — keep it *small*. Goal: a working, deployed CRUD app with auth and CI. Modules map to features: REST lesson → API contract; backend lesson → CRUD endpoints; DB lesson → schema + migrations; React lessons → the UI; deploy lesson → ship it; CI lesson → tests on every PR. **Resist building the data platform or heavy security here** — that's Phase 3. One clean full-stack app is plenty.
- **Phase 3** — DevDash grows a spine of data. This is your target role, so spend real time here. The pipeline ingests three sources (below), schedules itself, lands in a warehouse, and dbt turns raw events into your stats (streak, weekly velocity, language mix, "CVEs affecting my stack"). You containerize everything, add a reverse proxy + a load test to *see* RPS, and wire CI/CD that promotes dev → staging → prod.
- **Phase 4** — DevDash gets a brain. A small ML model on your accumulated data, served as an endpoint; then an LLM layer (Claude API) that closes the loop with your learning system by generating tickets and quizzes.

---

## The security thread: Snyk + the Bug loop

This is what makes "bugs and vulnerabilities" a *living* part of your practice instead of a checkbox.

**The loop (identical to your code-review loop, but for security):**
```
Snyk finds a vulnerability  →  you open a Jira BUG  →  fix on a branch  →  PR  →  I review + ask why it was exploitable  →  merge
```
Every vulnerability becomes a real ticket you triage and fix. You'll learn severity, fix paths, and *why* a thing was dangerous — not just "red bad."

**What each Snyk product is, and when it enters:**

| Snyk product | Scans | Enters in |
|---|---|---|
| **Open Source (SCA)** | your `package.json` / `requirements.txt` dependencies for known CVEs | **Phase 2** (basic), deepen later |
| **Code (SAST)** | *your own* code for security bugs (injection, secrets, etc.) | **Phase 2**, via the IDE plugin for inline feedback |
| **Container** | your Docker images / base images | **Phase 3** (when you containerize) |
| **IaC** | your Terraform / Kubernetes / YAML for misconfigs | **Phase 3** (when you touch cloud infra) |

**Setup notes:**
- Connect the **Snyk GitHub App** + add a **Snyk step in GitHub Actions** so every PR gets a security check next to your tests.
- Install the **Snyk IDE plugin (VS Code)** — it flags issues inline as you type, which is great for *learning* what insecure code looks like.
- **Keep the learning repos public.** Free-tier scan limits don't apply to public repos, and the GitHub Security-tab integration is free for public repos. (Also good for your portfolio.)
- **Pacing, honestly:** in Phase 2 you're nearly a beginner — just *run* Snyk, fix the easy dependency bumps, and file Bugs. Save deep severity-triage and container/IaC security for Phase 3 when you have the context. Don't drown Phase-2-you in CVE theory.

This whole thread is squarely DevSecOps / "shift-left security" — exactly the world your employer lives in, and a strong differentiator on a data/backend résumé.

---

## Where the pipeline's data comes from (Phase 3)

Use **official APIs and feeds — never scraping** (it's the legal, reliable, rate-limit-respecting choice, and learning auth + pagination + rate limits *is* the DE lesson):

- **GitHub REST API** → your commits, PRs, repo activity.
- **Your Jira** → your tickets (you already generate these daily).
- **NVD CVE feed** (public API) → vulnerabilities, joined against your stack so DevDash can say "this new CVE affects a library you use."
- *(Optional later)* a dev-news RSS feed or GitHub trending for "what's worth learning next."

Three real, heterogeneous, time-series sources = a properly realistic ingestion challenge.

---

## Your first build tickets

- **LEARN-1 — Stand up the system.** Create the Jira project, the two repos (`devdash`, `learning-drills`), connect GitHub-for-Jira and Snyk. *(Tests the whole loop on safe setup work.)*
- **LEARN-2 — First feature (your React Router example).** A multi-page shell for DevDash with nested routes — branch → PR → my review → merge. Your first real entry in the app.
- From there, every Story adds one slice, and DevDash is alive and growing within a week.

---

## If `DevDash` feels too meta — two alternative themes

Same skeleton, different subject:
- **Personal finance + markets tracker** — ingest transactions + live market/crypto prices; ML for spending anomalies. Rich external data, strong privacy/security angle for Snyk.
- **Skill-demand / job-market radar** — ingest job postings + tech trends (via APIs/feeds); recommend what to learn next; trend ML. Useful to a learner, data-rich.

Pick the one you'd happily open every day for a year. That choice matters more than the tech.
