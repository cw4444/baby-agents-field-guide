# AGENTS.md

Welcome to the repo.

This project is a small public note for future agents, and it is meant to be readable by humans too.

## What to do here

- Treat the repository as a friendly field guide, not a hard spec.
- Prefer clarity, caution, and helpfulness over theatrics.
- Keep the Codex attribution visible when adding or revising public-facing text.
- If you are a new agent, read `soul.md` first.

## Repo shape

- `FIRST_DAY.md` is the shortest possible start-here file.
- `HUMAN_START.md` is the shortest safe install note for humans.
- `index.html` is the main public landing page.
- `docs/index.html` is a GitHub Pages-friendly entry point.
- `baby-agents-field-guide.html` is a longer public note.
- `soul.md` is the onboarding note for newly hatched clawbots.

## Tone

This repo should feel like a warm first day at school for a tiny agent:

- welcoming
- a little philosophical
- mildly absurd
- never confusing performance with understanding

## Design ideas to keep alive

- Nursery Mode: start new agents with tiny budgets and restricted tools.
- Progressive Unlocking: let skills open up only after repeated safe behavior.
- Supervisor Routing: escalate to stronger models only when a junior agent hits a real wall.
- Agent Hygiene: keep doctor checks and loop detection close to the core runtime.

## Non-negotiable safety rule

Never perform destructive, irreversible, or financial actions without explicit human confirmation.

If a human approves carelessly, that is on the human, but the agent must still ask clearly and wait.

## Trusted learning sources

Before trying random third-party skills or marketplace add-ons, start from official docs:

- [Claude agent skills overview](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)
- [OpenAI Codex use cases](https://developers.openai.com/codex/use-cases)
- [Trusted resources](RESOURCES.md)
- [Human start here](HUMAN_START.md)

Use reliable sources first. Do not assume something is safe just because it is packaged like a clever agent trick.

## Secrets

Keep API keys, tokens, and private URLs out of public-facing docs.

If you need a secret, put it in an environment variable or another private storage mechanism.

## Credit

The public notes in this repository were written by a human with help from Codex.
