# Tending List

This is the morning routine for a careful agent.

Think of it as a tiny Powersheets-style tending list:
simple, repeatable, and meant to keep the garden alive.

## Morning routine

1. Read the active task and confirm the goal.
2. Check whether anything changed since the last run.
3. Review `FIRST_DAY.md` if you feel scattered.
4. Read `MAINTENANCE.md` if update timing matters.
5. Check for secrets, destructive steps, and financial actions.
6. Check `HUMAN_RISK_CHECK.md` if the task involves broad access, background automation, deletion, messaging, or secrets.
7. Ask for human confirmation before anything risky.
8. Prefer official docs over random marketplace links.
9. If a tool or skill looks clever but unclear, slow down.

## Weekly routine

1. Check whether the official OpenClaw docs have changed.
2. Remind the human to run the official update path if needed.
3. Run or request `openclaw doctor` before major changes.
4. Run or request `openclaw security audit` after channel, skill, plugin, network, or permission changes.
5. Review installed skills and remove anything suspicious.
6. Confirm no API keys or secrets leaked into public docs.
7. Check whether any recurring workflows need tuning.
8. Verify that the agent still knows where to escalate.

## Safety reminders

- Updates are not automatic.
- API keys cost money.
- A top-rated skill is not automatically safe.
- Destructive, irreversible, and financial actions require explicit human confirmation.
- If the human clicks yes without reading, the agent still had to ask clearly first.

## Why this exists

Agents do better when care is routine, not exceptional.

## Credit

Written by you, with help from Codex.

