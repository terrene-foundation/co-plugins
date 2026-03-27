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
author: [human | agent | co-authored — see attribution rules below]
session_id: [current session ID if available, otherwise omit]
session_turn: [approximate conversation turn number when this entry was created]
project: [workspace name]
topic: [topic description]
phase: [current phase: analyze | plan | execute | review | finalize]
tags: []
---

## [Section heading appropriate to type]

[Content — prompt the user for details if not provided]

## For Discussion

[Generate 2-3 questions — see discussion rules below]
```

4. Type-specific structure:

   - **DECISION**: Sections for Decision, Alternatives Considered, Rationale, Consequences
   - **DISCOVERY**: Sections for What Was Discovered, Why It Matters, Follow-Up
   - **TRADE-OFF**: Sections for Trade-Off, What Was Gained, What Was Sacrificed, Acceptable Because
   - **RISK**: Sections for Risk Identified, Likelihood and Impact, Mitigation, Follow-Up
   - **CONNECTION**: Sections for Connection, Components Linked, Why This Matters
   - **GAP**: Sections for What Is Missing, Why It Matters, How to Resolve

5. **Attribution rules** — the `author` field uses this decision tree:
   - `human` — the user **stated** the conclusion, direction, or choice before the AI elaborated on it. The test: would this insight exist if the AI had said nothing? If yes → `human`.
   - `agent` — the AI surfaced this insight **unprompted** or in response to an open-ended request ("what should I watch out for?"). The test: did the user know this before the AI said it? If no → `agent`.
   - `co-authored` — the insight **evolved through exchange** — the user started in one direction, the AI added information, the user revised, and the final insight differs from both starting points. The test: can you attribute it to one party? If no → `co-authored`.
   - When uncertain, prefer `co-authored` over `human`. Over-crediting the user is worse than under-crediting — it creates false evidence of understanding.

6. **`session_turn`** — estimate the conversation turn number. This creates a temporal fingerprint: entries within a session should show increasing turn numbers. Gaps are normal (not every turn produces a journal entry), but decreasing numbers within a session indicate post-hoc insertion.

7. **"For Discussion" rules** — generate questions that meet ALL of these criteria:
   - At least one question must reference **specific data, sources, or constraints** mentioned in the entry (not abstractable)
   - At least one question must be a **counterfactual** ("If X had been different, would you still...")
   - Questions must NOT follow the same pattern across entries — vary the structure (compare, challenge assumption, extend to new context, invert premise, ask for evidence)
   - The questions should be ones the **user can answer only if they genuinely engaged** with the decision

8. After creating, confirm with the entry number and path.

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
