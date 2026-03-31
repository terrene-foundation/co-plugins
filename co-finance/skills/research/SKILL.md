---
name: research
description: "Start a structured research workflow for a finance topic"
---

## Purpose

Guide a student through structured research — from forming a question to producing an annotated bibliography and synthesis. For UG/PG finance students working on papers, literature reviews, or thesis proposals.

## Input

`$ARGUMENTS` contains the research topic or question.

If `$ARGUMENTS` is empty, ask: "What topic or question would you like to research? Broad or narrow is fine — I will help you refine it."

## Workspace Resolution

1. If a workspace is active, output goes to `workspaces/<project>/research/`
2. Otherwise, present the output directly

## Workflow

### Step 1 — Define the Research Question

Sharpen a vague topic into a focused, answerable question using PICO adapted for finance:
- **P**opulation: which market, firms, or time period?
- **I**ntervention/Factor: what variable or event?
- **C**omparison: what baseline or alternative?
- **O**utcome: what is being measured?

Test: researchable in a semester? Enough sources available?

### Step 2 — Identify Source Types

Based on the question, recommend source types: academic journals, working papers (SSRN, NBER), textbooks, industry reports (McKinsey, IMF), news (FT, WSJ), data sources (WRDS, FRED, Bloomberg). Minimum sources: UG 8-12, PG 15-25.

### Step 3 — Evaluate Sources (CRAAP Test)

Teach the student to evaluate each source: Currency, Relevance, Authority, Accuracy, Purpose.

### Step 4 — Organize by Theme

Identify 3-5 major themes, map sources to themes, identify gaps, and note areas of agreement and disagreement.

### Step 5 — Synthesize Findings

Guide a synthesis narrative: what the literature collectively says, where scholars agree/disagree, dominant methodological approaches, and gaps the student's research could address.

### Step 6 — Create Annotated Bibliography

For each source: formatted citation, 2-3 sentence summary, 1-2 sentence evaluation, and relevance to the research question.

## Output (Workspace)

- `research/01-research-question.md` — Refined question with scope
- `research/02-source-plan.md` — Source types and search strategy
- `research/03-source-evaluation.md` — CRAAP evaluations
- `research/04-thematic-analysis.md` — Sources organized by theme
- `research/05-synthesis.md` — Narrative synthesis
- `research/06-annotated-bibliography.md` — Formatted bibliography
