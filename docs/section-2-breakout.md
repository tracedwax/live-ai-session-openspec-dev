# Section 2 — Breakout: run it on your own story

> **~35 min. Two rooms.** You saw the shape; now do it. **In: a spec. Out: design + tasks** — one small, full-stack increment. Hands on keys, screens shared.

**Each step says what to accomplish, not what to type** — talking to the agent in your own words *is* the skill. Stuck for words? Open the example prompt. Examples are a safety net, not the path.

> **Don't one-shot it.** Make one artifact, read it, fix it, then the next. If the agent races ahead, tell it to slow down.

### Step 0 — Open your repo
Open Claude in a repo you can write to, on **Opus**. Make sure **OpenSpec** is available (`openspec init`, or ask Claude). Ask Claude to **autosave** (a tiny git commit after each step — your undo trail; you never touch git).

### Step 1 — Pull your story
> *"Pull story [KEY] from Jira and summarize what it's asking for. Don't write anything yet — tell me what's still ambiguous."*

### Step 2 — Story → proposal
> *"`/opsx:propose` for this story."* Read `proposal.md`: is the **Why** right? Are the **Capabilities** named as behaviors? Fix anything wrong before moving on.

> **Note:** Steps 2–3 become **Product's** job going forward. You're learning them so you can review the spec you'll be handed — then your real work starts at Step 4.

### Step 3 — Proposal → specs (split if too big)
You should have one `spec.md` per capability, in **WHEN/THEN**. **If any spec has more than ~6–8 scenarios, split it into smaller specs first** — that's two behaviors hiding in one.
> *"This spec is doing too much — split it into smaller, independently shippable specs, one behavior each."*

### Step 4 — Spec → design + tasks  *(your half)*
Pick **one** spec and get its engineering artifacts:
> *"Take `specs/<capability>/spec.md` and give me the design and tasks for it: `design.md` (architecture, data model, risks, tradeoffs) and `tasks.md` (a numbered checklist where each task traces to a spec decision). Just this one capability — one small full-stack increment, not the whole feature."*

(`/opsx:propose` may have already produced these; if so, focus on this one spec and refine them.)

Read them as the person who'll build it:
- **design.md** — does the approach hold? Read the **risks**; flag anything that contradicts the spec.
- **tasks.md** — does every task trace back to a spec decision? A task that doesn't means the spec is incomplete.

**Incremental, full-stack, by behavior.** One capability end to end — never a "frontend task" / "backend task" / "header" split. If it feels big, go back to Step 3 and chop it.

> **Want it one artifact at a time?** Turn on OpenSpec's expanded workflow once — `openspec config profile` (choose *expanded*), then `openspec update` — and use `/opsx:continue` to generate the **next** artifact (proposal → spec → design → tasks), stopping to review each. That's the most incremental path.

### Step 5 — *(stretch)* start building
Build **one task at a time, TDD** — the discipline that keeps the agent honest:
> *"`/opsx:apply`. Work the tasks one at a time, in order: for each, write the test first, run it and watch it fail, write the code, run it and watch it pass, then commit. Show me the diff before anything lands."*

Each task already traces to a spec decision, so the agent **executes the plan instead of guessing.** If a task is too vague to test, the spec or design is incomplete — fix that first. Ambiguity dies in planning, not in the build.

## Done when

- You took **one spec** and produced a **reviewed `design.md` + `tasks.md`** for one full-stack increment
- You split at least once if your spec was too big
- *(stretch)* you started `/opsx:apply` on the first task

Bring one result and one honest opinion to [Section 3](section-3-qa.md).
