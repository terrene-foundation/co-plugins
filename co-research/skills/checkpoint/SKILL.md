---
name: checkpoint
description: Review learning progress and journal entries
arguments: []
---

# /checkpoint

Review your learning progress across the research project. This command surveys journal entries, decisions, and craft notes to show what you have learned and where gaps remain.

## Protocol

1. **Find the active workspace** by checking `workspaces/` for the most recently modified project directory
2. **Read all journal entries** from `journal/`
3. **Read all decision records** from `03-drafts/deliberation/decisions/`
4. **Read craft notes** from `craft-notes/`
5. **Synthesize a progress report**

## Report Contents

### Knowledge Map
Group journal entries by topic and show coverage:
- Which areas of the literature have been explored?
- Which areas remain unexplored?
- Which concepts has the author been taught about?

### Decision Trail
List all structural decisions with their rationale:
- What has been settled?
- What remains open?
- Are any prior decisions being contradicted by new information?

### Claim Status
From CLAIM journal entries:
- How many claims have been verified?
- How many remain unverified?
- Any FABRICATED or OVERCLAIMED findings outstanding?

### Defense Readiness
From DEFENSE journal entries:
- What challenges have been raised?
- Which have been addressed?
- Which remain open vulnerabilities?

### Gap Analysis
From GAP journal entries:
- What gaps have been identified?
- Which have been filled?
- Which remain?

### Writing Progress
From MARGIN journal entries:
- Which sections have been drafted?
- Which paragraphs have been approved?
- What is the current word count?

## Output Format

```
=== COR Checkpoint: [workspace] ===
Date: [today]

Knowledge coverage:
  Explored: [topics]
  Unexplored: [topics]

Decisions: [N] settled, [N] open
Claims: [N] verified, [N] outstanding
Challenges: [N] raised, [N] resolved
Gaps: [N] identified, [N] filled
Sections drafted: [list]

Recommendation: [what to focus on next]
```
