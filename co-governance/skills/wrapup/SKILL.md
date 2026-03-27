---
name: wrapup
description: Save session notes before ending. Captures context for the next session.
---

# Session Wrapup

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `_template/`)
3. If no workspace exists, ask the user to create one first

## Journal Check

Before writing session notes, review the session's work and create journal entries for any un-journaled decisions, discoveries, or risks:
- Were any significant decisions made without DECISION entries?
- Were any technical findings discovered without DISCOVERY entries?
- Were any risks identified without RISK entries?

Create entries for anything missing, then proceed to write session notes.

## Protocol

Write a `.session-notes` file in the workspace root capturing:

1. What was accomplished this session
2. What decisions were made
3. What the next steps are
4. Any unresolved questions or blockers

This file will be read by `/start` in the next session to restore context.
