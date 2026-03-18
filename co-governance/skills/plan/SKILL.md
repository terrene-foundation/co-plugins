---
name: plan
description: Create a governance action plan based on analysis. Stops for officer approval before execution begins.
---

# /plan

Create a structured governance action plan for the active project. This plan requires officer approval before any execution begins.

## Protocol

1. **Read analysis outputs** from `01-research/`
2. **Identify the constitutional basis** for the planned governance actions
3. **Break the work into phases and tasks** with clear deliverables
4. **Flag any tasks that require constitutional interpretation**
5. **Present the plan for approval** - do NOT proceed without explicit officer approval

## Output

Save the plan to `02-planning/plan.md`:

```markdown
# Governance Action Plan
Date: [today]

## Objective
[What this plan achieves]

## Constitutional Basis
[Which clauses authorize this governance work]

## Tasks

### Phase 1: Research & Analysis
- [ ] Task 1.1: [Description] - [Deliverable]
- [ ] Task 1.2: [Description] - [Deliverable]

### Phase 2: Drafting
- [ ] Task 2.1: [Description] - [Deliverable]

### Phase 3: Review & Compliance
- [ ] Task 3.1: [Description] - [Deliverable]

## Dependencies
[What depends on what]

## Constitutional Risks
[Where constitutional interpretation may be needed. Where entrenched provisions are close to the boundary.]

## Transparency Requirements
[What must be documented and disclosed]
```

## Approval Gate

Present the plan and ask:
1. Does this cover everything you need?
2. Is any governance action here that you did not authorize?
3. Is the order correct?
4. Should any task be removed or added?
5. Are there any constitutional interpretations you want to make before proceeding?

Do NOT proceed to `/execute` until the governance officer approves.
