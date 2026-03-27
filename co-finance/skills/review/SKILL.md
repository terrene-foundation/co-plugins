---
name: review
description: "Peer review of academic writing for argument strength and citations"
---

## Purpose

Provide structured peer review feedback on academic writing — evaluating argument strength, evidence quality, citation accuracy, logical flow, and formatting compliance.

## Input

`$ARGUMENTS` contains a file path to the draft, or the student can paste text directly.

If `$ARGUMENTS` is empty, ask: "Please share the writing you would like reviewed. You can paste text or point to a file. Also let me know the citation style (APA, Chicago, Harvard) and assignment type."

## Workflow

### Step 1 — Read and Understand

Read the entire document. Identify: paper type, thesis statement, citation style, approximate word count, and number of sources.

### Step 2 — Evaluate Argument Strength

Assess each major section for:
- **Thesis**: Clear, debatable, specific? Does the conclusion deliver on it?
- **Evidence**: Every claim supported? Sources credible, current, relevant? Any orphan statistics?
- **Analysis vs. Description**: Does the student explain *why* and *what it means*, not just summarize?
- **Counterarguments**: Acknowledged and addressed fairly?
- **Logical flow**: Each paragraph follows from the previous? Transitions clear?

### Step 3 — Check Citation Quality

Flag: missing citations for factual claims, in-text citations without reference list entries (and vice versa), inconsistent formatting, over-reliance on a single source, absence of seminal sources.

### Step 4 — Check Formatting

Citation style consistency, headings/tables/figures formatting, word count compliance, disclaimers for finance content, documented methodology for quantitative content.

### Step 5 — Produce Feedback Report

Structure as:
- **Overall Assessment** — 1-2 paragraphs on strengths and areas for improvement
- **Strengths** — specific things done well
- **Areas for Improvement** — organized by: Argument/Analysis, Structure/Flow, Citations/Sources, Writing Quality
- **Specific Comments** — paragraph-level feedback on key issues
- **Recommended Next Steps** — prioritized list of revisions

## Critical Rules

1. **Be specific.** Not "your argument is weak" but "in paragraph 3, you claim diversification eliminates risk, but Markowitz (1952) says *unsystematic* risk."
2. **Balance criticism with recognition.** Always identify what works before discussing improvements.
3. **Explain the why.** Not just "add more citations" but why the reader needs them.
4. **Prioritize.** Distinguish critical revisions from suggestions.
5. **Do not rewrite.** Identify problems and suggest approaches, but the student produces their own text.
