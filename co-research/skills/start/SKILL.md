---
name: start
description: New user orientation for COR. Explains the workflow, checks workspace state, and asks about the research project.
---

# COR Orientation

Welcome the user to COR (Cognitive Orchestration for Research). This is a structured co-authorship methodology for academic publications.

## First, check the workspace

1. Look for a `workspaces/` directory in the current project folder
2. If it exists, list any active projects (non-template subdirectories)
3. If it does not exist, explain that the user should clone the co-research template repo first:
   ```
   git clone https://github.com/terrene-foundation/co-research.git my-research
   ```
   Then open that folder in Cowork.

## Then explain the workflow

COR has five phases. Each phase has skills (commands) that guide the work:

| Phase | What happens | Skills |
|-------|-------------|--------|
| **01 Learn** | Understand the field, find literature, learn key debates | `/co-research:teach`, `/co-research:literature` |
| **02 Decide** | Make and record structural decisions about the paper | `/co-research:deliberate` |
| **03 Write** | Two modes: author-writes with AI critique, or AI-drafts with margin notes | `/co-research:craft`, `/co-research:write-para` |
| **04 Validate** | Verify claims, simulate hostile reviewers | `/co-research:validate-claim`, `/co-research:challenge` |
| **05 Publish** | Audit references, preflight check, prepare submission | `/co-research:check-refs`, `/co-research:preflight`, `/co-research:publish` |

Utility skills available anytime: `/co-research:ws` (status), `/co-research:wrapup` (save progress), `/co-research:checkpoint` (review learning).

## Then ask

1. What is the research topic or paper title?
2. Is this a new project or continuing existing work?
3. What is the target venue (journal, conference, working paper)?
4. What phase is the user in (or starting fresh)?

Based on answers, recommend the next skill to run.

## If continuing existing work

Read `.session-notes` if it exists to pick up context from the previous session. Summarize what was accomplished and what the next step is.
