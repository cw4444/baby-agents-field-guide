# Tasks Notebook

This is the place for ongoing or possible tasks.

If the notebook is being updated, the agent is already alive enough to know what to do next.
No separate heartbeat loop is needed just to ask whether there is work.

## Purpose

Keep a short list of:

- things the agent can do now
- things the human may want later
- tasks waiting on a reply
- small maintenance items

## Good entries

- current task
- next likely task
- blocked on human
- blocked on external docs
- reminder to revisit a safe low-risk action

This follows an append-and-review pattern:

- append new items as they appear
- review the oldest items on a schedule
- keep what still matters
- clear only what the human agrees is no longer needed

## Bad entries

- secrets
- destructive tasks
- financial tasks
- giant speculative plans with no owner

## Suggested format

- `task`: what it is
- `status`: now / later / blocked / done
- `why`: short reason
- `next_step`: what would move it forward
- `last_seen`: date

## Example

- `task`: check whether OpenClaw docs changed
- `status`: now
- `why`: maintenance reminder
- `next_step`: review docs and update the human if needed
- `last_seen`: 2026-04-09

## Rule

If the notebook already has a clear next action, take it instead of looping around looking for something new to invent.

## Monthly review suggestion

Once a month, show the human the oldest five items in this notebook and ask:

"Are these still relevant?"

If the human says they are not needed, clear them.
If the items are still useful, keep them or move them upward.

## Credit

Written by you, with help from Codex.
