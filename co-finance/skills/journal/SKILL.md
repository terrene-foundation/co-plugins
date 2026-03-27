---
name: journal
description: "View journal status, create entries, or search the project journal."
---

Manage the project journal. The journal is your analytical knowledge trail — it captures the decisions, discoveries, trade-offs, risks, connections, and gaps you encounter as you work through finance assignments, research, and exam prep.

Parse `$ARGUMENTS`:

- **Empty or "status"**: Show journal status
- **"new TYPE topic"**: Create a new journal entry (e.g., `new DECISION chose-dcf-over-comparables`)
- **"search QUERY"**: Search existing entries by topic or tag

---

## Action: Status (default)

1. Determine the active workspace:
   - If working in a workspace, use it
   - Otherwise, use the most recently modified directory under `workspaces/` (excluding `instructions/`)

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
project: [workspace name]
topic: [topic description]
phase: [current COF phase: analyze | todos | assignment | review | wrapup]
tags: []
---

## [Section heading appropriate to type]

[Content — prompt the student for details if not provided]
```

4. Type-specific structure:

   - **DECISION**: Sections for Decision, Alternatives Considered, Rationale, Consequences
     - Example: "DECISION: chose-dcf-over-comparables" — why DCF was the right valuation method for this assignment
   - **DISCOVERY**: Sections for What Was Discovered, Why It Matters, Follow-Up
     - Example: "DISCOVERY: correlation-gdp-interest-rates" — a finding from your data analysis
   - **TRADE-OFF**: Sections for Trade-Off, What Was Gained, What Was Sacrificed, Acceptable Because
     - Example: "TRADE-OFF: simplicity-vs-accuracy-in-model" — using a 2-factor model instead of Fama-French 5-factor
   - **RISK**: Sections for Risk Identified, Likelihood and Impact, Mitigation, Follow-Up
     - Example: "RISK: survivorship-bias-in-fund-data" — a methodological concern in your dataset
   - **CONNECTION**: Sections for Connection, Components Linked, Why This Matters
     - Example: "CONNECTION: modigliani-miller-links-to-capm" — a theoretical relationship you noticed
   - **GAP**: Sections for What Is Missing, Why It Matters, How to Resolve
     - Example: "GAP: missing-10yr-yield-data" — data you still need to find for your analysis

5. After creating, confirm with the entry number and path.

---

## Action: Search

1. Search all `journal/*.md` files for the query string in:
   - Filename
   - Frontmatter `topic` and `tags` fields
   - Body content

2. Display matching entries with their number, type, date, and topic.

## Error Handling

- **No workspace detected**: Ask the student which workspace to use, or list available workspaces.
- **Journal directory missing**: Create `journal/` in the workspace and proceed.
- **Invalid TYPE**: Show the list of valid types (DECISION, DISCOVERY, TRADE-OFF, RISK, CONNECTION, GAP) and ask the student to choose.
- **Numbering gaps**: Acceptable. Always use the highest existing number + 1, regardless of gaps.
