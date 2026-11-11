---
name: xinit
description: Initialize or refresh a project's agent docs (AGENTS.md, docs/CODE.md, docs/DESIGN.md, docs/STATUS.md, docs/ISSUES.md) from templates. Use when the user runs /xinit or asks to set up or standardize project docs for AI agents.
---

# xinit
Create or update the agent docs from `templates/` (next to this file):

| File | Purpose |
|---|---|
| `AGENTS.md` | Entry point: summary, principles, workflow, links (max ~40 lines) |
| `docs/CODE.md` | Code standard, structure, validation commands |
| `docs/DESIGN.md` | UI design standard (skip if the project has no UI) |
| `docs/STATUS.md` | Development progress |
| `docs/ISSUES.md` | Issue tracker (open and done issues) |

## Steps
1. Inspect the repo (read-only): root, package/solution files, existing `AGENTS.md`, `CLAUDE.md`, `README`, `docs/`, test/lint commands.
2. Ask the user only for what the repo cannot tell (stack, UI framework, goal), in one batch.
3. Write each file from its template. `AGENTS.md` must link every other doc in its References. Fill placeholders with facts from the repo, delete sections that do not apply, and mark unknowns `TODO(user)`.
4. If docs already exist, keep their rules and move them to the right file. Tell the user about any rule you drop. Do not delete user files. Keep existing issues in `docs/ISSUES.md`.
5. Keep it short: rules, not prose. Link between files instead of repeating.
6. Verify that linked paths exist and run the listed commands (or mark them unverified).
7. Report files changed, `TODO(user)` items and unverified commands. Do not commit unless asked.
