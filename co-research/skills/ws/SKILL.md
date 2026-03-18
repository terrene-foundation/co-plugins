---
name: ws
description: Show workspace status dashboard
arguments: []
---

# /ws

Show the current workspace status dashboard. This provides a quick overview of where things stand.

## Protocol

1. **Find the active workspace** by checking `workspaces/` for the most recently modified project directory
2. **If no workspace found**, list available workspaces (excluding `_template`) and suggest creating one

## Dashboard Contents

### Paper Overview
- Read the paper brief from `briefs/`
- Display: paper title, target venue, current phase

### Literature Status
- Count files in `01-analysis/literature/`
- List recent literature assessments

### Decisions Made
- Count files in `03-drafts/deliberation/decisions/`
- List the most recent 5 decisions

### Draft Status
- Check `03-drafts/versions/` for draft snapshots
- Report current draft version and date

### Validation Status
- Check `04-validate/reviews/` for verification reports, challenge results, preflight reports
- Summarize: what has been validated, what has not

### Journal Activity
- Count journal entries by type
- Show the most recent 5 entries

### Active Todos
- List items in `todos/active/`
- Highlight high-priority items

### Session Notes
- Check for `.session-notes` file
- If present, show last session summary

## Output Format

```
=== COR Workspace: [name] ===
Paper: [title]
Venue: [target]
Phase: [current phase]

Literature:  [N] assessments
Decisions:   [N] recorded
Drafts:      [current version or "no drafts yet"]
Validation:  [summary]
Journal:     [N] entries ([breakdown by type])
Todos:       [N] active ([N] high priority)

Recent activity:
  [Last 3 journal entries or actions]
```
