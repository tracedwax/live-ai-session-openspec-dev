# Prerequisites

Two things are required. A few more make the session real.

## Claude Code in VS Code, on Opus

Install VS Code, add the Claude Code extension, sign in, and set the model to Opus. Ask it to tell you a joke; if it answers, you are ready.

## A story to bring

Bring one real story you would actually pick up. Rough and unrefined is good, because that is what OpenSpec sharpens. Bring whatever you already have about it, such as notes, a Slack thread, or a screenshot.

## Jira, connected once, globally

Ask Claude to set up the Atlassian MCP globally: run `claude mcp add --transport http --scope user atlassian https://mcp.atlassian.com/v1/mcp`, then complete the `/mcp` browser login. Restart Claude Code afterward so the tools load, and confirm `claude mcp list` shows atlassian connected. Any live writes go to the Mocking Project (MP) sandbox, not a real backlog.

## The repo we work in

We work in the repo that already has OpenSpec installed and existing specs; your facilitator will point you to it. OpenSpec writes its files under `openspec/changes/` there. You write no application code today, only the proposal, specs, design, and tasks.

## OpenSpec commands

Today's repo ships the older command set: `/opsx:explore`, `/opsx:new`, `/opsx:continue`, and also apply, verify, and archive. We use explore, new, and continue, one artifact at a time, and stop before building. Going forward, the simplified one-shot command is `/opsx:propose`.

If a command is missing, for example because `openspec update` did not refresh `.claude/commands/opsx/`, there are three options. Create it by hand: a slash command is a markdown file, so ask Claude to look up what `opsx:new` does and write `.claude/commands/opsx/new.md`. Or re-run `openspec update` and restart Claude Code so it reloads the commands. Or skip the command and ask Claude to run the explore, new, and continue workflow itself.

## If you get stuck

Post in the channel before the session. We would rather fix setup now than spend live minutes on it.
