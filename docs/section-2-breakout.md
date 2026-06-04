# Section 2 — Breakout: run it on your own story

> **~35 min. Two rooms** (dev rooms, split for size). **In: a spec. Out: design + tasks** — one small, full-stack increment. **No code today.** Hands on keys, screens shared.

**Each step says what to accomplish, not what to type** — talking to the agent in your own words *is* the skill. Stuck for words? Open the example prompt. Examples are a safety net, not the path.

> **Don't one-shot it.** Make one artifact, read it, fix it, then the next. If the agent races ahead, tell it to slow down.

> **Today's commands.** This repo ships the older OpenSpec set, so we use **`/opsx:explore` → `/opsx:new` → `/opsx:continue`**, one artifact at a time, and **stop before building** — no `/opsx:ff` (fast-forwards everything), no `/opsx:apply` (writes code). *(Go-forward, the simplified one-shot is `/opsx:propose`.)*

### Step 0 — Open the repo
Open Claude in the repo we're working in today (it already has OpenSpec and existing specs), on **Opus**. Ask Claude to **autosave** — a tiny git commit after each step (your undo trail; you never touch git).

### Step 1 — Explore what's there
> *"`/opsx:explore` — walk the specs already in this repo and my story with me. What does this change touch? What's still ambiguous? Don't write anything yet."*

Nothing is saved in explore — it's thinking time. Let `/grill-me` find the holes if you want.

### Step 2 — Scaffold the change
> *"`/opsx:new` for my story."*

This scaffolds the change. It does **not** write the artifacts yet — that's the next step.

### Step 3 — Generate one artifact at a time
> *"`/opsx:continue`."* — produces the **next** artifact. Run it, review, run it again: **proposal → spec → design → tasks.**

**Keep the proposal and the spec identical to the Jira ticket.** Don't let Claude invent scope — the requirements come from the ticket, not from you. If `/opsx:continue` embellishes, tell it:
> *"Match the Jira ticket exactly; don't add scope. We're generating the design and tasks, not rewriting the requirements."*

### Step 4 — Split if a spec is too big
If a spec passes **~6–8 WHEN/THEN scenarios**, that's two behaviors — split it into smaller specs *before* generating design + tasks.
> *"This spec is doing too much — split it into smaller specs, one behavior each."*

### Step 5 — Your half: design + tasks
These come out of `/opsx:continue`. Read them as the person who'll build it:
- **`design.md`** — architecture, data model, **risks**, tradeoffs. Does the approach hold? Flag anything that contradicts the spec.
- **`tasks.md`** — a numbered checklist; **every task should trace to a spec decision.** A task that doesn't means the spec is incomplete.

**Incremental, full-stack, by behavior.** One capability end to end — never a "frontend task" / "backend task" / "header" split. If it feels big, go back to Step 4 and chop it.

### Step 6 — Stop here today
We're **not** building. Don't run `/opsx:apply` (code) or `/opsx:ff` (all artifacts at once) today — the win is a reviewed **design + tasks**. Building is a later session; when it comes, it's TDD, one task at a time (test → fail → code → pass → commit).

## Done when

- You ran **explore → new → continue**, generating proposal → spec → **design + tasks** for one increment
- Your **proposal + spec match the Jira ticket**; the **design + tasks** are your value-add
- You split at least once if a spec was too big

Bring one result and one honest opinion to [Section 3](section-3-qa.md).
