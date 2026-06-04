# Prerequisites

Two required things, and a few that make the session real.

## Required: Claude Code in VS Code (on Opus)

Install **VS Code**, add the **Claude Code extension**, sign in, and set the model to **Opus**. Ask it *"tell me a joke"* — if you get one back, you're ready.

## Required: a story to bring

Bring **one real story** you'd actually pick up. Rough is fine — unrefined is the point; that's what OpenSpec sharpens. Bring whatever you have about it too (notes, a Slack thread, a screenshot).

## Connect Jira (the MCP) — once, globally

> *"Set up the Atlassian MCP globally: run `claude mcp add --transport http --scope user atlassian https://mcp.atlassian.com/v1/mcp`, then walk me through the `/mcp` browser login."*

**Restart Claude Code after connecting** so the tools load; confirm `claude mcp list` shows `atlassian … ✓ Connected`. Any live writes go to the **Mocking Project (`MP`)** sandbox, not a real backlog.

## The repo we work in

Today we work in the repo that already has **OpenSpec installed and existing specs** (your facilitator points you to it). OpenSpec writes `openspec/changes/<change>/` files there. You write **no application code** today — just the proposal, specs, design, and tasks.

## OpenSpec commands (today vs. go-forward)

Today's repo ships the **older** set: **`/opsx:explore`, `/opsx:new`, `/opsx:continue`** (plus `apply`, `verify`, `archive`). We use **explore → new → continue** — one artifact at a time — and **stop before building** (no `ff`, no `apply`). *Go-forward,* the simplified one-shot is **`/opsx:propose`**.

**If an `/opsx:*` command is missing** (e.g. `openspec update` didn't refresh `.claude/commands/opsx/`), three fallbacks — easiest first:

1. **Create it by hand** — a slash command is just a markdown file in `.claude/commands/`. Ask Claude: *"Look up what OpenSpec's `opsx:new` command does and create `.claude/commands/opsx/new.md` for it."*
2. **Re-run `openspec update`, then restart Claude Code** so it reloads the commands.
3. **Skip the command** — *"Look up OpenSpec's explore / new / continue workflow and just run it yourself."*

## Stuck on setup?

Post in the channel before the session — we'd rather fix it now than spend live minutes on it.
