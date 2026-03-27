---
name: exam-prep
description: "Create a comprehensive exam preparation plan"
---

## Purpose

Create a comprehensive exam preparation plan for a finance course. Covers topic checklists, formula sheets, practice problems organized by topic, study schedules, and weak-area identification. Designed to make exam preparation structured and efficient.

## Input

`$ARGUMENTS` contains the course name, exam details, or topics to cover. Examples: "FNCE101 midterm covering chapters 1-6", "corporate finance final — WACC, capital budgeting, M&A", "international finance exam on exchange rates and balance of payments".

If `$ARGUMENTS` is empty, ask the student: "What exam are you preparing for? Please share: the course name, exam date (if known), topics covered, and any study materials or past exams you have access to."

## Workflow

### Step 1 — Map the Exam Scope

Based on the student's input, identify:

- **Topics covered**: List every topic on the exam
- **Topic weights**: If known, how much of the exam each topic represents
- **Question types**: Multiple choice, short answer, calculations, essays, case studies
- **Allowed resources**: Open book? Formula sheet provided? Calculator type?
- **Time limit**: How much time per question?

Route to the appropriate course tutor for domain expertise:

| Course Area | Tutor Agent |
|---|---|
| Introductory finance | **fnce101-tutor** |
| Corporate finance | **corporate-finance-tutor** |
| International finance | **international-finance-tutor** |
| Investments / portfolio / derivatives | **fmi-tutor** |

### Step 2 — Create Topic Checklist

For each exam topic, create a checklist the student can work through:

```
## Topic: [Name]

### Concepts to Know
- [ ] [Concept 1] — Can you define it in one sentence?
- [ ] [Concept 2] — Can you explain when and why it is used?
- [ ] [Concept 3] — Can you identify it in a new scenario?

### Formulas to Know
- [ ] [Formula 1] — Can you write it from memory and define every variable?
- [ ] [Formula 2] — Can you use it to solve a problem in under 3 minutes?

### Skills to Demonstrate
- [ ] [Skill 1] — Can you apply this to a problem you have not seen before?
- [ ] [Skill 2] — Can you explain your answer, not just compute it?

### Self-Test Question
[A single question the student can use to check if they truly understand this topic]
```

### Step 3 — Build Formula Sheet

Create a compact, well-organized formula sheet covering all exam topics:

- Group formulas by topic
- Define every variable (with units)
- Note when to use each formula
- Highlight formulas that are commonly confused with each other
- If the exam provides a formula sheet, focus the student's sheet on what is NOT provided

Format for quick reference during study:
```
## [Topic]

**[Formula Name]**
Formula: [expression]
Variables: [definitions with units]
Use when: [one-sentence description of when to apply]
Watch out: [common mistake]
```

### Step 4 — Generate Practice Problems by Topic

For each exam topic, generate 3-5 practice problems:

- At least one at each difficulty level (easy, medium, hard)
- At least one that matches the expected exam question format
- Include detailed solutions (hidden until the student attempts)
- Flag problems that test the most commonly examined aspects of each topic

Use the same problem generation approach as the `/practice` command.

### Step 5 — Create Study Schedule

Based on the exam date and number of topics, create a day-by-day study plan:

```
Day 1: Review [Topic 1] — read notes, complete topic checklist
Day 2: Practice problems for [Topic 1] — solve without notes
Day 3: Review [Topic 2] — read notes, complete topic checklist
Day 4: Practice problems for [Topics 1-2] — mixed problem set
...
Day N-2: Full practice exam under timed conditions
Day N-1: Review weak areas only — targeted practice
Day N: Light review of formula sheet, rest before exam
```

Principles:
- Space topics out (do not cram one topic in one sitting)
- Interleave practice (mix topics in later sessions)
- Build in review days to revisit earlier topics
- Final days are for targeted review, not new learning
- Include rest — exhausted students perform worse

### Step 6 — Identify Weak Areas

After the student works through practice problems, identify:

- Topics where they consistently make errors
- Types of errors (computational, conceptual, formula selection)
- Prerequisite gaps that underlie the errors
- Specific recommendations for what to review

Offer targeted practice for weak areas.

## Exam Day Tips

Include practical advice:

- **Time management**: Divide total time by number of questions; skip and return to hard ones
- **Read carefully**: Underline what the question is actually asking before calculating
- **Show your work**: Partial credit comes from showing the right approach, even if the final number is wrong
- **Sanity check**: Does your answer make sense? (A negative stock price, a 500% annual return, or a negative WACC should trigger a re-check)
- **Formula sheet**: If allowed, prepare it in advance and practice using it

## Agent Team

- **exam-coach** — Study plan design, problem generation, weak area analysis
- Appropriate **course tutor** — Domain expertise and problem verification
- **quantitative-analyst** — Verify all solutions and calculations
- **financial-literacy-expert** — Conceptual explanations for weak areas

## Skill References

- `17-exam-preparation/` — Exam preparation strategies
- `19-formula-reference/` — Formula quick reference (if populated)
- Relevant domain module from `.claude/skills/` based on course topics
