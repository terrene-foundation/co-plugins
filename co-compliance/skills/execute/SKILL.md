---
name: execute
description: Work through the compliance assessment plan one task at a time. Each task produces evidence-referenced deliverables.
---

# /execute

Work through the approved compliance assessment plan from `02-planning/plan.md`, one task at a time.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `_template/`)
3. If no workspace exists, ask the user to create one first

## Protocol

1. **Read the plan** from `02-planning/plan.md`
2. **Find the next incomplete task**
3. **Execute it**, producing the specified deliverable with proper citations and evidence references
4. **Save output** to `03-work/`
5. **Mark the task complete** in the plan
6. **Report what was done** and what the next task is

## Rules

- One task at a time. Do not batch.
- Each task produces a tangible, evidence-referenced output saved to the workspace.
- If a task requires a judgment call the compliance officer has not made (e.g., applicability determination, risk acceptance), ASK. Do not decide for them.
- If a task cannot be completed due to missing information, explain exactly what is needed.
- Every regulatory citation must include regulation name, section, jurisdiction, and effective date.
- Every compliance claim must reference the evidence that supports it.

## Next Step

When all tasks are complete, recommend `/review` for quality checking of the compliance work products.
