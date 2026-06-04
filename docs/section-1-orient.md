# Section 1: Orient

About 20 minutes, everyone together. By the end, the room has watched the whole flow once and knows which half is theirs.

## Rules of engagement

Follow along live on your own machine; you learn this by doing it, not by watching. Share your screen in the breakout so facilitators can help quickly. Ask questions the moment they come up. Two habits we keep all session: nothing is written to Jira until you approve it, and rough input is fine, because half-formed notes feed the agent better than a polished paragraph. Keep the cheat sheet open.

## Level-set (5 minutes)

Go around the room. Each person says what they did with AI this past week and which story they brought today. Confirm everyone has a story open in Jira, and flag anyone who does not.

## The handoff (3 minutes)

On Tuesday, product practiced turning stories into proposals and specs. One way to split the work is for that to be their job and the spec to come to you, but the process is out of scope today and that split is a work in progress, not a decision. What you practice today is the back half: a spec becomes a design and a task list. In comes a spec, out come a design and tasks. No code today.

The reason a developer should care: the spec is how the agent stops guessing. You review a short plan of WHEN and THEN behavior instead of unwinding hundreds of lines of wrong code afterward. Edge cases are decided before the build, not found in QA or production. And every task traces back to a spec decision, so the agent builds against the spec rather than improvising.

## The walkthrough (12 minutes)

One person runs the whole flow on a real story while the room watches. Pull the story from Jira first, so the room sees Claude read it through the MCP rather than pasting it in.

Then run the flow, naming each artifact as it appears.

1. Explore. Run `/opsx:explore` on the specs already in the repo and on the story, and run `/grill-me` alongside it to surface the gaps. Nothing is saved; this is thinking time.
2. Generate the proposal and spec. Either run `/opsx:new` then `/opsx:continue` to take them one at a time, or run `/opsx:propose` to generate them in one step, using whichever the repo has. Run `/grill-me` on the proposal and on the spec to pull out the decisions they are still missing. Keep both identical to the Jira ticket; if the agent adds scope, tell it to match the ticket.
3. Continue to the design and tasks. The same flow produces them. This is the developer's half.
4. Split when needed. If a spec passes six to eight WHEN/THEN scenarios, it is two behaviors; split it before going on.
5. Stop before building. Do not run `/opsx:apply` today; the goal is a design and tasks, not code.

A note for the room: new and continue lets you take the phases one at a time and review each; propose does it in one step. Use whichever the repo has.

Close by pointing at the result: a spec became a design and a task list you could build from, and the requirements stayed faithful to Jira. The worked example page shows a finished one if it helps.

If a command is missing, create it by hand or ask Claude to run the workflow itself. If grill-me is not installed, ask Claude to interview you one question at a time.

## Done when

The room has watched the flow produce a proposal, spec, design, and tasks. Everyone understands that the proposal and spec stay faithful to Jira and that the design and tasks are the developer's half. Everyone knows their room and has their story ready.
