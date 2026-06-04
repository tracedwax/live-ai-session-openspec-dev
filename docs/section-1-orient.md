# Section 1 — Orient

> **~20 min. All together.** Ends with everyone having watched the whole flow once and knowing their half of it.

## Rules of engagement (read first)

1. **Follow along live** — do it on your own machine, not by watching.
2. **Share your screen** in the breakout so facilitators can unstick you fast.
3. **Speak up the moment a question lands.**

Two habits all session: **nothing hits Jira until you say go**, and **messy input is the point**. Keep the **[Cheat Sheet](cheatsheet.md)** open — every command and rule on one screen.

## Welcome & level-set (5 min)

Round-robin, two things each:
> *"What did you do with AI this week? And which story did you bring today?"*

Confirm everyone has a story open. Anyone without one — flag it.

## The handoff frame (3 min)

> "Tuesday, Product turned stories into **proposals and specs**. **Going forward that's their job** — the spec comes to you. Today you'll run the *whole* pipeline so you can trust what you're handed, but your half is the back half: **the design and the tasks.** In: a spec. Out: design + tasks. No code today."

> **Why a dev should care (say it plainly):** *"The spec is how the AI stops guessing. You review a one-page plan of WHEN/THEN — not 500 lines of wrong code you have to unwind afterward. Edge cases get decided **before** you build, not found in QA or prod. And every task traces to a spec decision, so the agent builds against the spec instead of vibing."*

## Mike runs the whole flow once (12 min)

**Mike drives on a real story; everyone watches the shape.** Narrate each move and name the artifact + who owns it.

**The reveal — Claude reads Jira:** *"Pull my story from Jira and summarize it."* → "I didn't paste it; Claude read it through the **MCP**."

Then the flow (this is what the rooms repeat):

1. **Explore what's there.** `/opsx:explore` the specs already in the repo and your story. *"Thinking time — nothing's saved yet."*
2. **Scaffold.** `/opsx:new` creates the change. *"It scaffolds; it doesn't write the artifacts yet."*
3. **Generate one artifact at a time.** `/opsx:continue` produces the **next** artifact — proposal → spec → design → tasks — and you review each. **Keep the proposal and spec identical to the Jira ticket**; if it embellishes, say *"match the ticket exactly, don't add scope."* *"The requirements are Product's; your value-add is the design and the tasks."*
4. **Split if too big.** If a spec passes ~6–8 WHEN/THEN scenarios, it's two behaviors — split before going on.
5. **Stop before building.** We do **not** run `/opsx:ff` (fast-forwards everything) or `/opsx:apply` (writes code) today — the goal is **design + tasks**, not code.

> **Today vs. go-forward (say it):** *"Today we use `/opsx:new` + `/opsx:continue` — that's what's installed, and it lets us break the phases out and review each. The go-forward command is `/opsx:propose`, which rolls these up."*

Close: *"That's the target — a spec became a design and a task list you could build from, and we kept the requirements faithful to Jira. You'll do it on your own story in a minute."* (Want to see a finished one first? Show the **[Worked Example](worked-example.md)**.)

> **Fallback:** No `/opsx:*` commands in the repo? *"Look up OpenSpec's explore/new/continue and run that workflow yourself."* No `/grill-me`? *"Interview me one question at a time before writing."*

## Done when

- The room has seen **explore → new → continue** produce proposal → spec → **design + tasks**, named with owners
- Everyone knows the handoff (proposal + spec faithful to Jira; design + tasks are the dev's)
- Everyone knows their room and their story

Send them to [Section 2](section-2-breakout.md).
