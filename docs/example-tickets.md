# Example Stories

Four real tickets, shipped with the repo, if you didn't bring a story or want a reference for "what good looks like." Each is a realistic starting point for the dev flow: **story → proposal → spec → design + tasks.**

| Ticket | Type | Use it as |
|--------|------|-----------|
| **PUR-6243** | Bug / Purchase | ✅ **A clean spec exemplar** — its acceptance criteria are already Given/When/Then. Good model for what a `spec.md` should read like before you generate design + tasks. |
| **CHK-3334** | Story / Checkout | ✏️ **Sharpen-then-build** — requirement-shaped AC; turn it into a proposal + spec, then design + tasks. |
| **PPA-4978** | Bug / PPA | ✏️ **Behavior-rich** — business rules + edge cases; good for practicing the split when one spec gets too big. |
| **PUR-6336** | Task / AI data | ✏️ **"Is this one thing or many?"** — an implementation checklist; great for finding behavioral seams and splitting into smaller specs. |

The full files are in this repo (`examples/`). To use one:

> *"Pull [PUR-6243] from Jira (or read `examples/PUR-6243.md`). Treat it as my story: propose it, break it into specs, then take one spec and generate the design and tasks. Keep it to one full-stack increment."*

> **Splitting:** if a spec ends up with more than ~6–8 WHEN/THEN scenarios, that's two behaviors — split it into smaller specs first, then generate design + tasks for one.
