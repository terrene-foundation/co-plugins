---
name: exam-prep
description: "Create a comprehensive exam preparation plan"
---

## Purpose

Create a structured exam preparation plan: topic checklists, formula sheets, practice problems, study schedules, and weak-area identification.

## Input

`$ARGUMENTS` contains the course name, exam details, or topics to cover.

If `$ARGUMENTS` is empty, ask: "What exam are you preparing for? Share the course name, exam date (if known), topics covered, and any study materials you have."

## Workflow

### Step 1 — Map the Exam Scope

Identify: topics covered, topic weights (if known), question types (MC, short answer, calculations, essays), allowed resources, and time limit.

Route to the appropriate course tutor (fnce101-tutor, corporate-finance-tutor, international-finance-tutor, or fmi-tutor).

### Step 2 — Create Topic Checklist

For each exam topic, create a checklist covering:
- **Concepts to know** — can you define and apply each one?
- **Formulas to know** — can you write from memory and solve in under 3 minutes?
- **Skills to demonstrate** — can you apply to an unseen problem and explain your reasoning?
- **Self-test question** — one question to check true understanding

### Step 3 — Build Formula Sheet

Create a compact formula sheet grouped by topic. For each formula: define every variable (with units), note when to use it, and highlight common confusions. If the exam provides a formula sheet, focus on what is NOT provided.

### Step 4 — Generate Practice Problems

For each topic, generate 3-5 practice problems at mixed difficulty (easy, medium, hard). Include detailed solutions. Use the same approach as `/practice`.

### Step 5 — Create Study Schedule

Build a day-by-day study plan based on the exam date:
- Space topics out (no single-topic cramming)
- Interleave practice across topics in later sessions
- Build in review days for earlier topics
- Final days: targeted review only, not new learning
- Include rest before the exam

### Step 6 — Identify Weak Areas

After the student works through problems, identify: topics with consistent errors, error types (computational, conceptual, formula selection), prerequisite gaps, and specific review recommendations.

## Exam Day Tips

- **Time management**: divide time by questions; skip and return to hard ones
- **Read carefully**: underline what the question asks before calculating
- **Show work**: partial credit comes from the right approach, even with wrong numbers
- **Sanity check**: negative stock prices, 500% annual returns, or negative WACC should trigger a re-check
