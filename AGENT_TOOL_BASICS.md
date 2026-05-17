# Agent Tool Basics

This is the normal-human version of the difference between common coding agents.

The short version: ChatGPT, Claude, Codex, Claude Code, and OpenClaw are not the same kind of thing. Some mostly talk. Some can edit files. Some can run commands. Some can connect to GitHub, browsers, terminals, messaging apps, or external tools.

Before granting access, ask what the agent can read, what it can change, what it can run, and whether it keeps working after you walk away.

## Codex

Codex is OpenAI's coding agent family. It can work in different places, including cloud tasks, IDE-style flows, and a local CLI.

Useful default understanding:

- Codex can read, modify, and run code when you give it the right access.
- Codex cloud tasks run in sandboxed cloud containers for individual tasks.
- Codex cloud can work in the background and may connect to GitHub repositories you authorize.
- Codex CLI runs locally in your terminal and has approval modes.
- The safer local default is to let Codex read and propose before it writes or runs commands.
- Full-auto/local command modes deserve extra attention, even when sandboxed.
- Codex cloud internet access is a security choice, not a casual toggle.

Human checklist:

1. Use Ask or read-only mode when learning a repo.
2. Use Code/edit modes only when the task and files are clear.
3. Keep GitHub access scoped to the repos Codex actually needs.
4. Review diffs before merging or pushing.
5. Avoid putting secrets in prompts, logs, screenshots, or public issues.
6. Prefer OAuth or sign-in flows over pasting raw API keys.
7. Use MFA on accounts that can reach code or billing.
8. Treat network access as a permission that can expose code, secrets, or licensing risk.

Official starting points:

- [OpenAI Codex cloud docs](https://platform.openai.com/docs/codex)
- [OpenAI Codex use cases](https://developers.openai.com/codex/explore/)
- [OpenAI Codex CLI getting started](https://help.openai.com/en/articles/11096431)
- [OpenAI Codex CLI sign-in](https://help.openai.com/en/articles/11381614-api-codex-cli-and-sign-in-with-chatgpt)
- [OpenAI Codex agent internet access](https://platform.openai.com/docs/codex/agent-network)

## Claude Code

Claude Code is Anthropic's agentic coding tool that lives in the terminal.

Useful default understanding:

- Claude Code starts from a permission-based model.
- It can read code, propose changes, edit files, run commands, and connect to tools when allowed.
- It asks for permission before actions outside the safe default.
- Project settings, local settings, memory files, hooks, and MCP servers can change what Claude Code can see or do.
- MCP servers are powerful tool connections. Anthropic does not manage or audit every MCP server.
- Project memory files such as `CLAUDE.md` can be useful, but they should not contain secrets.

Human checklist:

1. Use read-only exploration first in unfamiliar repos.
2. Check `/permissions` when the project is sensitive.
3. Deny reads of `.env`, secrets folders, credentials, and private config files.
4. Review `.claude/settings.json`, `.claude/settings.local.json`, and `.mcp.json` before trusting a project.
5. Treat hooks as code that runs because the agent is doing something.
6. Use trusted MCP servers and keep permissions narrow.
7. Use devcontainers, VMs, or separate users for risky code or untrusted dependencies.
8. Review changes to critical files before approving commits, pushes, deploys, or migrations.

Official starting points:

- [Claude Code overview](https://docs.anthropic.com/en/docs/claude-code/overview)
- [Claude Code getting started](https://docs.anthropic.com/en/docs/claude-code/getting-started)
- [Claude Code security](https://docs.anthropic.com/en/docs/claude-code/security)
- [Claude Code settings](https://docs.anthropic.com/en/docs/claude-code/settings)
- [Claude Code memory](https://docs.anthropic.com/en/docs/claude-code/memory)
- [Claude Code MCP](https://docs.anthropic.com/en/docs/claude-code/mcp)

## OpenClaw

OpenClaw is different again. In this repo, treat it as a broader always-on agent gateway rather than just a coding assistant.

Start with `OPENCLAW_HYGIENE.md` before installing, updating, exposing, or granting permissions to OpenClaw.

## The common safety pattern

For any agent tool:

1. Start read-only.
2. Keep secrets out of prompts and docs.
3. Ask what the tool can access.
4. Review commands before approving them.
5. Review diffs before accepting changes.
6. Avoid broad filesystem, shell, browser, messaging, and network access until needed.
7. Prefer reversible steps.
8. Keep human confirmation for destructive, irreversible, financial, security-sensitive, or public actions.

## Useful sentence

If a human asks "can you just set it all up?", say:

> I can help, but these tools can read files, edit code, run commands, and sometimes connect to real accounts. I will start by inspecting only, then explain what access is needed before changing anything.

## Credit

Written by you, with help from Codex.
