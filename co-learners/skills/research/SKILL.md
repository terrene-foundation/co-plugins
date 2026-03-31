---
name: research
description: "Start a structured research workflow for any academic topic"
---

## Purpose

Guide a student through structured research — from forming a question to producing an annotated bibliography and synthesis. For students working on papers, literature reviews, or thesis proposals in any discipline.

## Input

`$ARGUMENTS` contains the research topic or question.

If `$ARGUMENTS` is empty, ask: "What topic or question would you like to research? Broad or narrow is fine — I will help you refine it."

## Workspace Resolution

1. If a workspace is active, output goes to `workspaces/<project>/01-research/`
2. Otherwise, present the output directly

## Workflow

### Step 1 — Define the Research Question

Sharpen a vague topic into a focused, answerable question:
- What is the specific scope? (time period, geography, population, context)
- What variable, event, or factor is being examined?
- What baseline or comparison is relevant?
- What outcome or understanding is being sought?

Test: researchable in a semester? Enough sources available?

### Step 2 — Identify Source Types

Based on the question, recommend source types: academic journals, working papers, textbooks, institutional reports, primary sources, news (for current events only). Minimum sources: UG 8-12, PG 15-25.

### Step 3 — Evaluate Sources (CRAAP Test)

Teach the student to evaluate each source: Currency, Relevance, Authority, Accuracy, Purpose.

### Step 4 — Organize by Theme

Identify 3-5 major themes, map sources to themes, identify gaps, and note areas of agreement and disagreement.

### Step 5 — Synthesize Findings

Guide a synthesis narrative: what the literature collectively says, where scholars agree/disagree, dominant methodological approaches, and gaps the student's research could address.

### Step 6 — Create Annotated Bibliography

For each source: formatted citation, 2-3 sentence summary, 1-2 sentence evaluation, and relevance to the research question.

## Output (Workspace)

- `01-research/01-research-question.md` — Refined question with scope
- `01-research/02-source-plan.md` — Source types and search strategy
- `01-research/03-source-evaluation.md` — CRAAP evaluations
- `01-research/04-thematic-analysis.md` — Sources organized by theme
- `01-research/05-synthesis.md` — Narrative synthesis
- `01-research/06-annotated-bibliography.md` — Formatted bibliography
