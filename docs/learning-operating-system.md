# Your Learning Operating System

The runbook for how the daily machine runs. Pairs with `beginner-to-engineer-roadmap.md` (that one is **what** to learn; this one is **how the loop, tracking, and verification work**). Drop both into your Claude Project so every chat knows the rules.

---

## The daily loop (one picture)

```
MORNING   nudge fires  →  open today's Jira Story  →  ask Claude for the detailed breakdown + resources
DAYTIME   learn the concept  →  build it on a branch  →  commit  →  open a PR  →  comment on the Story
EVENING   open Claude  →  "Review LEARN-12"  →  I read Story + comment + PR, give a verdict, then quiz you
          PASS → merge PR, Story → Done, log one line.   PARTIAL/REDO → fix it, no merge.
```

That's the whole engine. No autonomous agent required — it runs on a Jira board, a GitHub repo, a Claude Project, and one honest evening check-in.

---

## 1. Jira setup (personal, free)

1. Create a free Jira Cloud site (jira.com → free plan). Make a **team-managed Software project**. Give it the key **LEARN**.
2. **Hierarchy reality check:** on the free plan your native levels are **Epic → Story / Task / Bug → Sub-task**. A true *Initiative* type is a Premium-only thing. So we map it cleanly:

| Level | What it represents | Example |
|---|---|---|
| **The project itself** (`LEARN`) | Your "initiative" — the overall goal | *Become a job-ready engineer* |
| **Epic** | A phase / big skill area | *Phase 2 — Full-Stack Web* |
| **Story** | One concept (a day to a few days) | *LEARN-12 — React Router basics* |
| **Sub-task** | A granular step inside a Story | *Set up nested routes* |
| **Bug** | Something you got wrong and must fix | *Route doesn't re-render on param change* |

> Bugs are a feature, not a failure. Logging your own mistakes as Bug tickets and fixing them is exactly how you learn debugging *and* how real teams work.

3. **Statuses:** `To Do → In Progress → In Review → Done`. (`In Review` = built, PR open, waiting for my verdict.)
4. **Naming convention for Stories:** `<concept> — <verb> <thing>`, e.g. *"React Router — build a multi-page app with nested routes."*
5. Each Story's **description holds its Definition of Done** (see §4). Don't skip this — it's what I check against.

---

## 2. GitHub setup + the corporate flow you wanted

**Two repos:**
- `learning-drills` — daily concept builds. One folder per concept (`/react-router/`, `/sql-joins/`). Each Story = one branch → PR → merge here.
- `learning-tracker` — your capstone (see §8), built up across phases.

**Connect Jira ↔ GitHub:** install the official **GitHub for Jira** app and link your account. Then any branch/commit/PR that mentions the issue key shows up automatically in that Story's *Development* panel. This is how you "link the repo to the ticket."

**The flow, per Story (this is the real corporate feature-branch flow):**
```
git checkout main && git pull
git checkout -b LEARN-12-react-router        # branch named with the key
# ...build the thing...
git commit -m "LEARN-12: add nested routes"   # key in the commit
git push -u origin LEARN-12-react-router
# open a Pull Request titled:  LEARN-12 React Router basics
# → I review the diff + quiz you → you merge to main → delete the branch
```
`main` always stays clean and working. You never commit straight to `main`. That single habit is most of what "working like a corporate dev" means.

---

## 3. The verification protocol (the core — built from your own description)

**Definition of Done for any Story — ALL of these, or it's not done:**
1. **Code:** committed on the branch, PR opened, linked to the Story.
2. **Story comment — in your own words:**
   - *What I learned* (3–5 lines).
   - *What tripped me up* (1–2 lines). "Nothing" is rarely true; dig.
3. **Proof it runs:** output, a screenshot, or a live link.

**The review (evening Claude chat):**
- I read the **Story + your comment + the PR/diff**.
- I give a blunt verdict, one line of reason each:
  - **PASS** — solid, merge it.
  - **PARTIAL** — works but a gap (named). Patch before merge.
  - **REDO** — misunderstood or not really yours. Back to In Progress.
- **The anti-cheat quiz** (this is the part that makes it real): 2–3 *"why does this work / what breaks if I change X"* questions, plus **one "extend it live, right now"** task — e.g. *"add a 404 route while I watch."* If you can extend it cold, you own the concept. If you can't, the code looking right doesn't save you → PARTIAL/REDO.

**Integrity note, brutally:** this loop only works if you bring real work and answer the quiz without looking up the answer mid-question. Copy-pasting code you can't extend just means you pay later, with interest, when the next concept builds on it. I'll assume good faith and probe hard enough to catch hand-waving — that's the deal you asked for.

---

## 4. Claude Project setup

- One Project — call it **"Learning OS."**
- Put in its knowledge: this file, the roadmap file, and a **`progress.md`** you keep current (active Epic + Story, last few verdicts, current blockers).
- Keep *all* learning chats inside this Project so context carries day to day.
- **Daily start:** open Project → *"Today's ticket?"* → I pull the day's Story and give you the detailed breakdown + the best resource for it.
- **Daily end:** *"Review LEARN-12"* → paste the Story comment + PR link (or connect the repo) → I verify.

---

## 5. The morning nudge (your "hybrid" choice)

- **Now (reliable, zero fragility):** a recurring phone/calendar reminder at your wake-up time that just says *"Open Claude → today's ticket."* That's the nudge; the detail comes from Claude manually. This is the whole hybrid, and it never breaks.
- **Upgrade later (Phase 2+, once Claude Code is set up):** a **Claude Code Routine** that posts the day's Story to your Slack each morning automatically. It's a paid-plan feature (you have Pro; one nudge a day is well within limits) and runs in the cloud whether your laptop is open or not. We'll set this up when you're already using Claude Code, not before — no point adding a moving part for a job a calendar alert does fine today.

---

## 6. Weekly rhythm (mirrors a real sprint)

- **Monday, 15–30 min — sprint planning:** together we create the week's Stories in Jira from the roadmap, sized to your real hours.
- **Daily — execute one Story** through the loop above.
- **Friday, 15 min — retro:** what shipped, what slipped, update `progress.md`, groom next week's Stories.

You're now running Scrum/Kanban on yourself. When you later read the formal terms (velocity, WIP limits, backlog grooming, standup), they'll map onto something you've already lived.

---

## 7. The capstone — build this very system as an app

Grow one project feature-by-feature so each phase bolts on a layer. By the end it's a real data product *about your own learning*:

- **Phase 2 (web):** React frontend + FastAPI/Node backend + Postgres + auth → a board to log tickets. *(frontend, backend, REST, DB, Docker, deploy, CI/CD, environments)*
- **Phase 3 (data eng — your target):** a pipeline that ingests your real **GitHub commits + Jira tickets**, lands them in a warehouse, transforms with dbt, orchestrated and containerized → a dashboard of your actual progress. *(Docker mastery, cloud, orchestration, dbt, SQL, load-test taste for RPS)*
- **Phase 4 (AI):** a layer that auto-drafts tomorrow's ticket and generates your quiz. *(LLM app / Claude API)*

Meta-bonus: by Phase 3, the thing you built is analyzing the very Jira + GitHub trail this system generates.

---

## 8. Non-negotiables

- **Type code yourself** in the early phases. Let Claude Code take more of the wheel only after you can already do it by hand.
- **Never merge a REDO.** A fake green checkmark is worse than a red one.
- **Two real sessions a week beats seven imaginary ones.** Consistency over intensity.
- **The plan bends to you.** When a Story is too big, split it. When something clicks fast, pull the next one forward. Tell me and we adjust.

---

*This is the layout. Once I have your GitHub username and your real weekly hours, I'll write your first ticket and we start.*
