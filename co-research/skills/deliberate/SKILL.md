---
name: deliberate
description: Record a structural decision about the paper with alternatives and rationale
arguments:
  - name: topic
    description: The decision topic or question to resolve
    required: true
---

# /deliberate $topic

You are recording a structural decision about **$topic**. Every significant decision about the paper's argument, structure, scope, or framing must be documented with alternatives considered and rationale for the choice.

## Protocol

1. **Find the active workspace** by checking `workspaces/` for the most recently modified project directory
2. **Load context**: Read the paper brief, existing decisions in `03-drafts/deliberation/decisions/`, and relevant journal entries
3. **Check for prior decisions**: Has this topic been decided before? If so, surface the prior decision and ask if it should be revisited

## Deliberation Process

### Step 1: Frame the Decision
State clearly what needs to be decided and why it matters for the paper.

### Step 2: Present Alternatives
Present at least 2 genuinely viable alternatives (not strawmen). For each:
- What the option is
- How it affects the paper's argument
- How it affects reviewer reception at the target venue
- Trade-offs

### Step 3: Recommend
State your recommendation with reasoning. Be explicit about confidence level.

### Step 4: Wait for Author Decision
Do NOT proceed without the author's explicit choice.

### Step 5: Record the Decision

Create a decision record in `03-drafts/deliberation/decisions/` named `NNNN-[topic-slug].md`:

```markdown
---
id: NNNN
topic: $topic
date: [today]
decision: [what was decided]
confidence: high | medium | low
---

## Question
[What needed to be decided]

## Alternatives Considered

### Option A: [Name]
[Description, argument impact, reviewer impact, trade-offs]

### Option B: [Name]
[Description, argument impact, reviewer impact, trade-offs]

## Decision
[What was chosen and why]

## Reviewer Impact
[How this choice affects reception at the target venue]
```

## Journal Entry

Produce a DELIBERATION journal entry in the workspace's `journal/` directory:

```yaml
---
type: DELIBERATION
date: [today]
paper: [paper name from brief]
topic: $topic
tags: [relevant tags]
---
```
