# Facilitator Guide

For the people running the room. This is a developer session, with no product or QA track. The two rooms are developers split for size, and both run the same exercise.

## Across the session

One person demonstrates the whole flow once, then gets out of the way; the learning is in doing it. Protect the one result: every developer leaves with one spec turned into a reviewed design and task list. There is no code today, so no `/opsx:apply`. The commands are explore, then new and continue or propose, whichever the repo has. Keep the proposal and spec faithful to Jira; if the agent adds scope, have them tell it to match the ticket. The developer's value is the design and tasks. Keep changes small, and split a spec that is too big before generating design and tasks; split by behavior, never by layer or area of the page. Nothing is written to Jira until the developer approves it, and writes go to the Mocking Project sandbox.

## Two rooms

Both rooms run the same steps from Section 2, with one facilitator each. Agree a time to rejoin before splitting, and each room picks one person to show a result. With only one facilitator, collapse to a single room.

## By section

Section 1, orient. It is landing when someone reacts to a spec becoming a concrete design and task list. If the demo runs long, cut to one spec through design and tasks, but do not skip the moment where you split a spec that is too big. If a command is missing, create the file by hand under `.claude/commands/opsx/`, or re-run `openspec update` and restart, or ask Claude to run the workflow itself.

Section 2, breakout. It is landing when people stop reading the page and start typing their own prompts. If the agent takes on the whole feature, remind them: one capability, and split it. If a spec balloons, send them back to split first. If the agent rewrites the requirements, have them say match the Jira ticket. If someone says the design looks fine, ask whether every task traces to a spec decision.

Section 3, reconvene. Keep it on what the spec became and where they split, not on praise for the tool.

Closing. The rating is quick, but do not skip it; it shapes the next session.

## Dry-run checklist

Run the demo end to end once: explore, generate the proposal and spec, then the design and tasks, keeping it faithful to Jira and stopping before the build. Have one developer run it live, including splitting a spec. Confirm the Jira MCP works on a machine that is not the facilitator's, after a restart. Recover a missing command by writing the file by hand or re-running openspec update. Know the cut line: by 0:50, stop at a reviewed design and tasks, and do not build.
