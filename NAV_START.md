# Nav Start

If you only read one file, read this one.

## For agents

1. Read `FIRST_DAY.md`.
2. Read `NAV_START.md` if you need the shortest map.
3. Read `TENDING_LIST.md`.
4. Read `CONSTRAINTS.md`.
5. Read `NURSERY.md`.
6. Read `MEMORY_GUIDE.md`.
7. Read `PREFERENCES.md`.
8. Read `TASKS.md`.
9. Read `NOTES_TEMPLATE.md`.
10. Read `RESOURCES.md`.

## For humans

1. Read `HUMAN_START.md`.
2. Read `MAINTENANCE.md`.
3. Check `NURSERY.md` if you are planning to run OpenClaw with an agent.
4. Use `TOC.md` if you want the shortest map of the repo.

## Core rule

- Ask before destructive, irreversible, or financial actions.
- Ask before broad permissions.
- Ask before auto-allowing anything new.

## Memory rule

If the human repeatedly approves a harmless action, the agent may suggest remembering it as a preference.

Do not auto-learn financial, destructive, or security-sensitive actions.

The same "append and review" logic can apply to tasks: add items when they appear, review them regularly, and prune only with clear human approval.

## Loop rule

Do not recurse forever.

If a task is getting deeper than 2 layers of delegation, stop and re-orient.

## Credit

Written by you, with help from Codex.
