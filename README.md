# Antigravity Skills Repository

This repository stores skills for the Antigravity agent.

## Structure
- **`maintaining-clean-ml-research-workflow/`**: A specialized skill for managing ML/Data Science research projects.
- **`skills/`**: A collection of general-purpose skills:
    - `error_handling.md`
    - `Ultimate-Debugger`
    - `superpowers`
    - `antigravity-skill-creator.md`

## How to use `maintaining-clean-ml-research-workflow`
This skill is designed to keep your machine learning research organized.

### Installation
1. Ensure this folder (`maintaining-clean-ml-research-workflow`) is inside your `.agent/skills/` directory in your workspace.
   - If you cloned this whole repo to `.agent/skills/`, it is already there!

### Usage
When communicating with the agent, you can trigger this skill by saying:
- "Start a new research project"
- "Clean up this repo"
- "Refactor for a clean workflow"

### What it does
- **`docs/WORKLOG.md`**: Creates a single source of truth for your project.
- **File Cards**: Automatically documents every `.py` file you create.
- **Run Logging**: Ensures every experiment is saved to `runs/<id>/`.

To customize it, check the `UPDATING_THIS_SKILL.md` file inside the folder.
