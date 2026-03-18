---
name: design-assessment
description: Design an assessment task aligned to specific learning outcomes that tests genuine understanding and resists trivial AI completion.
argument-hint: "[learning outcome or assessment context]"
---

# /design-assessment $ARGUMENTS

Design an assessment task for **$ARGUMENTS**.

## Protocol

1. **Identify the learning outcomes** this assessment must test
2. **Determine the assessment type** (exam, essay, project, portfolio, presentation, practical)
3. **Design the task** with clear instructions, conditions, and AI use policy
4. **Analyze AI-resilience**: run the task description through an AI-resilience check
5. **Draft the companion rubric** (defer to rubric-builder for complex rubrics)
6. **Save the assessment** to `03-work/`

## Assessment Specification Template

```markdown
# Assessment: [Name]
Course: [Course code and name]
Weight: [% of final grade]
Due: [Date or week]

## Learning Outcomes Assessed
- LO1: [Outcome]
- LO2: [Outcome]

## Task Description
[Clear, specific instructions for students]

## Conditions
- Time: [Duration or deadline]
- Resources: [What students may use]
- Collaboration: [Individual / group / pair]
- AI Policy: [Prohibited / permitted with disclosure / required with reflection]

## Submission Requirements
[Format, length, components]

## Rubric
[See companion rubric document]

## AI-Resilience Analysis
[How does this assessment perform if a student uses AI? What modifications make it more resilient?]
```

## Next Step

After designing the assessment, recommend `/build-rubric` to create the detailed rubric, or `/audit-ai-resilience` to stress-test the design.
