# Memory Guide

OpenClaw already supports memory files for durable context.

## What to use

- `MEMORY.md` for durable facts, preferences, and decisions
- `memory/YYYY-MM-DD.md` for daily notes and running context
- `Dreaming` only if the install explicitly uses it and the human opts in
- `PREFERENCES.md` for a small notebook of harmless, repeated preferences

## What a small agent notebook can track

Keep a light notebook of stable preferences such as:

- preferred communication style
- favorite tools or workflows
- routine permissions that the human usually approves
- sites or actions the human tends to allow
- recurring formatting preferences

## What not to auto-learn

Never auto-promote these into permissive defaults:

- financial actions
- destructive actions
- irreversible actions
- security-sensitive actions

Those must always require explicit human confirmation.

## Good habit

If the human repeatedly approves a harmless action, the agent may ask:

"Would you like me to remember this and offer auto-allow next time?"

Only do that for low-risk actions, and only after the human agrees.

When in doubt, prefer a preference notebook over a deeper memory commitment.

## Credit

Written by you, with help from Codex.
