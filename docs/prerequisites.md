# Prerequisites

Two required things, and a few that make the hour real.

## Required: Claude Code in VS Code (on Opus)

Install **VS Code**, add the **Claude Code extension**, sign in, and set the model to **Opus**. Ask it *"tell me a joke"* — if you get one back, you're ready.

## Required: a story to bring

Bring **one real story** you'd actually pick up. Rough is fine — unrefined is the point; that's what OpenSpec sharpens. Bring whatever you have about it too (notes, a Slack thread, a screenshot).

## Connect Jira (the MCP) — once, globally

> *"Set up the Atlassian MCP globally: run `claude mcp add --transport http --scope user atlassian https://mcp.atlassian.com/v1/mcp`, then walk me through the `/mcp` browser login."*

**Restart Claude Code after connecting** so the tools load; confirm `claude mcp list` shows `atlassian … ✓ Connected`. Any live writes go to the **Mocking Project (`MP`)** sandbox, not a real backlog.

## OpenSpec

The flow uses `/opsx:propose` (and `/opsx:apply`). If your repo doesn't have it:
- Run `openspec init` in your repo (`npm i -g @fission-ai/openspec` first if needed), **or**
- Tell Claude: *"Look up what OpenSpec's opsx propose does and run that workflow yourself."*

## A repo to work in

Open Claude in a repo you can write to — your own working repo is fine. OpenSpec writes `openspec/changes/<change>/` files here (proposal, specs, design, tasks). You write **no application code** today unless you reach the build stretch.

> **Stuck on setup?** Post in the channel before the session — we'd rather fix it now than spend live minutes on it.
