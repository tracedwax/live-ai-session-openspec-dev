# Run of Show — OpenSpec for Devs

> **The page to keep open while you facilitate.** ~75 minutes. **Dev-only session — no Product track, no QA track.** Everyone together → **Mike demos once** → two **dev** rooms (split for size, same exercise) → reconvene.

## At a glance

| Section | Time | Who | What |
|---------|------|-----|------|
| **1 — Orient** | 0:00–0:20 | Everyone | Level-set, the handoff frame, connect Jira, **Mike runs the whole flow once** (`explore → new → continue`: proposal → spec → design → tasks) |
| **2 — Breakout** | 0:20–0:55 | Two dev rooms | Each dev runs it on their own story; the win is **one spec → reviewed design + tasks** |
| **3 — Reconvene** | 0:55–1:10 | Everyone | Two people show a result, open questions |
| **Closing** | 1:10–1:15 | Everyone | Plus/delta retro + rate the session |

> **Buffer:** Section 2 carries the slack. If a room flies, generate the next change. If it's slow, protect the one win: **one spec → a reviewed `design.md` + `tasks.md`.** Either way, **no `apply`/`ff` today** — design + tasks, not code.

## The spine (the whole session in one line)

> **`/opsx:explore` the specs that are there → `/opsx:new` → `/opsx:continue` one artifact at a time (proposal → spec → design → tasks) → review each.** Keep the **proposal + spec identical to Jira**; your value-add is **design + tasks.** No `ff`/`apply` today. *(Go-forward command: `/opsx:propose`.)*

> **The handoff (say it):** proposal + specs become **Product's** job going forward. Devs run the whole pipeline today so they can trust the spec they're handed; the dev's half is **design + tasks → build.**

## Facilitators & rooms

Two **dev** rooms running the **same** steps — split only so it's not one big room.

| Room | Facilitator | Output |
|------|-------------|--------|
| **Room A** | Mike | Each dev: one spec → reviewed `design.md` + `tasks.md`, one small full-stack increment |
| **Room B** | second facilitator | Same |

Open and close together.

## What's in the room (check before you start)

- [ ] **Claude Code in VS Code**, signed in, **Opus** model
- [ ] **Jira MCP connected (global)** — `claude mcp add --transport http --scope user atlassian https://mcp.atlassian.com/v1/mcp`, then `/mcp` to log in; **restart** so tools load
- [ ] **The working repo** open — it has OpenSpec installed and **existing specs**; OpenSpec writes `openspec/changes/...` here
- [ ] **OpenSpec commands present** — `/opsx:explore`, `/opsx:new`, `/opsx:continue`. Missing one? Create the file by hand at `.claude/commands/opsx/<name>.md` (or ask Claude), or re-run `openspec update` + **restart**. See [Prerequisites](prerequisites.md).
- [ ] Each dev has **one real story** to bring
- [ ] Any Jira writes go to the **Mocking Project (`MP`)** sandbox

## The pages

1. [Section 1 — Orient](section-1-orient.md) — level-set + Mike's demo
2. [Section 2 — Breakout](section-2-breakout.md) — the activity, with every prompt
3. [Section 3 — Reconvene](section-3-qa.md) — show & ask
4. [Closing](closing.md) — retro + Return-on-Time kata
5. [Cheat Sheet](cheatsheet.md) · [Worked Example](worked-example.md) · [The OpenSpec Process](openspec-process.md) — references

## Dry-run focus

Short on time? **Mike runs it end-to-end once**: `/opsx:explore` the existing specs → `/opsx:new` → `/opsx:continue` (proposal → spec → design → tasks), narrating **keep proposal+spec identical to Jira**, the **split-if-too-big** moment, and **stop before build**. Then one dev runs it live. That's the session.

## Housekeeping (read at the top)

- **Hands on keys.** Everyone runs it on their own story, screens shared.
- **Incremental, small chunks.** `/opsx:continue` one artifact at a time; split a spec >6–8 scenarios *before* design/tasks.
- **Behavior, not page area.** A spec is a full-stack behavior, never "the frontend" or "one panel."
- **Faithful to Jira.** Proposal + spec mirror the ticket; design + tasks are the value-add.
- **No code today.** Stop at design + tasks; don't `apply` or `ff`.
- **Nothing hits Jira without you confirming it.**
