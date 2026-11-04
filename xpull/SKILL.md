---
name: xpull
description: Pull the latest changes and resolve merge conflicts. Use when the user runs /xpull or asks to pull or merge.
---

# xpull
Pull from the remote, resolve any merge conflicts and commit the merge.

1. Run `git status`. If there are uncommitted changes, ask with AskUserQuestion whether to commit, stash or cancel.
2. Run `git pull`. If there are no conflicts, report the result and stop.
3. For each conflicted file, read both sides and the surrounding code, then resolve it so both intents are kept.
4. If a conflict is unclear (both sides change the same logic, intent cannot be inferred), ask with AskUserQuestion. Show both versions and offer options: keep ours, keep theirs, combine. Never guess.
5. Verify no conflict markers remain, then run the project's build or tests if known (see `docs/CODE.md`).
6. Run `git add` on the resolved files and `git commit` with a one-sentence message (for example "Merge origin/main and resolve conflicts").
7. Never force, reset or discard changes. If something fails, report the error and stop. Do not push unless asked.
