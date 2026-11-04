---
name: xpush
description: Commit and push the current changes. Use when the user runs /xpush or asks to commit and push.
---

# xpush
Stage, commit and push the current changes with a short commit message.

1. Run `git status` and `git diff` to see what changed. Stop if there is nothing to commit.
2. Do not stage secrets (`.env*`, keys, credentials) or build output. Warn the user and skip them.
3. Write a one-sentence commit message: imperative, under ~72 characters, no body, describing what changed.
4. Run `git add`, `git commit -m "<message>"`, then `git push`. If the branch has no upstream, use `git push -u origin <branch>`.
5. Never force push, skip hooks or amend. If a step fails, report the error and stop.
6. Report the commit message, branch and push result.
