---
name: outline
description: "Structure the assignment — stops for student approval before drafting begins"
---

## Purpose

Create a structured plan for the assignment based on research. This is the planning phase — no drafting begins until the student approves.

## Input

`$ARGUMENTS` contains the assignment or topic name.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `_template/`)

## Protocol

1. **Read research** from `01-research/`
2. **Read assignment brief** from `briefs/` if available
3. **Create outline** with sections, key arguments per section, and sources to use
4. **Present for approval** — show the student the full outline

## Output

Save to `02-outline/outline-[topic-slug].md`:

```markdown
# Outline: [Topic]

## Thesis / Central Argument

[One clear statement]

## Sections

1. [Section name] — [what this covers, ~word count]
   - Key argument: ...
   - Sources: ...
2. [Section name] — ...
   ...

## Methodology (if applicable)

[Approach to analysis]
```

## Approval Gate

**HARD GATE**: Do NOT proceed to drafting until the student approves.

Ask:

- Does this cover everything the assignment requires?
- Is the order logical for your argument?
- Should any section be added, removed, or reorganized?

## Journal Entry

Record planning decisions and rationale in `journal/`. Type: DECISION.
