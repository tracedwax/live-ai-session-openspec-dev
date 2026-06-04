# Cheat Sheet

In comes a spec. Out come a design and tasks you can build from, one small full-stack increment. No code today.

## The flow

1. Open the repo. It already has OpenSpec and existing specs.
2. Run `/opsx:explore` to think through the specs that are there and your story. Use `/grill-me` to pressure-test it. Nothing is saved.
3. Run `/opsx:new` to scaffold the change. No artifacts yet.
4. Run `/opsx:continue` for the next artifact, one at a time: proposal, spec, design, tasks. Run `/grill-me` on the proposal and spec to surface missing decisions. Review each.
5. Stop. Do not run `/opsx:ff` or `/opsx:apply` today.

## Commands

`/opsx:explore` thinks a story through; nothing is saved.
`/opsx:new` scaffolds the change.
`/opsx:continue` generates the next artifact: proposal, spec, design, tasks.
`/grill-me` interviews you one question at a time.
`/opsx:ff` fast-forwards all artifacts at once; not today.
`/opsx:apply` builds the code; not today.

Going forward, the simplified one-shot is `/opsx:propose`, which is roughly new plus ff. Today we use new and continue so we can take the phases one at a time.

## Rules

Keep the proposal and spec identical to the Jira ticket; the requirements come from the ticket, not from you. Split by behavior, not by area of the page. Keep changes small, and split a spec with more than six to eight WHEN/THEN scenarios before generating design and tasks. Do not one-shot it: one artifact, review, then the next. Every task should trace to a spec decision; if it does not, the spec is incomplete. Confirm before any Jira write, and use the Mocking Project (MP) sandbox.

## The handoff (a potential split, work in progress, out of scope)

One way to split the work is proposal and spec to product, design and tasks to you. This is not prescribed; the process is your team's call and out of scope for this training. What we practice today is the tool: spec to design to tasks, and building later.
