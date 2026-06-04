# Facilitator Guide (Dev session)

> For the people running the room. This is a **dev-only** session — **no Product track, no QA track.** The "two rooms" are just devs split for size; both rooms run the **same** exercise.

## Cross-cutting

- **Mike demos the whole flow once, then get out of the way.** The learning is them doing it.
- **Protect the one win:** every dev leaves with **one spec turned into a reviewed `design.md` + `tasks.md`** for one full-stack increment. **No code today** — no `/opsx:apply`, no `/opsx:ff`.
- **Today's commands:** `/opsx:explore` → `/opsx:new` → `/opsx:continue` (one artifact at a time). *Go-forward is `/opsx:propose`* — say so, but don't use it today.
- **Keep proposal + spec faithful to Jira.** The requirements are Product's; if `/opsx:continue` embellishes, have them tell it *"match the ticket, don't add scope."* The dev's value-add is design + tasks.
- **Incremental, behavior, small chunks.** One spec at a time; if a spec has >6–8 WHEN/THEN, split it *before* design/tasks. Full-stack by behavior — never frontend/backend/page-area.
- **Confirm-before-write:** nothing hits Jira until the dev says go; writes go to the **Mocking Project (`MP`)** sandbox.

## Two-room coordination

- Both rooms are dev rooms running the same steps from [Section 2](section-2-breakout.md). Mike runs one; a second facilitator runs the other.
- Agree a rejoin time before splitting; each room nominates one person to show in [Section 3](section-3-qa.md).
- Solo? Collapse to one room — the page supports it.

## Per-section

**Section 1 — Orient.** *Cue it's landing:* someone reacts when a spec becomes a concrete `design.md` + `tasks.md`. *Risk:* the demo runs long — if it bleeds, cut to **one** spec → design + tasks; don't skip the split-if-too-big moment. *Risk:* an `/opsx:*` command is missing (e.g. `openspec update` didn't refresh `.claude/commands/opsx/`) — **create the command file by hand** at `.claude/commands/opsx/<name>.md` (or ask Claude to), or re-run `openspec update` and **restart Claude Code**; worst case, "ask Claude to look up the OpenSpec workflow and run it itself."

**Section 2 — Breakout.** *Cue:* people stop reading the prompt page and start typing their own. *Risk:* the agent bites off the whole feature → remind them: one capability, split it. *Risk:* a spec balloons → send them back to split first. *Risk:* `/opsx:continue` rewrites the requirements → "match the Jira ticket, don't add scope." *Risk:* "design looks fine, ship it" → ask *"does every task trace to a spec decision?"*

**Section 3 — Reconvene.** Keep it on *"what did your spec become, and where did you split?"* not tool praise.

**Closing.** The Return-on-Time kata is non-negotiable — even 60 seconds.

## Dry-run checklist

- [ ] Demo: **`/opsx:explore` → `/opsx:new` → `/opsx:continue`** (proposal → spec → design → tasks), end to end once
- [ ] One dev runs it live, including the split judgment, keeping proposal+spec faithful to Jira
- [ ] Jira MCP connected on a non-facilitator machine (restart after connecting)
- [ ] A missing `/opsx:*` command recovered via the by-hand file (or `openspec update` + restart)
- [ ] Cut line known: at 0:50, stop at **a reviewed design + tasks**; no `apply`/`ff`
