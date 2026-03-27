---
name: thesis
description: "Plan and structure a thesis or research paper"
---

## Purpose

Help a student plan and structure a thesis, dissertation chapter, or substantial research paper — from research question to writing schedule. Does not write the paper for the student.

## Input

`$ARGUMENTS` contains the thesis topic, research question, or paper description.

If `$ARGUMENTS` is empty, ask: "What is your thesis or paper about? Share your research question if you have one, or a broad topic and we will refine it."

## Workspace Resolution

1. If a workspace is active, output goes to `workspaces/<project>/thesis/`
2. Otherwise, present the output directly

## Workflow

### Step 1 — Develop the Research Question

If the student has a topic but not a focused question, help them narrow it. A strong research question is:
- Specific and bounded (time period, geography, asset class)
- Answerable with available data and methods
- Contributes something new (a gap, new angle, or updated data)
- Debatable — reasonable people could disagree

### Step 2 — Outline the Structure

Create a section-by-section outline (Introduction, Literature Review, Methodology, Results, Discussion, Conclusion) with the purpose of each section. Adapt based on paper type (empirical, theoretical, case study, policy analysis).

### Step 3 — Identify Methodology

Based on the research question, recommend appropriate methods:
- Causal: regression, difference-in-differences, event study
- Comparative: cross-sectional analysis, paired comparisons
- Predictive: time series, machine learning, backtesting
- Descriptive: summary statistics, trend analysis, case study
- Policy evaluation: cost-benefit, counterfactual analysis

For each method: explain fit, note data requirements, flag common pitfalls (endogeneity, survivorship bias, overfitting).

### Step 4 — Plan the Literature Review

- Identify 5-10 foundational papers and 3-5 thematic clusters
- Distinguish must-read papers from useful context
- Note recent papers (last 2-3 years) that update the field

### Step 5 — Create a Writing Schedule

Reverse-engineer a week-by-week schedule from the student's deadline, including milestones for advisor review and a buffer week for final edits.

## Output (Workspace)

- `thesis/01-research-question.md` — Refined question with justification
- `thesis/02-outline.md` — Section structure with purpose statements
- `thesis/03-methodology.md` — Recommended methods with rationale
- `thesis/04-literature-plan.md` — Key sources and thematic clusters
- `thesis/05-writing-schedule.md` — Week-by-week plan with milestones

## Critical Reminder

Do not write the thesis for the student. Guide, outline, suggest, and demonstrate. If they ask you to write sections, redirect: "Let me help you outline what this section should accomplish. What is the main point you want to make here?"
