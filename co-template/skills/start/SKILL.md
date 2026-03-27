---
name: start
description: New user orientation. Explains the CO workflow, checks workspace state, and asks about the project.
---

# CO Orientation

Welcome the user to this CO workspace. This is a structured methodology for human-AI collaboration.

## First, check the workspace

1. If `$ARGUMENTS` specifies a project name, focus on `workspaces/$ARGUMENTS/`
2. Otherwise, look for a `workspaces/` directory in the current project folder
3. If workspaces exist, list any active projects (non-template subdirectories)
4. If no workspaces exist, explain that the user needs to set up a workspace:
   ```
   cp -r workspaces/_template workspaces/my-project
   ```

## Then explain the workflow

This CO workspace has five phases:

| Phase | What happens | Skill |
|-------|-------------|-------|
| **01 Research** | Understand the problem space, gather information | `/co-template:analyze` |
| **02 Plan** | Create a structured plan; stops for your approval | `/co-template:plan` |
| **03 Execute** | Work through the plan one task at a time | `/co-template:execute` |
| **04 Review** | Quality check, adversarial critique | `/co-template:review` |
| **05 Finalize** | Polish, validate, prepare final output | `/co-template:finalize` |

Utility skills: `/co-template:ws` (status), `/co-template:wrapup` (save progress), `/co-template:checkpoint` (review learning).

## Then ask

1. What is the project or task?
2. Is this new or continuing existing work?
3. What is the target output (report, analysis, document, plan)?
4. What phase is the user in (or starting fresh)?

Based on answers, recommend the next skill to run.

## If continuing existing work

Read `.session-notes` if it exists. Summarize what was accomplished and what the next step is.
