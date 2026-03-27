---
name: todos
description: "Load phase 02 (todos) — create a project plan with all deliverables and milestones"
---

## What This Phase Does (present to student)

Turn the research and outline into a complete project plan — every deliverable, section, and task needed to finish the project, organized by milestone. This is your roadmap from first draft to final submission.

## Your Role (communicate to student)

Review and approve the plan before drafting starts. This is your most important checkpoint — the plan is a contract for what gets produced. Focus on whether the milestones describe the work you need to submit and whether the timeline fits your deadline.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `instructions/`)
3. If no workspace exists, ask the student to create one first
4. Read all files in `workspaces/<project>/briefs/` for student context (this is the student's input surface)

## Phase Check

- Read files in `workspaces/<project>/02-plans/` and `workspaces/<project>/03-structure/` for context
- Check if `todos/active/` already has files (resuming)
- All todos go into `workspaces/<project>/todos/active/`

## Workflow

### 1. Review research and outline

Reference the analysis in `workspaces/<project>/01-analysis/` and structure in `workspaces/<project>/03-structure/`. Work through every file.

- Review with specialists to ensure the research foundation is solid
- Confirm the outline and argument structure are ready to support drafting
- Identify any remaining research needs (additional sources, data to collect, calculations to run)

### 2. Break down into specific deliverables

Identify every concrete deliverable the student needs to produce:

- **Written sections**: Introduction, literature review, methodology, analysis, discussion, conclusion
- **Data work**: Tables, charts, calculations, datasets to compile
- **Citations**: Sources to locate, format, and integrate
- **Supporting materials**: Appendices, bibliography, executive summary, abstract
- **Presentation materials**: Slides, speaker notes, handouts (if applicable)
- **Formatting**: Compliance with style guide (APA, Chicago, etc.), page limits, margin requirements

### 3. Create task list organized by section and deliverable

Create detailed todos for EVERY task required. Place them in `todos/active/`.

**CRITICAL: Write ALL todos for the ENTIRE project.**

- Do NOT limit to "just the first section" or "what should be done now"
- Do NOT prioritize or filter — write EVERY task required to complete the full project
- Cover every section, every data table, every citation, every formatting requirement
- Each todo should be detailed enough to work on independently
- If the outline references it, there must be a todo for it
- For large projects (20+ todos), organize into numbered milestones/groups for clarity

### 4. Estimate effort and create timeline

- Map milestones to the student's deadline
- Identify which tasks can be done in parallel
- Flag tasks that depend on others (e.g., "analysis section depends on data collection")
- Build in time for revision and proofreading

### 5. Red team the plan for completeness

Review with agents continuously until they are satisfied there are no gaps remaining:

- Does every section in the outline have corresponding tasks?
- Are citation and formatting tasks included, not just writing?
- Is the timeline realistic given the deadline?
- Are there dependencies that could create bottlenecks?

### 6. STOP — present plan and wait for student approval

Present the complete plan organized by milestones. For each milestone, explain:

- **What will be completed** after this milestone (e.g., "Literature review drafted with 15 sources integrated")
- **How many tasks** are involved (gives a sense of relative effort)
- **Dependencies** — which milestones must come first (in plain language: "We need to finish data collection before we can write the analysis section")
- **Timeline** — when this milestone should be done relative to the deadline

Then ask these specific questions:

1. "Does this plan cover everything your assignment requires?"
2. "Is anything here that you did not ask for or do not need?"
3. "Is anything missing that you expected to see?"
4. "Does the order make sense — are the most important sections tackled first?"
5. "Does the timeline work with your deadline and other commitments?"

**Do NOT proceed to drafting until the student explicitly approves.**

## Agent Teams

Deploy these agents as a team for project planning:

- **todo-manager** — Create and organize the detailed todos, ensure completeness
- **assignment-analyst** — Break down assignment requirements, identify missing tasks, check rubric coverage
- **research-assistant** — Verify that all research needs are captured as tasks
- **peer-reviewer** — Review the plan for gaps, unrealistic timelines, or missing deliverables
- **deep-analyst** — Identify failure points, dependencies, and risks in the plan

For projects involving quantitative work, additionally deploy:

- **quantitative-analyst** — Ensure data analysis and calculation tasks are properly scoped
- **financial-engineer** — Ensure valuation or modeling tasks are realistic

Red team the plan with agents until they confirm no gaps remain.
