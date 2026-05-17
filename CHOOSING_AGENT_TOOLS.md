# Choosing Agent Tools

This is the practical version of "which agent should a normal human start with?"

Default recommendation: use the most official, bounded tool that can do the job.

An agent that helps inside a clear workspace is one safety class. An always-on gateway that can reach messages, files, browsers, shell commands, accounts, plugins, and schedules is a different safety class.

## Start here

For most normal humans, start with:

- Codex for code, repositories, documentation, data work, research packages, GitHub tasks, app builds, and bounded automations.
- Claude Code for terminal-based coding work when the human understands the project folder, permissions, and command approvals.
- Claude Cowork for non-developer knowledge work when the human wants Claude Desktop to handle multi-step admin, files, research, reports, and scheduled tasks.

Reach for OpenClaw-style gateways only when the human understands:

- what accounts the gateway can reach
- what files it can read and write
- whether it can run shell commands
- whether it can message people
- whether it can run after the human walks away
- whether it uses subscription limits, credits, extra usage, or API keys
- how to update, pause, audit, and remove it

## Why bounded tools first

Codex, Claude Code, and Claude Cowork are still powerful. They can touch real files, run commands, connect to tools, and spend money through usage-based services.

The difference is that they are vendor-supported products with clearer approval flows, documented security models, official update paths, and narrower starting contexts.

That does not make them risk-free. It does make them a better first step for many humans than installing an always-on local agent gateway from a short social-media command.

Plain-English rule:

> A one-line install is not an operational security model.

## Codex is often the first stop

Codex is a good first stop when the work is bounded:

- inspect this repo
- explain this codebase
- clean up these docs
- build a small app
- make a branch or pull request
- analyze this dataset
- turn these notes into a structured artifact
- run tests and report what changed

Use read-only or ask mode first when the human is unsure. Use edit or code mode once the task, files, and expected output are clear.

Codex is increasingly useful beyond code, but the same guardrails apply: check what it can access, review diffs and outputs, and do not hand it broad permissions just because the task sounds harmless.

## Claude Code and Claude Cowork

Claude Code is closer to a terminal coding assistant. It is useful when the human or agent knows where the project lives and can review file edits, commands, permissions, settings, and MCP servers.

Claude Cowork is aimed more at everyday knowledge work inside Claude Desktop. Anthropic describes it as using the same agentic architecture as Claude Code, but for work beyond coding: formatted documents, organized files, synthesized research, reports, recurring tasks, and similar admin work.

Cowork is not "just chat." It can work with local files, connected tools, plugins, scheduled tasks, internet access, and real outputs on the human's computer. That means it needs the same caution around files, deletion, schedules, connectors, billing, and dependency loops.

## OpenClaw-style gateways

OpenClaw may be the right tool when the human genuinely needs a broader personal-agent gateway across channels, models, tools, plugins, and background workflows.

That is a higher-risk setup than "help me edit this repo."

Before using it, read:

- `OPENCLAW_HYGIENE.md`
- `HUMAN_RISK_CHECK.md`
- `AGENT_TOOL_BASICS.md`

If the human does not know what a daemon, API key, OAuth scope, shell command, scheduled task, or provider billing route is, start with a bounded tool instead.

## Simple decision tree

1. Is this one repo, folder, dataset, document, or project?
   Start with Codex, Claude Code, or Claude Cowork.

2. Does the task require background operation, messaging channels, cross-app routing, or always-on behavior?
   Consider OpenClaw only after checking permissions, billing, updates, and audit paths.

3. Does the human seem confused, rushed, or over-trusting?
   Use `HUMAN_RISK_CHECK.md` and inspect before acting.

4. Is money, deletion, accounts, production, messaging, health, finance, or legal impact involved?
   Stop and ask for explicit confirmation.

## Credit

Written by you, with help from Codex.
