---
name: journal
description: "View journal status, create entries, or search the project journal."
---

Manage the project journal — your knowledge trail capturing decisions, discoveries, trade-offs, risks, connections, and gaps.

Parse `$ARGUMENTS`:
- **Empty or "status"**: Show journal status
- **"new TYPE topic"**: Create a new entry (e.g., `new DECISION chose-comparative-method`)
- **"search QUERY"**: Search existing entries

---

## Action: Status (default)

1. Determine the active workspace (or most recently modified under `workspaces/`, excluding `_template/`)
2. In `journal/`: count total entries, count by type, list 5 most recent (date, type, topic), show highest entry number
3. Present as a compact summary

---

## Action: New Entry

1. Parse TYPE and topic. Valid types: DECISION, DISCOVERY, TRADE-OFF, RISK, CONNECTION, GAP
2. Determine next sequential number (highest existing `NNNN-` prefix + 1, or `0001`)
3. Create at `journal/NNNN-TYPE-topic.md` with frontmatter (type, date, project, topic, phase, tags) and type-specific sections:
   - **DECISION**: Decision, Alternatives Considered, Rationale, Consequences
   - **DISCOVERY**: What Was Discovered, Why It Matters, Follow-Up
   - **TRADE-OFF**: Trade-Off, What Was Gained, What Was Sacrificed, Acceptable Because
   - **RISK**: Risk Identified, Likelihood and Impact, Mitigation, Follow-Up
   - **CONNECTION**: Connection, Components Linked, Why This Matters
   - **GAP**: What Is Missing, Why It Matters, How to Resolve
4. Include a `## For Discussion` section with 2-3 probing questions
5. Confirm with entry number and path

---

## Action: Search

Search all `journal/*.md` files (filename, frontmatter topic/tags, body content) and display matches with number, type, date, and topic.

## Error Handling

- **No workspace**: ask which to use or list available
- **Journal directory missing**: create `journal/` and proceed
- **Invalid TYPE**: show valid types and ask the student to choose
- **Numbering gaps**: acceptable; always use highest + 1
