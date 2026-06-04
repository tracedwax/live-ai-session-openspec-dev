# Cheat Sheet

One screen. Keep it open while you work.

> **In:** an OpenSpec **spec.** **Out:** a **design + tasks** you can build from. One small, full-stack increment. **No code today.**

## The flow (today's commands)
1. **Open the repo** — it already has OpenSpec and existing specs.
2. **`/opsx:explore`** — think through the specs that are there + your story. *Nothing is saved.*
3. **`/opsx:new`** — scaffold the change. *(No artifacts yet — that's the next step.)*
4. **`/opsx:continue`** (repeat) — generate the **next** artifact, one at a time: **proposal → spec → design → tasks.** Review each.
5. **Stop.** Do **not** run `/opsx:ff` or `/opsx:apply` today — we want design + tasks, not code.

## Commands (today)
| Command | Does |
|---|---|
| `/opsx:explore` | think it through (nothing saved) |
| `/opsx:new` | scaffold the change |
| `/opsx:continue` | generate the **next** artifact (proposal → spec → design → tasks) |
| `/grill-me` | interview me one question at a time |
| `/opsx:ff` | fast-forward **all** artifacts — **not today** (overshoots) |
| `/opsx:apply` | build the code — **not today** |

> **Go-forward:** the simplified one-shot is **`/opsx:propose`** (≈ `new` + `ff`). Today we use `new` + `continue` so we can **break the phases out** and review each.

## Rules
- **Keep the proposal + spec identical to the Jira ticket.** Don't invent scope — requirements are Product's. Your value-add is **design + tasks**.
- **Behavior, not page area.** A full-stack behavior, never "frontend / backend / header."
- **Small chunks.** Split a spec with **>6–8 WHEN/THEN** into smaller specs *before* design + tasks.
- **Don't one-shot.** One artifact → review → next. Tell it to slow down if it races.
- **Every task traces to a spec decision.** If not, the spec is incomplete.
- **Confirm before any Jira write.** Sandbox = **Mocking Project (`MP`)**.

## The handoff *(potential process — WIP, out of scope today)*
*One possible* split: proposal + spec → **Product**, design + tasks → **you**. **Not prescribed** — process is your team's call and out of scope for this training. What we practice today is the **tool**: spec → design → tasks (→ build, later).
