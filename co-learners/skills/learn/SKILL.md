---
name: learn
description: "Reflect on what you learned — extract knowledge into the COL system"
---

## Purpose

Reflect on the project and capture what was learned — both for the student and for the system. Phase 05 output goes into .claude/ (the COL system itself), not the workspace.

## Input

`$ARGUMENTS` contains the assignment or topic name.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `_template/`)

## Protocol

1. **Review the full project trail** — read journal/, 04-review/, 03-drafts/
2. **Reflect with the student**:
   - What concepts did you master?
   - What's still unclear?
   - What study strategies worked?
   - What connections did you discover between topics?
3. **Identify patterns worth keeping**:
   - Writing structures that worked well -> skills
   - Research strategies that proved effective -> skills
   - Quality standards learned from review -> rules
   - Recurring workflow improvements -> commands
4. **For each proposed upgrade**, present:
   - What it is and why it matters
   - Where it would go in .claude/
   - Draft content
5. **Student approves each proposal** before any .claude/ modification

## What /learn Produces

Output goes into the COL system itself, not the workspace:

```
.claude/
  skills/      <- new or refined knowledge
  rules/       <- new or refined quality standards
  commands/    <- refined workflows
```

Next assignment, the system is stronger. The tenth assignment benefits from the first nine.

## Approval Gate

**HARD GATE**: The system proposes. The student disposes. No pattern becomes institutional knowledge without explicit student approval.

## Journal Entry

Record what was learned and what was upgraded in `journal/`. Type: DISCOVERY or DECISION.
