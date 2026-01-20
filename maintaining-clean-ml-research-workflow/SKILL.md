---
name: maintaining-clean-ml-research-workflow
description: Managing ML research and engineering workflows. Use when the user asks to "start a new research project", "refactor for cleanliness", or mentions "clean workflow" or "iterative research".
---

# Maintaining Clean ML/Research Workflow

## When to use this skill
- When starting a new data science or ML research project/repo.
- When cloning an existing repo to augment/modify it.
- When the user asks to "clean up" or "refactor" a messy research repo.
- When building iterative pipelines or multi-agent workflows.

## Workflow
1.  **Initialize/Update Worklog**: Ensure `docs/WORKLOG.md` exists and is up-to-date. This is the SINGLE SOURCE OF TRUTH.
2.  **System Flow Check**: Ensure the high-level system flow is documented (either in `docs/SYSTEM_FLOW.md` or a section in WORKLOG).
3.  **Plan Changes**: Create a checklist in `docs/WORKLOG.md` before writing code.
4.  **Execute & Document**:
    - Update code.
    - Update/Create "File Card" in `docs/WORKLOG.md` for *every* modified .py file.
    - Update Per-File Logic Diagrams in the file comments.
5.  **Log Run**: If running an experiment, save artifacts to `runs/<run_id>/` and add an entry to the Run Index in `docs/WORKLOG.md`.
6.  **Verify & Cleanup**: Check for file sprawl. Delete unused files. Verify `README.md` mirrors the current state.

## Instructions

### A. Single Source of Truth (`docs/WORKLOG.md`)
- **NEVER** create scattered note files (e.g., `notes.txt`, `plan_v2.md`).
- **ALWAYS** write all plans, logic explanations, file registries, and run logs into `docs/WORKLOG.md`.
- Use the [WORKLOG_TEMPLATE](resources/WORKLOG_TEMPLATE.md) for structure.

### B. System Flow Documentation
- Before significant changes, update the "System Flow" section.
- Describe the pipeline end-to-end: Inputs -> Process -> Outputs.
- Use a Mermaid diagram if possible, or a clear text-based flow.

### C. Per-File Logic Diagrams
- In **EVERY** Python file you touch, maintain a block comment at the top (or class/main level) with a "Logic Flow" section.
- Format:
  ```python
  """
  Purpose: [One line summary]
  
  Logic Flow:
  [Input] -> [Step 1] -> [Condition?] -> [Step 2] -> [Output]
  
  [DIAGRAM PROMPT: Create a mermaid flowchart showing inputs, main processing steps, distinct branches, and outputs for this file.]
  """
  ```
- **UPDATE** this whenever the logic changes.

### D. File Cards
- In `docs/WORKLOG.md`, under the "File Registry" section, maintain a card for every file using [FILE_CARD_TEMPLATE](resources/FILE_CARD_TEMPLATE.md).
- Must include: Purpose, Inputs, Outputs, Diagram Prompt, Call Sites, Validation.

### E. Reproducibility & Run Logging
- **ALWAYS** save runs to `runs/<run_id>/`.
- Save:
    - Command executed.
    - `logs.txt` (stdout/stderr).
    - `config.json` (parameters).
    - `env_snapshot.txt` (pip freeze).
- Add an entry to "Run Index" in `docs/WORKLOG.md` linking to the run folder.

### F. Change Tracking
- In `docs/WORKLOG.md`, under "Change Log", record "Before -> After" for significant logic changes.
- Explain *why* it changed and *evidence* that the new version works.

### G. Repo Hygiene
- **Strictly** limit root-level files.
- Allowed root files: `README.md`, `.gitignore`, `requirements.txt`, `setup.py`.
- Source code in `src/` or specific package folders.
- Docs in `docs/`.
- Runs in `runs/`.
- **PROPOSE DELETION** of any file not in the "File Registry".

### H. Code Quality
- Variable/Function names must be self-explanatory (no `x`, `df2`).
- Public functions require docstrings.
- Comments must explain *why*, not just *what*.

## Resources
- [Worklog Template](resources/WORKLOG_TEMPLATE.md)
- [File Card Template](resources/FILE_CARD_TEMPLATE.md)
- [Run Log Template](resources/RUN_LOG_TEMPLATE.md)
- [Checklist Template](resources/CHECKLIST_TEMPLATE.md)
- [System Flow Template](resources/SYSTEM_FLOW_TEMPLATE.md)
