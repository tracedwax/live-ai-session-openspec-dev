# Run of Show — OpenSpec for Devs

> **The page to keep open while you facilitate.** ~75 minutes. **Dev-only session — no Product track, no QA track.** Everyone together → **Mike demos once** → two **dev** rooms (split for size, same exercise) → reconvene.

## At a glance

| Section | Time | Who | What |
|---------|------|-----|------|
| **1 — Orient** | 0:00–0:20 | Everyone | Level-set, the handoff frame, connect Jira, **Mike runs the whole flow once** (story → proposal → specs → one spec → design + tasks) |
| **2 — Breakout** | 0:20–0:55 | Two dev rooms | Each dev runs it on their own story; the win is **one spec → reviewed design + tasks** |
| **3 — Reconvene** | 0:55–1:10 | Everyone | Two people show a result, open questions |
| **Closing** | 1:10–1:15 | Everyone | Plus/delta retro + rate the session |

> **Buffer:** Section 2 carries the slack. If a room flies, push `/opsx:apply` to start building from the tasks. If it's slow, protect the one win: **one spec → a reviewed `design.md` + `tasks.md`.**

## The spine (the whole session in one line)

> **Story → `/opsx:propose` → break into specs (split any spec that's too big) → take ONE spec → generate design + tasks → review.** In: a spec. Out: design + tasks. **Incremental, full-stack by behavior, small chunks.**

> **The handoff (say it):** proposal + specs become **Product's** job going forward. Devs learn the whole pipeline today so they can trust the spec they're handed; the dev's half is **spec → design + tasks → build.**

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
- [ ] **OpenSpec available** — `/opsx:propose` works (`npm i -g @fission-ai/openspec` + `openspec init`, or ask Claude to look it up and run it)
- [ ] A **repo to work in** — OpenSpec writes `openspec/changes/...` here
- [ ] Each dev has **one real story** to bring
- [ ] Any Jira writes go to the **Mocking Project (`MP`)** sandbox, not a real backlog

## The pages

1. [Section 1 — Orient](section-1-orient.md) — level-set + Mike's demo
2. [Section 2 — Breakout](section-2-breakout.md) — the activity, with every prompt
3. [Section 3 — Reconvene](section-3-qa.md) — show & ask
4. [Closing](closing.md) — retro + Return-on-Time kata
5. [Facilitator Guide](facilitator-guide.md) — cues, risks, recovery
6. [The OpenSpec Process](openspec-process.md) — the reference (who owns each artifact)
7. [Example Stories](example-tickets.md) — four real tickets to practice on

## Dry-run focus

Short on time? **Mike runs the flow end-to-end once** (story → proposal → 2–3 specs → split one → pick one spec → `design.md` + `tasks.md`), narrating the **split-if-too-big** moment and the **proposal+spec is Product's going forward** frame. Then one dev runs **spec → design + tasks** live. That's the session.

## Housekeeping (read at the top)

- **Hands on keys.** Everyone runs it on their own story, screens shared.
- **Incremental, small chunks.** One spec at a time; split anything too big *before* generating design/tasks.
- **Behavior, not page area.** A spec is a full-stack behavior, never "the frontend" or "one panel."
- **Nothing hits Jira without you confirming it.**
