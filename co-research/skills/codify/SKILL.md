---
name: codify
description: "Load phase 05 (codify) for the current workspace. Capture institutional knowledge."
---

## What This Phase Does (present to user)

Capture everything we learned during this initiative — the decisions, patterns, and domain knowledge — so that future work starts with full context. This is the institutional memory: next time anyone works on related topics, the AI already knows what was decided and why.

## Your Role (communicate to user)

Confirm that the captured knowledge accurately represents the decisions made and their rationale. You're reviewing for intent and accuracy — "Does this describe what we decided and why?"

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `instructions/`)
3. If no workspace exists, ask the user to create one first
4. Read all files in `workspaces/<project>/briefs/` for user context

## Phase Check

- Read `workspaces/<project>/04-validate/` to confirm validation passed (if applicable)
- Review the knowledge base for areas that need updating
- Output updates go into appropriate project directories

## Workflow

### 1. Knowledge extraction

Review all work produced in this initiative:

- What decisions were made and why
- What patterns emerged
- What risks were identified and how they were addressed
- What cross-references were established

### 2. Decision log consolidation

Collect all decisions from the implementation phase and create a consolidated decision log:

```yaml
decisions:
  - decision: "Example decision description"
    rationale: "Why this was chosen over alternatives"
    alternatives_rejected: "What other options were considered"
    date: 2026-03-24
    initiative: project-name
    confidence: high
```

Store in `workspaces/<project>/decisions.yml` for future reference.

### 3. Pattern observation

Identify recurring patterns from this initiative that could improve future work:

- **Process patterns**: What workflow steps were most/least effective?
- **Decision patterns**: Were there recurring decision types (e.g., "always chose simpler over comprehensive")?
- **Quality patterns**: What issues came up repeatedly during review?
- **Agent patterns**: Which agent combinations worked well together?

Document observations for the learning pipeline. If a pattern appears with high confidence (3+ occurrences), propose it as a candidate rule or skill update.

### 4. Update knowledge base

Update the relevant areas of the project's documentation:

- Add or update documents in the appropriate directory
- Ensure cross-references are bidirectional
- Update any affected foundational documents (with care — these are authoritative)
- Add supporting research to the appropriate documentation area

### 5. Update memory and session notes

If significant knowledge was gained that applies across sessions:

- Update auto-memory with key patterns and decisions
- Ensure the anti-amnesia rules are still accurate
- Update learned-instincts if new patterns were confirmed

### 6. Present captured knowledge

Summarize what was captured and where it lives. Ask:

- "Does this accurately represent what we decided?"
- "Is there anything we learned that I missed capturing?"
- "Should any of this be kept confidential rather than in the knowledge base?"

### 7. What comes next

After codification, guide the user to the appropriate next step:

**Does this work need further iteration?**

- More tasks to implement → Run `/co-research:implement` again
- New concerns emerged → Run `/co-research:analyze` on the new concern
- Adjacent initiative needed → Create a new brief and start a new cycle

**Is this work complete?**

- Knowledge is captured, initiative is done → The knowledge base is updated for future sessions

**Are there domain-specific next steps?**

- Check available commands (e.g., `/co-research:publish`) for post-codification workflows specific to this project type

## Agent Teams

Deploy these agents as a team for codification:

**Knowledge extraction team:**

- **deep-analyst** — Identify core decisions and patterns worth capturing
- **requirements-analyst** — Distill requirements into reusable knowledge

**Quality team:**

- **cross-reference-auditor** — Review captured knowledge for accuracy and completeness
- **claims-verifier** — Verify any factual claims in the captured knowledge
