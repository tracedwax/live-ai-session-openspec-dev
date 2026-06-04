# Example Stories

Four real tickets, in case you did not bring a story or want a reference for what good looks like. Each is a realistic starting point for the flow: explore, generate the proposal and spec, then the design and tasks.

- PUR-6243 (bug, Purchase): a clean spec to copy. Its acceptance criteria are already in Given/When/Then, so it is a good model for what a spec should read like before you generate design and tasks.
- CHK-3334 (story, Checkout): requirement-shaped acceptance criteria. Turn it into a proposal and spec, then design and tasks.
- PPA-4978 (bug, PPA): business rules and edge cases. Good for practicing the split when one spec gets too big.
- PUR-6336 (task, AI data): an implementation checklist. Good for finding the behavioral seams and splitting into smaller specs.

The full files are in this repo under `examples/`. To use one: pull it from Jira, or read `examples/PUR-6243.md`, treat it as your story, generate the proposal and spec, then take one spec and generate the design and tasks, keeping it to one full-stack increment.

If a spec ends up with more than six to eight WHEN/THEN scenarios, that is two behaviors. Split it into smaller specs first.
