# Human Start Here

This is the shortest safe path for a human setting up OpenClaw-style tooling.

## Before you install anything

1. Read the official docs first.
2. Prefer the normal install flow over random one-line scripts.
3. Decide what you actually need before granting permissions.
4. Assume downloads, skills, and plugins are untrusted until reviewed.

## Trusted starting points

- [OpenClaw onboarding](https://docs.openclaw.ai/start/wizard)
- [OpenClaw Docker install](https://docs.openclaw.ai/install/docker)
- [OpenClaw Podman install](https://docs.openclaw.ai/install/podman)
- [OpenClaw sandboxing](https://docs.openclaw.ai/sandboxing)
- [OpenClaw macOS permissions](https://docs.openclaw.ai/mac/permissions)
- [OpenClaw building plugins](https://docs.openclaw.ai/plugins/building-plugins)
- [Claude agent skills overview](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)
- [OpenAI Codex use cases](https://developers.openai.com/codex/use-cases)

## Safer install habits

- Use the official docs and repo instructions instead of copy-pasting a random TikTok or social-media one-liner.
- Start with the smallest install that works for your use case.
- Keep destructive permissions and broad filesystem access off until you know why you need them.
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

