---
name: checkpoint
description: Review progress and learning. What has been accomplished, what patterns emerged, what to improve.
---

# Checkpoint

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, review `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `_template/`)
3. If no workspace exists, ask the user to create one first

## Protocol

Review the current state of the project and learning:

1. Read all journal entries from `journal/`
2. Read all completed todos from `todos/completed/`
3. Summarize what has been learned
4. Identify patterns that emerged during work
5. Suggest improvements to the workflow

Present as a progress review with specific observations.
