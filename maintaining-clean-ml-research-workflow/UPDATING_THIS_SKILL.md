# How to Update This Skill

As you iterate on your research workflow, you will likely want to change how this skill behaves. Here is a guide on what to update for common changes.

## 1. You want to change the folder structure or file names
- **Update**: `SKILL.md` (Instructions section G: Repo Hygiene).
- **Update**: `resources/WORKLOG_TEMPLATE.md` (File Registry section).

## 2. You want to capture new metrics or artifacts in runs
- **Update**: `resources/RUN_LOG_TEMPLATE.md`.
- **Update**: `SKILL.md` (Instructions section E: Reproducibility).

## 3. You want to change the "File Card" format
- **Update**: `resources/FILE_CARD_TEMPLATE.md`.
- **Update**: `SKILL.md` (Instructions section D: File Cards).

## 4. You want to add a new step to the workflow (e.g., Code Review)
- **Update**: `SKILL.md` (Workflow section).
- **Update**: `resources/CHECKLIST_TEMPLATE.md`.

## 5. The agent isn't following a rule strict enough
- **Update**: `SKILL.md` (Instructions section). Add a capitalized "MUST" or "ALWAYS" constraint.
- **Example**: Change "Update the worklog" to "ALWAYS update the worklog BEFORE creating any code files."

## 6. How to reload changes
After modifying these files, the agent should pick up the changes in the next task/session. No restart is usually required, but you can explicitly ask the agent to "reread the skill instructions" if needed.
