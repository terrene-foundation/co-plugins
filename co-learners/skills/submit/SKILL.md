---
name: submit
description: "Format and package your work for submission"
---

## Purpose

Package the finalized work and prepare for submission. Runs final validation against assignment requirements.

## Input

`$ARGUMENTS` contains the assignment or topic name.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `_template/`)

## Protocol

1. **Confirm review is complete** — check that 04-review/ has findings and critical issues are resolved
2. **Package the output** — ensure 05-output/ contains the finalized work
3. **Run final validation**:
   - All citations verified and properly formatted
   - Assignment requirements from briefs/ all addressed
   - Word count within limits (if specified)
   - Formatting meets submission requirements
4. **Pre-submission checklist**:
   - [ ] All critical review issues resolved
   - [ ] All citations are real and properly formatted
   - [ ] Assignment requirements fully addressed
   - [ ] Formatting matches submission requirements
   - [ ] Student has reviewed and approved the final version

## Approval Gate

**HARD GATE**: Student approves before submission. Ask:

- Does this cover everything your assignment requires?
- Is anything missing that you expected to include?
- Is the formatting correct for this submission?
- Are you satisfied this represents your best work?

## Journal Entry

Record what was submitted and any final notes in `journal/`. Type: DECISION.
