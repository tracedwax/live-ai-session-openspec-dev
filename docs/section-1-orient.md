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

> "Tuesday, Product turned stories into **proposals and specs**. **Going forward that's their job** — the spec comes to you. Today you'll see the *whole* pipeline so you can trust what you're handed, but your half is the back half: **take a spec, generate the design and the tasks, then build.** In: a spec. Out: design + tasks."

> **Why a dev should care (say it plainly):** *"The spec is how the AI stops guessing. You review a one-page plan of WHEN/THEN — not 500 lines of wrong code you have to unwind afterward. Edge cases get decided **before** you build, not found in QA or prod. And every task traces to a spec decision, so the agent builds against the spec instead of vibing."*

## Mike runs the whole flow once (12 min)

**Mike drives on a real story; everyone watches the shape.** Narrate each move and name the artifact + who owns it.

**The reveal — Claude reads Jira:** *"Pull my story from Jira and summarize it."* → "I didn't paste it; Claude read it through the **MCP**."

Then the flow, one artifact at a time (this is what the rooms repeat):

1. **Story → proposal.** `/opsx:propose`. Open `proposal.md`, read the **Why / What Changes / Capabilities / Impact**. *"This is Product's deliverable going forward."*
2. **Proposal → specs.** One `spec.md` per capability, in **WHEN/THEN**. *"Also Product's, with you reviewing."*
3. **Split if too big.** If a spec has **more than ~6–8 WHEN/THEN** scenarios, it's two behaviors — split it into smaller specs *before* going further. Show that judgment call out loud.
4. **Spec → design + tasks (your half).** Take **one** spec and generate `design.md` (architecture, data, **risks**) and `tasks.md` (a numbered checklist, each item tracing to a decision). *"This is where your job starts."*
5. **Name the discipline:** *"One spec, one full-stack increment — a behavior, not a page area. Small chunks, or the agent goes off the rails."*

Close: *"That's the target — a spec became a design and a task list you could build from. You'll do it on your own story in a minute."*

> **Fallbacks:** No `/opsx:propose`? *"Look up OpenSpec's opsx propose and run that workflow yourself."* No `/grill-me`? *"Interview me one question at a time before writing."*

## Done when

- The room has seen **story → proposal → specs → one spec → design + tasks**, named with owners
- Everyone knows the handoff (proposal+spec → Product; spec → design+tasks → you)
- Everyone knows their room and their story

Send them to [Section 2](section-2-breakout.md).
