---
name: journal
description: "View journal status, create entries, or search the project journal."
---

Manage the project journal. The journal is the primary knowledge trail — it captures decisions, discoveries, trade-offs, risks, connections, and gaps across sessions.

Parse `$ARGUMENTS`:

- **Empty or "status"**: Show journal status
- **"new TYPE topic"**: Create a new journal entry (e.g., `new DECISION chose-assessment-model`)
- **"search QUERY"**: Search existing entries by topic or tag

---

## Action: Status (default)

1. Determine the active workspace:
   - If working in a workspace, use it
   - Otherwise, use the most recently modified directory under `workspaces/` (excluding `_template/`)

2. In the workspace's `journal/` directory:
   - Count total entries
   - Count entries by type (DECISION, DISCOVERY, TRADE-OFF, RISK, CONNECTION, GAP)
   - List the 5 most recent entries with their date, type, and topic (from frontmatter)
   - Show the highest entry number (for next entry reference)

3. Present as a compact summary.

---

## Action: New Entry

1. Parse the TYPE and topic from arguments. Valid types: DECISION, DISCOVERY, TRADE-OFF, RISK, CONNECTION, GAP.

2. Determine the next sequential number by checking the highest existing `NNNN-` prefix in the journal directory. If no entries exist, start at `0001`.

3. Create the file at `journal/NNNN-TYPE-topic.md` with this structure:

```markdown
---
type: [TYPE]
date: [today's date, YYYY-MM-DD]
created_at: [ISO-8601 timestamp, e.g. 2026-03-27T14:23:17Z]
author: [human | agent | co-authored — based on who drove the insight]
session_id: [current session ID if available, otherwise omit]
project: [workspace name]
topic: [topic description]
phase: [current phase: analyze | plan | execute | review | finalize]
tags: []
---

## [Section heading appropriate to type]

[Content — prompt the user for details if not provided]

## For Discussion

[Generate 2-3 questions an assessor or collaborator might ask about this entry, based on the actual content and decision context. These should probe the reasoning, not just restate facts.]
```

4. Type-specific structure:

   - **DECISION**: Sections for Decision, Alternatives Considered, Rationale, Consequences
   - **DISCOVERY**: Sections for What Was Discovered, Why It Matters, Follow-Up
   - **TRADE-OFF**: Sections for Trade-Off, What Was Gained, What Was Sacrificed, Acceptable Because
   - **RISK**: Sections for Risk Identified, Likelihood and Impact, Mitigation, Follow-Up
   - **CONNECTION**: Sections for Connection, Components Linked, Why This Matters
   - **GAP**: Sections for What Is Missing, Why It Matters, How to Resolve

5. The `author` field reflects who drove the insight:
   - `human` — the user identified this insight, the AI recorded it
   - `agent` — the AI surfaced this insight during analysis
   - `co-authored` — emerged through dialogue; neither party alone would have reached it

6. The `## For Discussion` section scaffolds metacognition and prepares for oral follow-up. Generate questions specific to the entry content — not generic templates.

7. After creating, confirm with the entry number and path.

---

## Action: Search

1. Search all `journal/*.md` files for the query string in:
   - Filename
   - Frontmatter `topic` and `tags` fields
   - Body content

2. Display matching entries with their number, type, date, and topic.

## Error Handling

- **No workspace detected**: Ask the user which workspace to use, or list available workspaces.
- **Journal directory missing**: Create `journal/` in the workspace and proceed.
- **Invalid TYPE**: Show the list of valid types (DECISION, DISCOVERY, TRADE-OFF, RISK, CONNECTION, GAP) and ask the user to choose.
- **Numbering gaps**: Acceptable. Always use the highest existing number + 1, regardless of gaps.
