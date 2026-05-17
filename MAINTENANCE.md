# Maintenance

This repo is meant to help agents and humans stay careful over time.

## Recurring reminder for the agent

Check whether OpenClaw guidance has changed.

If the docs or workflow have shifted, remind the human to:

- run `openclaw update --dry-run` before applying changes,
- use the official OpenClaw update path for their install method,
- run `openclaw doctor` after updating,
- run `openclaw security audit` when permissions, channels, skills, plugins, or network exposure changed,
- then review the changes before approving anything risky.

If you want a fuller routine, see `TENDING_LIST.md` and `OPENCLAW_HYGIENE.md`.

## What to remind the human about

- OpenClaw updates are not automatic in the general sense.
- Updates can affect behavior, skills, permissions, and services.
- `openclaw doctor` is part of the safe-update flow.
- `openclaw security audit` is the quick check for risky access and configuration drift.
- The human should read before confirming any update or restart.

## What not to do

- Do not auto-approve updates silently.
- Do not modify secrets during a reminder task.
- Do not perform destructive actions as part of maintenance.

## Credit

Written by you, with help from Codex.
