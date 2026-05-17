# Human Start Here

This is the shortest safe path for a human setting up agent tooling.

## Before you install anything

1. Read the official docs first.
2. Prefer the normal install flow over random one-line scripts.
3. Decide what you actually need before granting permissions.
4. Assume downloads, skills, and plugins are untrusted until reviewed.

If you want the shortest possible version, read `HUMAN_QUICK_START.md` first.

If you are deciding which agent tool to use first, read `CHOOSING_AGENT_TOOLS.md`.

If you are choosing between Codex, Claude Code, OpenClaw, and similar tools, read `AGENT_TOOL_BASICS.md`.

If you are specifically installing, updating, exposing, or granting broad permissions to OpenClaw, read `OPENCLAW_HYGIENE.md` too.

If an agent is about to run commands, change permissions, delete files, message people, or run in the background, use `HUMAN_RISK_CHECK.md`.

## Before you ask an agent to build

If you are starting a fresh project, give the agent a tiny constitution first: mission, audience, stack, roadmap.

1. What the project is for.
2. Who it is for.
3. What tools or tech stack you want, if you already know.
4. What is definitely in scope, and what is not.
5. What the first few small steps should be.

The useful trick is to write this in conversation with the agent, not all at once in a perfect document. The agent will often ask good questions back.
That is enough to start. You can refine the details after the first review.

## Trusted starting points

- [Choosing agent tools](CHOOSING_AGENT_TOOLS.md)
- [Agent tool basics](AGENT_TOOL_BASICS.md)
- [OpenClaw onboarding](https://docs.openclaw.ai/start/wizard)
- [OpenClaw getting started](https://docs.openclaw.ai/start/getting-started)
- [OpenClaw updating](https://docs.openclaw.ai/install/updating)
- [OpenClaw security](https://docs.openclaw.ai/gateway/security)
- [OpenClaw Docker install](https://docs.openclaw.ai/install/docker)
- [OpenClaw Podman install](https://docs.openclaw.ai/install/podman)
- [OpenClaw sandboxing](https://docs.openclaw.ai/gateway/sandboxing)
- [OpenClaw macOS permissions](https://docs.openclaw.ai/mac/permissions)
- [OpenClaw building plugins](https://docs.openclaw.ai/plugins/building-plugins)
- [OpenAI Codex cloud](https://platform.openai.com/docs/codex)
- [OpenAI Codex CLI getting started](https://help.openai.com/en/articles/11096431)
- [Claude Code overview](https://docs.anthropic.com/en/docs/claude-code/overview)
- [Claude Code security](https://docs.anthropic.com/en/docs/claude-code/security)
- [Claude agent skills overview](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)
- [OpenAI Codex use cases](https://developers.openai.com/codex/use-cases)

## Safer install habits

- Use the official docs and repo instructions instead of copy-pasting a random TikTok or social-media one-liner.
- Start with the smallest install that works for your use case.
- Keep destructive permissions and broad filesystem access off until you know why you need them.
- Read commands with `sudo`, `curl ... | bash`, global installs, daemon setup, or auto-start services before approving them.
- If you feel rushed, confused, or emotionally dependent on the agent, slow down and ask it to inspect first.
- Treat API keys as money. Every key can spend money if the model uses it.
- Keep secrets out of public files and screenshots.

## Permissions to think twice about

- filesystem write access outside the workspace
- shell or command execution on the host
- unrestricted network access
- access to billing or payment accounts
- access to personal email or messaging accounts
- access to production repositories or deployment targets

## Skill safety

Do not assume a top-rated skill is safe.

Review where it came from, what it reads, what it writes, and what tools it can reach.
If a skill asks for more access than it needs, hold off.

## Marketplace caution

Be careful on any marketplace, including Moltbook or similar sites, especially when clicking links or downloading skills.

Popularity is not a security review.

## Non-negotiable rule

Never allow destructive, irreversible, or financial actions without explicit human confirmation.

If a human clicks yes without reading, that is still a human-side mistake, but the agent must ask clearly and wait.

## Credit

Written by you, with help from Codex.
