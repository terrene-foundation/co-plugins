---
name: analyze
description: "Load phase 01 (analyze) — research and analyze a topic before writing begins"
---

## What This Phase Does

Research and analyze your topic in depth before any writing begins. Find sources, identify theories and debates, map the literature, and build a clear picture of the intellectual landscape.

## Your Role (Student)

Review the research findings and confirm the direction. Tell us if anything is off, missing, or if you want a different angle.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `instructions/`)
3. If no workspace exists, ask the student to create one first
4. Read all files in `workspaces/<project>/briefs/` for student context

## Phase Check

Output goes into `workspaces/<project>/01-analysis/`, `02-plans/`, and `03-structure/`.

## Workflow

### 1. Understand the assignment

Clarify: what is being asked (essay, case study, thesis, presentation), the research question, course and level, professor's requirements (length, sources, format), and deadline.

### 2. Deep research

Document in `01-analysis/01-research/` using subdirectories and sequential naming (01-, 02-, etc). Identify seminal papers, textbooks, key authors, empirical data, case studies, competing theories, and relevant data sources (FRED, World Bank, Bloomberg).

### 3. Organize themes and gaps

Identify major themes, areas of agreement and disagreement, gaps in current research, relevant theoretical frameworks, strength of evidence, and counterarguments to address.

### 4. Create outline

Build a proposed structure in `02-plans/` and `03-structure/`:
- Thesis statement or central argument
- Logical section flow, each building on the previous
- Evidence and sources mapped to sections
- Where data analysis or calculations are needed
- How counterarguments will be addressed

### 5. Red team for gaps

Review critically: missing perspectives or sources, logical soundness, weak points a professor would challenge, sufficient evidence for each claim, credible and academic sources.

### 6. Present findings to student

Summarize in plain language: your topic (restated), what the literature says, key debates, proposed approach, sources collected, and gaps/considerations. Ask: "Does this cover your topic? Is the direction right? Anything to add, remove, or rethink?"
