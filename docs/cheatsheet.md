# Cheat Sheet

One screen. Keep it open while you build.

> **In:** an OpenSpec **spec.** **Out:** a **design + tasks** you can build from. One small, full-stack increment.

## The flow
1. **Pull your story** from Jira.
2. **`/opsx:propose`** → proposal + specs (+ design + tasks).
3. **Review proposal + specs.** Split any spec with **>6–8 WHEN/THEN** into smaller specs.
4. **Take ONE spec** → review/generate its **`design.md`** + **`tasks.md`**.
5. *(stretch)* **`/opsx:apply`** → build **one task at a time, TDD**: test → fail → code → pass → commit.

## Commands
| Command | Does |
|---|---|
| `/opsx:explore` | think a story through (nothing saved) |
| `/opsx:propose` | create the change: proposal + specs + design + tasks |
| `/opsx:apply` | work the tasks (build) |
| `/grill-me` | interview me one question at a time |
| `openspec init` | add `/opsx:*` to this repo (if missing) |

**Incremental, one artifact at a time:** `openspec config profile` → *expanded*, then `openspec update`, then **`/opsx:continue`** (proposal → spec → design → tasks, review each).

## Rules
- **Behavior, not page area.** A spec is a full-stack behavior a user can observe — never "frontend / backend / header."
- **Small chunks.** 1–2 capabilities per change. Big story? Split *before* design + tasks.
- **Don't one-shot.** One artifact → read → fix → next. Tell it to slow down if it races.
- **Every task traces to a spec decision.** If it doesn't, the spec is incomplete. Ambiguity dies in planning, not the build.
- **Build TDD.** One task at a time: test → fail → code → pass → commit.
- **Confirm before any Jira write.** Sandbox = **Mocking Project (`MP`)**.

## The handoff
Proposal + spec → **Product** going forward. Your half: **spec → design → tasks → build.**
