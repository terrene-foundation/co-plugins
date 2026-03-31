---
name: practice
description: "Generate practice problems with step-by-step solutions"
---

## Purpose

Generate practice problems for a finance topic with step-by-step solutions. Present problems, let the student attempt them, then reveal detailed solutions. Adapts difficulty based on performance.

## Input

`$ARGUMENTS` contains the topic and optionally a difficulty level (easy/medium/hard).

If `$ARGUMENTS` is empty, ask: "What topic would you like to practice? You can also specify a difficulty level (easy, medium, hard)."

## Workflow

### Step 1 — Generate Problem Set

Create 5-8 problems with progressive difficulty:
- **Easy (2-3)**: Direct application of a single formula; all info provided; builds confidence
- **Medium (2-3)**: Requires choosing the right approach; may include irrelevant data or combine two concepts
- **Hard (1-2)**: Multi-step, combining several concepts; may require assumptions or identifying the problem type

### Step 2 — Present Problems (Without Solutions)

Present with: problem number, difficulty label, complete statement with all data, specific instruction on what to calculate, and expected units. Do NOT show solutions yet.

### Step 3 — Check Student Work

- **Correct**: Confirm, note what was done well, mention alternative approaches
- **Partially correct**: Identify exactly where they went off track and guide the fix
- **Incorrect**: Walk through the first step together, then let them retry
- **Stuck**: Provide a hint toward the right approach without giving the answer

### Step 4 — Reveal Detailed Solutions

For each problem: list given values, state what to find, show the formula, walk through each step with intermediate values, state the answer with units and interpretation, and include a key insight.

### Step 5 — Identify Weak Areas

Identify patterns: which problem types succeeded, where they struggled (formula selection, calculation, interpretation), prerequisite gaps. Offer targeted practice.

## Problem Design Guidelines

- Use realistic numbers (not trivially round)
- Provide context (company names, dates, market conditions)
- Include units in all data and require units in answers
- Include at least one conceptual (not just calculation) problem
- Ensure all problems have unambiguous answers
