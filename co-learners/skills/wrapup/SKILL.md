---
name: wrapup
description: "Write session notes before ending. Captures context for next session."
---

Write session notes to preserve context for the next session.

1. Determine the active workspace:
   - If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
   - Otherwise, use the most recently modified directory under `workspaces/` (excluding `_template/`)

### Journal Check

Before writing session notes, review the session's work and create journal entries for any un-journaled decisions, discoveries, or risks:
- Were any analytical decisions made without DECISION entries?
- Were any research findings discovered without DISCOVERY entries?
- Were any risks identified without RISK entries?

Create entries for anything missing, then proceed to write session notes.

2. Write a `.session-notes` file in the workspace root using plain language a student can understand:
   - **Accomplished**: Describe in terms of academic progress ("Completed literature review section with 12 sources" not "Modified 8 files")
   - **In progress**: Describe what section or task is being worked on
   - **Blockers**: Describe any decisions needed from the student in clear, specific terms
   - **Next steps**: Describe what will happen next session in terms of academic outcomes
   - **Active todo**: Which todo was being worked on (for context restoration)

3. Keep it concise (under 30 lines). This file is read by the next session's startup to restore context.

4. Overwrite any existing `.session-notes` — only the latest matters.
