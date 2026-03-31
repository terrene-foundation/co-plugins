---
name: draft
description: "Produce the work one section at a time — each section builds understanding"
---

## Purpose

Work through the approved outline, drafting one section at a time. The student makes the analytical decisions; the AI assists with structure, evidence integration, and clarity.

## Input

`$ARGUMENTS` contains the assignment or topic name.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `_template/`)

## Protocol

1. **Read the approved outline** from `02-outline/`
2. **Find the next incomplete section**
3. **Draft the section** — explain key choices, cite sources properly
4. **Teach while drafting** — the student should understand why every sentence is there
5. **Save to `03-drafts/`** and mark the section complete
6. **Report progress** — what's done, what's next

## Rules

- **One section at a time.** Do not draft the entire assignment in one pass.
- **Student decides.** If a section requires an analytical judgment (which evidence to prioritize, which interpretation to favor), ask the student.
- **Teach, don't just produce.** Every draft interaction should build the student's understanding of the subject and of writing.

## Journal Entry

Record significant decisions or trade-offs made during drafting in `journal/`.

## Next Step

When all sections are complete, recommend `/challenge` to stress-test the work.
