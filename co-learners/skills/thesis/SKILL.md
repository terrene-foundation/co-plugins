---
name: thesis
description: "Plan a thesis or research paper — question, argument, methodology, structure"
---

## Purpose

Plan a thesis or research paper from question to structure. Helps the student refine their research question, identify their contribution, select methodology, and plan the paper structure.

## Input

`$ARGUMENTS` contains the paper topic or research area.

If `$ARGUMENTS` is empty, ask: "What topic or research area is your thesis about?"

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project, use `workspaces/$ARGUMENTS/`
2. Otherwise, use most recently modified under `workspaces/` (excluding `_template/`)

## Protocol

1. **Refine the research question** — is it specific, researchable, significant?
2. **Identify the contribution** — what new argument or analysis does this paper offer?
3. **Select methodology** — what approach fits the question? (analytical, empirical, comparative, case study, qualitative, mixed methods)
4. **Plan the structure** — sections, argument flow, evidence placement
5. **Create a timeline** — milestones with realistic deadlines
6. **Save to `02-outline/`**

## Approval Gate

Present the complete plan. Ask:

- Is the research question focused enough?
- Does the methodology match your assignment requirements?
- Is the timeline realistic given your other commitments?

## Journal Entry

Record structural decisions in `journal/`. Type: DECISION.
