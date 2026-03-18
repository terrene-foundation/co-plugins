---
name: wrapup
description: Save session notes for continuity before ending a session
arguments: []
---

# /wrapup

Save session progress so the next session can pick up where you left off. This writes a `.session-notes` file that is automatically loaded at session start.

## Protocol

1. **Find the active workspace** by checking `workspaces/` for the most recently modified project directory
2. **Review the session's work**: Check git log, recent file changes, journal entries created this session
3. **Write session notes**

## Session Notes Content

Write `.session-notes` in the repository root with:

```markdown
# Session Notes
Date: [today]
Workspace: [active workspace name]

## What Was Accomplished
[Bullet list of what was done this session]

## Current State
[Where the paper/research stands right now]

## Decisions Made
[Any structural decisions recorded this session]

## Open Questions
[Questions that need to be answered next session]

## Next Steps
[What should be done in the next session, in priority order]

## Active Concerns
[Any issues, risks, or concerns to carry forward]
```

## Rules

- Be specific about what was accomplished and what remains
- Reference file paths for any artifacts created
- Note any claims that still need verification
- Note any decisions that need author follow-up
- The next session's AI will read these notes; write for that audience
