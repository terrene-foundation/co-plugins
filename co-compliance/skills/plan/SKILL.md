---
name: plan
description: Create a compliance assessment plan based on regulatory analysis. Stops for human approval before execution begins.
---

# /plan

Create a structured compliance assessment plan for the active project. This plan requires human approval before any assessment work begins.

## Protocol

1. **Read analysis outputs** from `01-research/`
2. **Define assessment scope** based on applicable regulations and organizational context
3. **Break the assessment into phases and tasks** with clear deliverables
4. **Identify dependencies** between regulatory requirements
5. **Present the plan for approval** - do NOT proceed without explicit approval

## Output

Save the plan to `02-planning/plan.md`:

```markdown
# Compliance Assessment Plan
Date: [today]
Scope: [What is being assessed]
Regulations: [In-scope regulations]
Timeline: [Target completion or audit date]

## Objective
[What this assessment will produce]

## Assessment Phases

### Phase 1: Requirement Extraction
- [ ] Task 1.1: [Regulation] - Extract requirements - Requirements register
- [ ] Task 1.2: [Regulation] - Extract requirements - Requirements register

### Phase 2: Control Mapping
- [ ] Task 2.1: Map [requirement area] to controls - Control mapping document
- [ ] Task 2.2: Map [requirement area] to controls - Control mapping document

### Phase 3: Gap Analysis
- [ ] Task 3.1: Assess gaps in [area] - Gap assessment with severity ratings
- [ ] Task 3.2: Assess gaps in [area] - Gap assessment with severity ratings

### Phase 4: Reporting
- [ ] Task 4.1: Draft compliance report - Report draft
- [ ] Task 4.2: Prepare audit documentation - Evidence package

## Dependencies
[What depends on what]

## Risks
[What could delay or complicate the assessment]

## Out of Scope
[What this assessment explicitly does not cover]
```

## Approval Gate

Present the plan and ask:
1. Does this cover all the regulations and requirements you need assessed?
2. Is anything here that you did not ask for or that is out of scope?
3. Is the phasing correct? Are dependencies captured?
4. Are there any organizational constraints (deadlines, resource limits) that affect this plan?

Do NOT proceed to `/execute` until the compliance officer approves.
