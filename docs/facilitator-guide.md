# Facilitator Guide (Dev session)

> For the people running the room. This is a **dev-only** session — **no Product track, no QA track.** The "two rooms" are just devs split for size; both rooms run the **same** exercise.

## Cross-cutting

- **Mike demos the whole flow once, then get out of the way.** The learning is them doing it.
- **Protect the one win:** every dev leaves with **one spec turned into a reviewed `design.md` + `tasks.md`** for one full-stack increment. `/opsx:apply` (building) is stretch.
- **Incremental, behavior, small chunks.** One spec at a time; if a spec has >6–8 WHEN/THEN, split it *before* generating design/tasks. Full-stack by behavior — never a frontend/backend or by-page-area split.
- **Say the handoff out loud:** proposal + specs become **Product's** job going forward; devs learn the whole pipeline today so they can trust the spec they're handed. Their half is **spec → design + tasks → build.**
- **Confirm-before-write:** nothing hits Jira until the dev reads the plan and says go; writes go to the **Mocking Project (`MP`)** sandbox.

## Two-room coordination

- Both rooms are dev rooms running the same steps from [Section 2](section-2-breakout.md). Mike runs one; a second facilitator runs the other.
- Agree a rejoin time before splitting; each room nominates one person to show in [Section 3](section-3-qa.md).
- Solo? Collapse to one room — the page supports it.

## Per-section

**Section 1 — Orient.** *Cue it's landing:* someone reacts when a spec becomes a concrete `design.md` + `tasks.md`. *Risk:* the demo runs long — if it bleeds, cut to **one** spec → design + tasks; don't skip the split-if-too-big moment, that's the judgment they need. *Risk:* `/opsx:propose` not installed — `openspec init` live or "ask Claude to look it up and run it."

**Section 2 — Breakout.** *Cue:* people stop reading the prompt page and start typing their own. *Risk:* the agent bites off the whole feature → remind them: one capability, split it. *Risk:* a spec is too big and design/tasks balloon → send them back to split first. *Risk:* "design looks fine, ship it" → ask *"does every task trace to a spec decision?"*

**Section 3 — Reconvene.** Keep it on *"what did your spec become, and where did you split?"* not tool praise.

**Closing.** The Return-on-Time kata is non-negotiable — even 60 seconds.

## Dry-run checklist

- [ ] Demo: **story → proposal → 2–3 specs → split one → pick one spec → `design.md` + `tasks.md`**, end to end once
- [ ] One dev runs **spec → design + tasks** live, including the split judgment
- [ ] Jira MCP connected on a non-facilitator machine (restart after connecting)
- [ ] Cut line known: at 0:50, stop at **a reviewed design + tasks**; skip the build stretch
