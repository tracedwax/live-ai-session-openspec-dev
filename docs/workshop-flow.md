# Run of Show

The page to keep open while you facilitate. About 75 minutes. A developer session, with no product or QA track. Everyone starts together, one person demonstrates once, the room splits into two developer rooms, and everyone comes back together.

## At a glance

Section 1, orient, 0:00 to 0:20, everyone: level-set, the handoff, connect Jira, and one person runs the whole flow once. Section 2, breakout, 0:20 to 0:55, two rooms: each developer runs it on their own story, and the result is one spec turned into a reviewed design and tasks. Section 3, reconvene, 0:55 to 1:10, everyone: two people show a result and we take questions. Closing, 1:10 to 1:15: a short retro and a rating.

Section 2 carries the slack. If a room moves fast, start a second change. If it is slow, protect the one result: one spec, a reviewed design and tasks. Either way, there is no code today.

## The flow

Run `/opsx:explore` on the specs that are there, with `/grill-me`. Generate the change either one artifact at a time with `/opsx:new` and `/opsx:continue`, or in one step with `/opsx:propose`, whichever the repo has. Run `/grill-me` again on the proposal and the spec. Keep the proposal and spec identical to the Jira ticket; the design and tasks are the developer's work. Stop before `/opsx:apply`; there is no code today.

## The handoff (a potential split, work in progress, out of scope)

One way to split the work is proposal and spec to product, design and tasks to developers. The process is out of scope today and this split is a work in progress, not a decision; say so if anyone asks. Developers run the whole pipeline today only so they can trust a spec they are handed. What we teach is the tool.

## Rooms

Two developer rooms run the same steps, split only so it is not one large room, with one facilitator each. Open and close together, and each room picks one person to show a result at reconvene. If there is only one facilitator, run a single room.

## What's in the room

Claude Code in VS Code, signed in, on Opus. The Jira MCP connected globally, with Claude restarted so the tools load. The working repo open, with OpenSpec and existing specs. The OpenSpec commands present: explore, then new and continue, or propose. If one is missing, create the file by hand under `.claude/commands/opsx/`, or re-run `openspec update` and restart, or ask Claude to run the workflow itself. Each developer with one real story. Any Jira writes going to the Mocking Project sandbox.

## Pages

Section 1 orient, Section 2 breakout, Section 3 reconvene, the closing, the cheat sheet, the worked example, and the OpenSpec process page.

## Dry-run focus

If you are short on time, run it end to end once: explore the existing specs, generate the proposal and spec with new and continue or with propose, then the design and tasks. Narrate keeping the proposal and spec faithful to Jira, splitting a spec that is too big, and stopping before the build. Then have one developer run it live.

## Housekeeping

Everyone works on their own story with screens shared. Keep changes small and split a spec that is too big before generating design and tasks. Split by behavior, not by area of the page. Keep the proposal and spec faithful to Jira. There is no code today; stop at design and tasks. Nothing is written to Jira without approval.
