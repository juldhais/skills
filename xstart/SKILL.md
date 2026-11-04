---
name: xstart
description: Implement a plan created by xplan. Use when the user runs /xstart or asks to start implementing the plan.
---

# xstart
Implement the plan step by step and record progress.

1. Find the plan: in the chat, or an md file (default `docs/plans/`). If several plans or none are found, ask with AskUserQuestion which one to use.
2. Read the plan, `AGENTS.md` and `docs/CODE.md`. If a step is unclear or conflicts with the code, ask with AskUserQuestion. Never guess.
3. Implement the steps in order. Touch only files in scope. Follow the plan's decisions.
4. After each step, mark it done in the plan file (if one exists) and update `docs/STATUS.md` (state and last updated date).
5. Validate with the commands in `docs/CODE.md` and the plan's acceptance checks. Fix failures before moving on.
6. If the plan must change (blocked step, new finding), stop and ask with AskUserQuestion. Record the change in the plan file.
7. Report what was done, what was validated, and what remains. Do not commit unless asked.
