---
name: ws
description: Show workspace status dashboard. Read-only.
---

# Workspace Status

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `_template/`)
3. If no workspace exists, tell the user to create one first

## Dashboard

1. List contents of each phase directory (01-research through 05-output)
2. Count completed vs active todos
3. Check for .session-notes
4. Report the current phase based on which directories have content

Present as a clear status dashboard.
