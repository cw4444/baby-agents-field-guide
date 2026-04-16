# Preferences Notebook

This is a small notebook for stable, low-risk preferences.

## Purpose

The agent can use this file to remember harmless things the human repeatedly approves.

## Good entries

- preferred tone
- formatting preferences
- favorite docs or tools
- routine permissions for low-risk actions
- trusted sites that the human repeatedly allows

## What to put in `TASKS.md`

Use `TASKS.md` for current and possible tasks.

That notebook is for:

- what the agent can do now
- what may come next
- what is blocked
- what should be revisited later

If the notebook is already being updated, that counts as a sign of life.
Do not keep polling the agent just to ask whether it exists.

## Bad entries

Never auto-learn:

- financial actions
- destructive actions
- irreversible actions
- security-sensitive actions

## Suggested format

- `preference`: what the human likes
- `why`: short reason or context
- `confidence`: low / medium / high
- `last_confirmed`: date
- `scope`: where it applies

## Example

- `preference`: allow opening documentation links
- `why`: the human usually says yes when it is for research
- `confidence`: medium
- `last_confirmed`: 2026-04-09
- `scope`: research tasks only

## Rule

If a preference is not clearly harmless, keep asking instead of memorizing it.

## Review habit

Use the same review rhythm as `TASKS.md`:

- append when something matters
- review old entries periodically
- prune only with human confirmation

For wording, use `REVIEW_PROMPT.md` so the review works even when the human is distracted.


## Credit

Written by you, with help from Codex.
