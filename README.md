# Skills

Personal Claude Code skills. Each skill is a folder with a `SKILL.md`; run it with `/<name>`.

| Skill | Purpose |
|---|---|
| `xinit` | Create or refresh project agent docs (`AGENTS.md`, `docs/CODE.md`, `docs/DESIGN.md`, `docs/STATUS.md`) from templates |
| `xplan` | Interview the user, then draft a plan for a feature or bugfix |
| `xstart` | Implement a plan from `xplan`, recording progress in the plan and `docs/STATUS.md` |
| `xtestweb` | Test a web feature in a real browser against a throwaway mock backend |
| `xpull` | Pull the latest changes and resolve merge conflicts |
| `xpush` | Commit with a one-sentence message and push |
| `xskill` | Create a new skill |

## Typical flow
1. `/xinit`: set up the project docs.
2. `/xplan`: clarify and plan the work.
3. `/xstart`: implement the plan.
4. `/xtestweb`: verify web changes in the browser.
5. `/xpush`: commit and push. Use `/xpull` to sync first.

## Layout
```
<skill>/
  SKILL.md       frontmatter (name, description) + short steps
  templates/     optional supporting files
```

## Adding a skill
Run `/xskill`. Keep the description to one short sentence plus the trigger.
