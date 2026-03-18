---
name: start
description: New user orientation. Explains the COE workflow, checks workspace state, and asks about the course or project.
---

# COE Orientation

Welcome the user to this CO for Education workspace. This is a structured methodology for human-AI collaboration in university teaching design.

## First, check the workspace

1. Look for a `workspaces/` directory in the current project folder
2. If it exists, list any active projects (non-template subdirectories)
3. If it does not exist, explain that the user needs to set up a workspace:
   ```
   cp -r workspaces/_template workspaces/my-course
   ```

## Then explain the workflow

This COE workspace has five phases:

| Phase | What happens | Skill |
|-------|-------------|-------|
| **01 Research** | Understand the pedagogical context, student population, institutional requirements | `/co-education:analyze` |
| **02 Plan** | Create assessment or course design plan; stops for your approval | `/co-education:plan` |
| **03 Execute** | Build assessments, rubrics, materials one task at a time | `/co-education:execute` |
| **04 Review** | Alignment audit, AI-resilience review, fairness check | `/co-education:review` |
| **05 Finalize** | Polish, validate against learning outcomes, prepare for deployment | `/co-education:finalize` |

Domain-specific skills: `/co-education:design-assessment`, `/co-education:build-rubric`, `/co-education:map-outcomes`, `/co-education:audit-ai-resilience`, `/co-education:design-course`.

Utility skills: `/co-education:ws` (status), `/co-education:wrapup` (save progress), `/co-education:checkpoint` (review learning).

## Then ask

1. What course or assessment are you working on?
2. Is this a new course design, a revision of existing assessments, or a specific assessment task?
3. What is your institution and student context (cohort size, level, delivery mode)?
4. What are you most concerned about (AI integrity, alignment, workload, accreditation)?

Based on answers, recommend the next skill to run.

## If continuing existing work

Read `.session-notes` if it exists. Summarize what was accomplished and what the next step is.
