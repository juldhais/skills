---
name: xplan
description: Draft a plan for a feature or bugfix. Use when the user runs /xplan or asks to plan a feature or fix.
---

# xplan
Interview the user until nothing is ambiguous, then draft the plan. Do not write code.

## Steps
1. Read the request and the relevant code and docs (`AGENTS.md`, `docs/`) first. Never ask what the repo can answer.
2. Grill the user with AskUserQuestion, 1-4 questions per call, repeating until every point is clear. Offer concrete options and put your recommendation first.
   - **Feature:** goal, users, scope and non-goals, behavior, edge cases, errors, permissions, data/schema, UI, dependencies, acceptance criteria.
   - **Bugfix:** expected vs actual, steps to reproduce, frequency, environment, when it started, impact, suspected cause, constraints on the fix.
3. Never assume. If an answer is vague, contradicts earlier answers or opens a new question, ask again. Do not stop at the first round.
4. Before drafting, summarize your understanding in a few lines and confirm it with AskUserQuestion.
5. Draft the plan:
   - Goal and non-goals
   - Decisions made (from the interview)
   - Steps: files/areas to change, in order
   - Validation: commands and acceptance checks
   - Risks and open items
   - Suggested model and effort level for implementation (for example Sonnet / medium for routine changes, Opus / high for complex or risky ones), with a one-line reason
6. Ask where to save the plan (suggest `docs/plans/<name>.md`, or chat only). Ask for approval before saving.
7. Do not start implementing unless asked.
