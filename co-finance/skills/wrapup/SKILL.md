---
name: wrapup
description: "Write session notes before ending. Captures context for next session."
---

Write session notes to preserve context for the next session.

1. Determine the active workspace:
   - If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
   - Otherwise, use the most recently modified directory under `workspaces/` (excluding `instructions/`)

### Journal Check

Before writing session notes, review the session's work and create journal entries for any un-journaled decisions, discoveries, or risks:
- Were any analytical decisions made without DECISION entries? (e.g., choosing a valuation method, selecting a data source, picking a theoretical framework)
- Were any research findings discovered without DISCOVERY entries? (e.g., correlations in data, key insights from literature, surprising results)
- Were any risks identified without RISK entries? (e.g., data quality issues, survivorship bias, missing variables)

Create entries for anything missing, then proceed to write session notes.

2. Write a `.session-notes` file in the workspace root using plain language a student can understand:
   - **Accomplished**: Describe in terms of what academic progress was made ("Completed literature review section with 12 sources" not "Modified 8 files"; "Finished data analysis for Table 3 showing GDP correlation" not "Updated pandas dataframe pipeline")
   - **In progress**: Describe what section or task is being worked on ("Working on methodology section — explaining the regression approach" not "Refactoring the analysis module")
   - **Blockers**: Describe any decisions needed from the student in clear, specific terms ("Need to decide whether to use 5-year or 10-year data window for the analysis — 5-year is more current but 10-year captures the 2008 crisis")
   - **Next steps**: Describe what will happen next session in terms of academic outcomes ("Next session: draft the discussion section and start on conclusions")
   - **Active todo**: Which todo was being worked on (for the AI's context restoration)

3. Keep it concise (under 30 lines). This file is read by the next session's startup to restore context.

4. Overwrite any existing `.session-notes` — only the latest matters.
