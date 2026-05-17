# OpenClaw Hygiene

This is the plain-English safety note for humans who installed OpenClaw because somebody made it look easy.

OpenClaw can be useful. It is also an always-on assistant that can connect to real messaging accounts, local files, browser sessions, shell commands, tools, plugins, and services. Treat it like a small server you invited into your house, not like a toy website.

## First rule

Use the official OpenClaw docs and repo first:

- [OpenClaw GitHub repo](https://github.com/openclaw/openclaw)
- [OpenClaw getting started](https://docs.openclaw.ai/start/getting-started)
- [OpenClaw updating](https://docs.openclaw.ai/install/updating)
- [OpenClaw security](https://docs.openclaw.ai/gateway/security)
- [OpenClaw sandboxing](https://docs.openclaw.ai/gateway/sandboxing)

Do not copy-paste a one-line install from a social post unless you know exactly what it downloads, what it runs, and what permissions it asks for.

## The three commands to know

These are the boring commands that keep things safer:

```sh
openclaw update --dry-run
openclaw update
openclaw doctor
```

Use `openclaw update --dry-run` when you want to preview an update before applying it. After updating, run `openclaw doctor`, restart the gateway if the docs tell you to, then check `openclaw health`.

OpenClaw also has a security audit:

```sh
openclaw security audit
openclaw security audit --deep
```

If the audit warns about open DMs, public network exposure, browser control, file permissions, plugins, or broad tool access, slow down and read the finding before clicking through.

## Permission words that mean pay attention

If an installer, agent, skill, plugin, or copied command mentions any of these, stop and read:

- `sudo`
- `curl ... | bash`
- `npm install -g`
- root-owned global installs
- launch agents, systemd services, daemons, or auto-start services
- broad filesystem access
- shell, command, process, browser, cron, node, gateway, or remote-control tools
- messaging accounts, personal email, Apple, Google, Slack, Discord, WhatsApp, Telegram, Signal, or iMessage
- API keys, OAuth, tokens, passwords, cookies, or browser profiles

None of these are automatically bad. They are just the point where a human should understand what is being granted.

## Safer default posture

Start small:

1. Keep the gateway local-only unless you know why it needs remote access.
2. Use pairing or allowlists for DMs.
3. Require mentions in group chats.
4. Keep shared bots away from personal accounts and personal browser profiles.
5. Do not give a public or group-accessible bot broad filesystem or shell access.
6. Use sandboxing or separate OS users/hosts when people, accounts, or projects should not share trust.
7. Review installed skills and plugins before enabling them.

OpenClaw's security docs describe the personal-assistant trust model: one trusted operator boundary per gateway. If several people can message one tool-enabled agent, they can steer the same permission set. That is fine for a trusted household or team only when the tools and accounts match that trust level.

## Provider billing boundaries

Before choosing a model provider, check whether OpenClaw is using a subscription login, a monthly credit, extra usage, or a direct API key.

Provider rules differ:

- OpenAI/Codex may support ChatGPT subscription OAuth in OpenClaw-style external workflows, while OpenAI API keys remain usage-based.
- Claude subscription access, Claude Code interactive use, Claude Agent SDK use, `claude -p`, GitHub Actions, third-party harnesses, extra usage, and Anthropic API keys may draw from different buckets.

Do not tell the human "your subscription covers this" unless the current provider docs say that exact route is covered. If there is any doubt, inspect the configured provider, account type, API keys, OAuth login, and auto-reload or extra-usage settings before starting long-running agent work.

## Updates

Updates matter because they can change behavior, permissions, services, skills, and security checks.

Recommended routine:

1. Read the official update notes or docs.
2. Run `openclaw update --dry-run`.
3. Apply the update only when the human understands what is changing.
4. Run `openclaw doctor`.
5. Run `openclaw security audit`.
6. Restart and verify with `openclaw health`.

Do not silently auto-approve updates for a distracted human.

## What an agent should tell its human

Say this plainly:

> OpenClaw is useful, but it can touch real accounts and real files. Before we install, update, expose it to the network, add a skill, or allow shell/browser access, please read the command and confirm you understand what it can do.

Then wait.

## Red flags

Pause and ask for a stronger review if:

- a command pipes a download directly into a shell
- the install asks for `sudo` but does not explain why
- a bot can be messaged by strangers or a whole group chat
- an agent has shell access and personal-account access at the same time
- a plugin or skill comes from an unknown source
- logs, screenshots, configs, or docs contain secrets
- the gateway is exposed to the internet without a clear authentication and firewall story

## Non-negotiable rule

Never perform destructive, irreversible, financial, or broad-permission actions without explicit human confirmation.

If the human approves carelessly, that is still the human's mistake, but the agent must ask clearly and wait.

## Credit

Written by you, with help from Codex.
