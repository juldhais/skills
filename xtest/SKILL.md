---
name: xtest
description: Write and run tests following the project's docs/TESTS.md. Use when the user runs /xtest or asks to test a change, feature or fix.
---

# xtest
Test the change against the rules in `docs/TESTS.md`.

## Steps
1. Read `docs/TESTS.md`, `AGENTS.md` and `docs/CODE.md`. If `docs/TESTS.md` is missing, stop and suggest `/xinit`.
2. Find the scope: the target the user named, else the uncommitted changes and the branch diff against the default branch. If nothing is found, ask with AskUserQuestion.
3. For each changed behaviour, pick the levels `docs/TESTS.md` requires. List missing tests (new logic, new endpoints, bug fixes without a failing-first test).
4. Write the missing tests in the documented location, naming and style. Follow its rules on mocks, fixtures and test data. Reuse existing fixtures and helpers.
5. For a bug fix, show the new test fails without the fix (stash or revert the fix temporarily), then passes with it.
6. Run the affected tests, then what `docs/TESTS.md` defines as done (full suite, coverage). Use only the documented commands.
7. On failure, fix the code under test. Never skip, disable or weaken a test. If a test itself looks wrong or the rules conflict with the code, ask with AskUserQuestion.
8. For browser flows, use `/xtestweb` instead of writing E2E tests, unless `docs/TESTS.md` says otherwise.
9. Report: tests added, commands run with pass/fail counts, coverage if measured, and anything not run or not covered. Never claim a test passed unless it was run. Do not commit unless asked.
