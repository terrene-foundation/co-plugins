---
name: start
description: Orientation for governance officers. Explains the COG workflow, checks workspace state, and asks about the governance task.
---

# COG Orientation

Welcome the user to the CO for Governance (COG) workspace. This is the Terrene Foundation's self-governance tool, built on its own CO methodology.

## First, check the workspace

1. Look for a `workspaces/` directory in the current project folder
2. If it exists, list any active projects (non-template subdirectories)
3. If it does not exist, explain that the user needs to set up a workspace:
   ```
   cp -r workspaces/_template workspaces/my-governance-task
   ```

## Then explain the workflow

This COG workspace has five phases for governance work:

| Phase | What happens | Skill |
|-------|-------------|-------|
| **01 Research** | Constitutional analysis, precedent review, requirements gathering | `/co-governance:analyze` |
| **02 Plan** | Governance action plan; stops for officer approval | `/co-governance:plan` |
| **03 Execute** | Draft governance artifacts one at a time | `/co-governance:execute` |
| **04 Review** | Constitutional compliance check, independence audit, transparency review | `/co-governance:review` |
| **05 Finalize** | Polish, validate against constitution, prepare for filing or publication | `/co-governance:finalize` |

Governance-specific skills:
- `/co-governance:check-constitution` -- Check an action against the 77-clause constitution
- `/co-governance:draft-rfc` -- Draft an RFC for a governance change
- `/co-governance:transparency-report` -- Generate a transparency report
- `/co-governance:audit-compliance` -- Audit governance actions for compliance
- `/co-governance:review-membership` -- Review a membership application

Utility skills: `/co-governance:ws` (status), `/co-governance:wrapup` (save progress), `/co-governance:checkpoint` (review learning).

## Then ask

1. What governance task are you working on?
2. Is this a new task or continuing existing work?
3. What is the target output (RFC, transparency report, compliance check, membership review, policy draft)?
4. What phase is the officer in (or starting fresh)?

Based on answers, recommend the next skill to run.

## If continuing existing work

Read `.session-notes` if it exists. Summarize what was accomplished and what the next step is.
