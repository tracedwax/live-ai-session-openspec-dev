# OpenSpec for Devs: Spec to Design and Tasks

This is the developer session. It picks up where the product session left off. A spec comes to you, and you turn it into the two things you build from: a design and a task list, one small full-stack increment at a time.

You work in Claude Code inside VS Code, with the Jira MCP and OpenSpec, on the Opus model.

## The handoff (a potential split, work in progress, out of scope)

On Tuesday, product practiced taking a story and producing a proposal and specs. One way to divide the work is for that to sit with product and for the spec to come to you. The process itself is out of scope for this training, and that division is a work in progress, not a decision. Today you run the whole pipeline so you can trust a spec you are handed. What we teach is the back half: in comes a spec, and out come a design and tasks a developer or the agent can build from.

## The flow

1. Bring a story and pull it from Jira.
2. Run `/opsx:explore` to think through the specs already in the repo and your story. Use `/grill-me` here to pressure-test it. Nothing is saved yet.
3. Generate the change. Either go one artifact at a time with `/opsx:new` then `/opsx:continue`, or generate them together with `/opsx:propose`. Use whichever your repo has; both produce the proposal, then the spec, then the design, then the tasks.
4. Run `/grill-me` again on the proposal and the spec to surface the decisions they are still missing, and keep both identical to the Jira ticket. Do not invent scope.
5. Stop before building. Do not run `/opsx:apply` today. We want a design and tasks, not code.

`/opsx:new` plus `/opsx:continue` lets you take the phases one at a time and review each; `/opsx:propose` does them in one step. Either is fine.

Two things we hold to all session. Keep changes small, one or two capabilities, so the agent does not take on too much. Split by behavior, not by area of the page: a spec is a behavior a user can observe end to end, such as guest checkout, not the header or the payment panel.

## How the session runs

Section 1 is orient, everyone together: a short level-set, then one person runs the whole flow once. Section 2 is the breakout, in two rooms: you run it on your own story. Section 3 is reconvene, everyone together: show one result and ask questions. Then a short closing retro and rating.

## Before you arrive

Do the prerequisites: Claude in VS Code on Opus, the Jira MCP connected globally, the working repo with OpenSpec and existing specs, and one real story. Keep the cheat sheet open. The method is in the OpenSpec process page.
