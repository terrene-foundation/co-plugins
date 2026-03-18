---
name: design-course
description: Design or restructure a course's assessment architecture for alignment, progression, and AI-resilience.
argument-hint: "[course name or code]"
---

# /design-course $ARGUMENTS

Design the assessment architecture for **$ARGUMENTS**.

## Protocol

1. **Gather course information**: learning outcomes, credit points, student cohort size, delivery mode, semester structure
2. **Design the assessment portfolio**: a set of assessments that collectively cover all learning outcomes
3. **Ensure progression**: assessments should build in complexity across the semester
4. **Balance assessment types**: mix formative and summative, individual and group, written and oral
5. **Check total workload**: the combined assessment load must be proportionate to credit points
6. **Apply AI-resilience principles** to each assessment in the portfolio
7. **Save the course design** to `03-work/`

## Course Assessment Architecture Template

```markdown
# Course Assessment Architecture: $ARGUMENTS
Date: [today]

## Course Information
- Code: [Code]
- Title: [Title]
- Credit points: [N]
- Cohort size: [N students]
- Delivery: [On-campus / online / hybrid]
- Semester: [Duration and structure]

## Learning Outcomes
1. [LO1]
2. [LO2]
...

## Assessment Portfolio

| # | Assessment | Type | Weight | Due | LOs Assessed | AI Policy |
|---|---|---|---|---|---|---|
| 1 | [Name] | [Type] | [%] | [Week] | LO1, LO3 | [Policy] |
| 2 | [Name] | [Type] | [%] | [Week] | LO2, LO4 | [Policy] |

Weights must sum to 100%.

## Assessment Progression
[How assessments build on each other across the semester]

## Workload Analysis
[Estimated student hours per assessment, total hours vs credit point expectations]

## AI-Resilience Summary
[Overall course-level strategy for assessment integrity in the GenAI era]

## Formative Assessment Plan
[Non-graded activities that prepare students for summative assessments]
```

## Next Step

After designing the course architecture, recommend `/design-assessment` for each individual assessment, then `/build-rubric` for each rubric.
