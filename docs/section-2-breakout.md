# Section 2: Breakout

About 35 minutes, in two rooms (developer rooms, split for size). In comes a spec; out come a design and tasks, one small full-stack increment. No code today. Work on your own story, hands on keys, screens shared.

Each step says what to accomplish, not exactly what to type. Talking to the agent in your own words is the skill. If you are stuck for words, open the example prompt; the examples are a fallback, not the path.

Do not one-shot it. Make one artifact, read it, fix it, then the next. If the agent races ahead, tell it to slow down.

## Step 0: Open the repo

Open Claude in the repo we are working in today, which already has OpenSpec and existing specs, on Opus. Ask Claude to make a small git commit after each step as an undo trail; you do not need to touch git yourself.

## Step 1: Explore

Run `/opsx:explore` to walk the specs already in the repo and your story. Run `/grill-me` alongside it to surface what is missing. Nothing is saved here; it is thinking time.

## Step 2: Generate the proposal and spec

Generate the change. Either go one artifact at a time with `/opsx:new` then `/opsx:continue`, or generate everything in one step with `/opsx:propose`. Use whichever your repo has. Run `/grill-me` on the proposal and on the spec to pull out the decisions they are still missing.

Keep the proposal and the spec identical to the Jira ticket. The requirements come from the ticket, not from you. If the agent adds scope, tell it to match the ticket exactly.

## Step 3: Split a spec that is too big

If a spec passes six to eight WHEN/THEN scenarios, that is two behaviors. Split it into smaller specs before you generate the design and tasks.

## Step 4: The design and tasks, your half

The design and tasks come out of the same flow. Read them as the person who will build it. The design covers the approach, data, risks, and tradeoffs; check that it holds and flag anything that contradicts the spec. The tasks are a numbered checklist, and every task should trace to a spec decision; one that does not means the spec is incomplete.

Keep it to one capability, end to end, full-stack. Do not split by layer or by area of the page. If it feels too big, go back to Step 3 and split.

## Step 5: Stop here today

We are not building. Do not run `/opsx:apply` today; the result we want is a reviewed design and task list. Building is a later session.

## Done when

You ran explore, generated a proposal and spec, and produced a design and tasks for one increment. The proposal and spec match the Jira ticket, and the design and tasks are your work. You split at least once if a spec was too big. Bring one result and one honest opinion to Section 3.
