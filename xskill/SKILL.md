---
name: xskill
description: Create a new skill. Use when the user runs /xskill or asks to make a skill.
---

# xskill
Create a new skill in `~/.claude/skills/<name>/SKILL.md`.

## Steps
1. Use AskUserQuestion (one call, only what is missing): name, purpose, when it should trigger. Offer suggested options where possible.
2. If the skill already exists, read it and improve it instead of overwriting.
3. Write `SKILL.md` with this frontmatter:
   ```
   ---
   name: <lowercase-hyphen-name>
   description: <what it does>. Use when <trigger>.
   ---
   ```
4. Keep the description to one short sentence plus the trigger. No lists, no detail.
5. Keep the body short: a one-line purpose, then numbered steps. Rules, not prose.
6. Add `templates/` or other files only if the skill needs them.
7. Report the path created. Do not commit unless asked.
