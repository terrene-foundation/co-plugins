---
name: todos
description: "Load phase 02 (todos) for the current workspace"
---

## What This Phase Does (present to user)

Turn the research and plans into a complete roadmap — every task needed to deliver the initiative, organized by milestones.

## Your Role (communicate to user)

Review and approve the roadmap before work starts. This is your most important checkpoint — the roadmap is a contract for what gets delivered. Focus on whether the milestones describe the outcomes you want.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `instructions/`)
3. If no workspace exists, ask the user to create one first
4. Read all files in `workspaces/<project>/briefs/` for user context

## Phase Check

- Read files in `workspaces/<project>/02-plans/` for context
- Check if `todos/active/` already has files (resuming)
- All todos go into `workspaces/<project>/co-research:todos/active/`

## Workflow

### 1. Review plans with specialists

Reference plans in `workspaces/<project>/02-plans/` and work through every file.

- Consult relevant domain experts for specialized work
- Ensure cross-references and dependencies are mapped

### 2. Create comprehensive todos

**CRITICAL: Write ALL todos for the ENTIRE initiative.**

- Do NOT limit to "phase 1" or "what should be done now"
- Do NOT prioritize or filter — write EVERY task required to complete the full initiative
- Cover research, drafting, review, cross-referencing, and finalization — everything
- Each todo should be detailed enough to execute independently
- If the plans reference it, there must be a todo for it
- For large initiatives (20+ todos), organize into numbered milestones/groups

Each todo should specify:

- **What**: The specific deliverable
- **Where**: The file path(s) for output
- **Evidence type**: What completion evidence is needed (see `/co-research:implement` completion evidence)
- **Expert consultation**: Which agents should be consulted

Create detailed todos for EVERY task required. Place them in `todos/active/`.

### 3. Red team the todo list

Review with agents continuously until they are satisfied there are no gaps remaining.

### 4. STOP — present roadmap and wait for human approval

Present the complete roadmap organized by milestones. For each milestone, explain:

- **What will be delivered** after this milestone is complete
- **How many tasks** are involved
- **Dependencies** — which milestones must come first

Then ask these specific questions:

1. "Does this roadmap cover everything you described in your brief?"
2. "Is anything here that you didn't ask for or don't need right now?"
3. "Is anything missing that you expected to see?"
4. "Does the milestone order make sense?"

**Do NOT proceed to implementation until the user explicitly approves.**

## Agent Teams

Deploy these agents as a team for todo creation:

- **todo-manager** — Create and organize the detailed todos, ensure completeness
- **requirements-analyst** — Break down requirements, identify missing tasks
- **deep-analyst** — Identify failure points, dependencies, and gaps

Red team the todo list with agents until they confirm no gaps remain.
