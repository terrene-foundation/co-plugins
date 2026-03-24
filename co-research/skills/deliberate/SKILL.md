---
name: deliberate
description: "Record a structural decision about the paper. What was decided, why, what was rejected."
---

## What This Command Does (present to user)

Records a structural decision about the paper — subtitle choice, section ordering, scope boundary, what to include or exclude. The decision and its rationale are documented for the audit trail.

## Your Role (communicate to user)

This is your decision. I present the options, explain the trade-offs, and suggest a recommendation. But you decide. The record captures your reasoning, not mine.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a workspace, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/`
3. Store decisions in `workspaces/<project>/03-drafts/deliberation/decisions/`

## Workflow

### 1. Parse the topic

Extract the decision topic from `$ARGUMENTS`.

### 2. Frame the decision

Present clearly:

- What is being decided
- What options exist (at least 2 genuinely viable alternatives)
- Trade-offs for each option
- Reviewer impact: how would each choice affect reception at the target venue?
- Recommendation with reasoning

### 3. Wait for the author's decision

This is a FULL verification gate. The author must explicitly state their choice. Do not proceed without it.

### 4. Record the decision

Store a structured decision record:

```markdown
# Decision: [Topic]

**Date**: [Date]
**Decided**: [What was decided]
**Rationale**: [Why — in the author's words if possible]
**Alternatives considered**:

- [Option A] — rejected because [reason]
- [Option B] — rejected because [reason]
  **Reviewer impact**: [How this affects reception]
  **Confidence**: [Author's confidence level]
```

Save in `workspaces/<project>/03-drafts/deliberation/decisions/<topic-slug>.md`.

### 5. Confirm

Show the recorded decision to the author. Ask: "Does this accurately capture your reasoning?"

## Approval Gate

FULL verification — the author must explicitly make the decision and confirm the record captures it accurately.

## Agent Team

- No specific agent delegation — this is a direct interaction between the AI and the author
- **field-expert** may be consulted if the decision involves domain knowledge
