---
name: analyze
description: "Load phase 01 (analyze) for the current workspace"
---

## What This Phase Does (present to user)

Research and validate the initiative before execution begins. We study the landscape, evaluate the approach, identify stakeholders, and create a clear picture of what to deliver. Nothing gets created until this research is done.

## Your Role (communicate to user)

Review our research findings and confirm we understood your intent. You'll see an analysis of the initiative's strengths, who it affects, what risks exist, and a plan for execution. Tell us if anything is off or missing.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `instructions/`)
3. If no workspace exists, ask the user to create one first
4. Read all files in `workspaces/<project>/briefs/` for user context (this is the user's input surface)

## Phase Check

- Output goes into `workspaces/<project>/01-analysis/`, `workspaces/<project>/02-plans/`, and `workspaces/<project>/03-user-flows/`

## Workflow

### 1. Understand the initiative

Read the brief and any related existing documents in the knowledge base. Understand the intent before diving into research.

### 2. Research thoroughly

Document in detail in `workspaces/<project>/01-analysis/01-research`.

- Use as many subdirectories and files as required
- Name them sequentially as 01-, 02-, etc, for easy referencing
- Research may include: competitive landscape, governance precedents, regulatory context, partnership considerations, existing standards in the area

### 3. Cross-reference with existing knowledge base

Check alignment with existing project documentation, anchor documents, and any established standards or strategy documents relevant to this workspace.

### 4. Document analysis and plans

Document analysis in `workspaces/<project>/01-analysis/`, plans in `workspaces/<project>/02-plans/`.

- Use as many subdirectories and files as required
- Name them sequentially as 01-, 02-, etc, for easy referencing

### 5. Red team (internal quality check)

Work with agents to scrutinize analysis and plans:

- Identify any gaps, regardless how small
- Go back to first principles and identify the most robust approaches
- Analysis must flow logically into plans

### 6. Present findings to the user

Summarize the analysis in plain language. Cover:

- **What we're doing** — one paragraph describing the initiative
- **Who it affects** — stakeholders and their concerns
- **What the landscape looks like** — relevant precedents, regulations, or competing approaches
- **Proposed approach** — the recommended path forward with rationale
- **Risks and considerations** — anything the user should know, explained with impact

Ask the user: "Does this match your intent? Anything we got wrong, missed, or should rethink?"

## Agent Teams

Deploy these agents as a team for analysis:

**Core research team:**

- **deep-analyst** — Risk analysis, failure points, cascading effects
- **requirements-analyst** — Break down requirements, define scope

**Research co-authorship (invoke for publication-related work):**

- **literature-researcher** — Systematic literature discovery and assessment
- **field-expert** — Domain knowledge, historical context, debates
- **argument-critic** — Adversarial review, logical gap detection

Red team the analysis with agents until they confirm no gaps remain.
