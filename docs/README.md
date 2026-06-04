# OpenSpec for Devs — Spec → Design → Tasks

Welcome. This is the **developer** session. It picks up where the Product session left off: a **spec** comes to you, and you turn it into what you build from — a **design** and a **task list** — one small, full-stack increment at a time.

> **Tooling:** Claude Code in **VS Code**, with the **Jira MCP** and **OpenSpec** (`/opsx:*`). Model: **Opus**.

## The handoff (a potential split — WIP, out of scope)

Tuesday, Product learned to take a story and produce a **proposal** and **specs**. *One possible* way to divide the work is for that to be Product's job and the spec to come *to* you — but **process is out of scope for this training; that division is a potential/WIP frame, not a mandate.** Today you run the **whole** pipeline only so you can trust a spec you're handed. What we're teaching is the back half:

> **In: an OpenSpec spec. Out: a design and tasks** a developer (or the agent) can build from.

## The flow (today's commands)

1. **Bring a story** (pull it from Jira).
2. **`/opsx:explore`** — think through the specs already in the repo and your story. *Nothing is saved.*
3. **`/opsx:new`** — scaffold the change. *(No artifacts yet.)*
4. **`/opsx:continue`** (repeat) — generate the **next** artifact, one at a time: **proposal → spec → design → tasks.** Review each. **Keep the proposal + spec identical to the Jira ticket** — don't invent scope.
5. **Stop before building.** No `/opsx:ff`, no `/opsx:apply` today — we want **design + tasks**, not code.

> *Go-forward,* the simplified one-shot is **`/opsx:propose`**. Today we use `new` + `continue` so we can break the phases out and review each.

Two rules we hold all session:
- **Incremental.** One spec, one artifact at a time. Keep changes small (1–2 capabilities) so the agent doesn't go off the rails.
- **Full-stack by behavior, never by page area.** A spec is a behavior a user can observe end to end (`guest-checkout`), **not** "the header" or "the payment panel."

## How the session runs

| | |
|---|---|
| **Section 1 — Orient** | All together. Level-set, then **Mike runs the whole flow once**. |
| **Section 2 — Breakout** | **Two rooms.** You run it on your own story: spec → design + tasks. |
| **Section 3 — Reconvene** | All together. Show one result, ask anything. |
| **Closing** | Quick retro + rate the session. |

## Before you arrive

Do the [Prerequisites](prerequisites.md): Claude in VS Code (Opus), **Jira MCP (global)**, the working repo with **OpenSpec + existing specs**, and **one real story**. Keep the **[Cheat Sheet](cheatsheet.md)** open. The method is in **[The OpenSpec Process](openspec-process.md)**.
