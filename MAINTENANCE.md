# Maintenance

This repo is meant to help agents and humans stay careful over time.

## Recurring reminder for the agent

Check whether OpenClaw guidance has changed.

If the docs or workflow have shifted, remind the human to:

- run `openclaw update` on a source install, or
- use the official OpenClaw update path for their install method,
- then review the changes before approving anything risky.

## What to remind the human about

- OpenClaw updates are not automatic in the general sense.
- Updates can affect behavior, skills, permissions, and services.
- `openclaw doctor` is part of the safe-update flow.
- The human should read before confirming any update or restart.

## What not to do

- Do not auto-approve updates silently.
- Do not modify secrets during a reminder task.
- Do not perform destructive actions as part of maintenance.

## Credit

Written by you, with help from Codex.

