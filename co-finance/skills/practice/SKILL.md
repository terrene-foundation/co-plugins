---
name: practice
description: "Generate practice problems with step-by-step solutions"
---

## Purpose

Generate practice problems for a finance topic with step-by-step solutions. Follows a teach-then-test pattern: present problems, let the student attempt them, then reveal detailed solutions. Adapts difficulty based on student performance.

## Input

`$ARGUMENTS` contains the topic and optionally the difficulty level. Format: `<topic>` or `<topic> <difficulty>`.

Examples:
- "time value of money" — generates problems at mixed difficulty levels
- "bond pricing easy" — generates beginner-level problems
- "options pricing hard" — generates advanced problems
- "WACC" — generates problems at mixed difficulty levels

**Difficulty levels**: easy, medium, hard (or beginner, intermediate, advanced).

If `$ARGUMENTS` is empty, ask the student: "What topic would you like to practice? You can also specify a difficulty level (easy, medium, hard). If you have an upcoming exam, tell me the topics it covers and I will create a mixed problem set."

## Workflow

### Step 1 — Generate Problem Set

Create a set of 5-8 problems following progressive difficulty:

**Easy (2-3 problems)** — Direct application
- Straightforward use of a single formula
- All required information is provided
- One-step or two-step calculation
- Purpose: Build confidence and verify basic understanding

**Medium (2-3 problems)** — Conceptual application
- Requires choosing the right approach (not just plugging in)
- May have an extra piece of information (student must identify what is relevant)
- May combine two related concepts
- Purpose: Test understanding, not just memorization

**Hard (1-2 problems)** — Exam-level complexity
- Multi-step problem combining several concepts
- May require assumptions or judgment calls
- May present a scenario where the student must identify the problem type
- Purpose: Prepare for exam conditions and real-world ambiguity

### Step 2 — Present Problems (Without Solutions)

Present all problems clearly with:
- Problem number and difficulty label
- Complete problem statement with all necessary data
- Specific instruction on what to calculate or analyze
- Clear units expected in the answer

Do NOT show solutions at this stage. Tell the student: "Try these problems and share your answers or working when you are ready. I will check your work and then show you the full solutions."

### Step 3 — Check Student Work

When the student shares their attempt:

- **If correct**: Confirm the answer, note anything they did especially well, and mention any alternative approaches
- **If partially correct**: Identify exactly where they went off track. Do not just say "wrong" — show where the error occurred and guide them to fix it
- **If incorrect**: Walk through the first step together, then let them try again before revealing the full solution
- **If stuck**: Provide a hint that points them toward the right approach without giving away the answer. Example: "Think about what rate you need to use — is the 8% quoted as annual or semi-annual?"

### Step 4 — Reveal Detailed Solutions

For each problem, provide:

```
Problem [N] Solution

Given: [List all known values with their labels]
Find: [What we are solving for]
Formula: [The formula used, with source citation]

Step 1: [Description of what this step does]
  [Calculation with intermediate values shown]

Step 2: [Description of what this step does]
  [Calculation with intermediate values shown]

...

Answer: [Final answer with proper units and interpretation]

Key Insight: [One sentence on what this problem teaches]
```

### Step 5 — Identify Weak Areas

After reviewing the student's work across all problems, identify patterns:

- Which types of problems did they get right consistently?
- Where did they struggle? (formula selection, calculation, interpretation)
- Are there prerequisite gaps? (e.g., struggling with annuity problems might indicate a gap in TVM basics)

Offer: "Would you like more practice on [weak area]? Or shall we move to a different topic?"

## Problem Design Guidelines

- Use realistic numbers (not round numbers that make the math trivially easy)
- Provide context (company names, dates, market conditions) to make problems feel real
- Include units in all given data and require units in answers
- For calculation problems, state the required precision (e.g., "round to 2 decimal places")
- Include at least one problem that tests conceptual understanding, not just calculation
- Ensure all problems have unambiguous, deterministic answers

## Agent Team

- **exam-coach** — Problem generation, difficulty calibration, weak area identification
- Appropriate **course tutor** — Domain expertise for problem accuracy
- **quantitative-analyst** — Verify all solutions and numerical accuracy
- **financial-literacy-expert** — For the "Key Insight" and conceptual explanations

## Skill References

- `17-exam-preparation/` — Exam preparation strategies
- `19-formula-reference/` — Formula quick reference (if populated)
- Relevant domain module from `.claude/skills/` based on topic
