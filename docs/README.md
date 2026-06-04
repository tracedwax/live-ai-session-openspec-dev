# OpenSpec for Devs — Spec → Design → Tasks

Welcome. This is the **developer** session. It picks up where the Product session left off: Product hands you a **spec**, and you turn it into what you build from — a **design** and a **task list** — one small, full-stack increment at a time.

> **Tooling:** Claude Code in **VS Code**, with the **Jira MCP** and **OpenSpec** (`/opsx:*`). Model: **Opus**.

## The handoff (say this out loud)

Tuesday, Product learned to take a story and produce a **proposal** and **specs**. **Going forward, that's Product's job** — proposal and spec come *to* you. Today you learn the **whole** pipeline so you can read and trust what Product hands you, but **your job starts at the spec**:

> **In: an OpenSpec spec. Out: a design and tasks** a developer (or the agent) can build from.

## The flow

1. **Bring a story** (pull it from Jira).
2. **Story → proposal** (`/opsx:propose`).
3. **Proposal → specs** — one spec per capability. *If a spec is too large, split it into smaller specs first.*
4. **Spec → design + tasks** — the engineering artifacts. **This is your half.**
5. *(stretch)* **Tasks → build** with `/opsx:apply`.

Two rules we hold all session:
- **Incremental.** One spec, one increment at a time. If the agent bites off too much it goes off the rails — keep chunks small.
- **Full-stack by behavior, never by page area.** A spec is a behavior a user can observe end to end (`guest-checkout`), **not** "the header" or "the payment panel."

## How the session runs

| | |
|---|---|
| **Section 1 — Orient** | All together. Level-set, then **Mike runs the whole flow once**. |
| **Section 2 — Breakout** | **Two rooms.** You run it on your own story: spec → design + tasks. |
| **Section 3 — Reconvene** | All together. Show one result, ask anything. |
| **Closing** | Quick retro + rate the session. |

## Before you arrive

Do the [Prerequisites](prerequisites.md): Claude in VS Code, **Jira MCP (global)**, **OpenSpec**, a repo to work in, and **one real story**. The method is in **[The OpenSpec Process](openspec-process.md)** — keep it open.
