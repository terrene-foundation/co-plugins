---
name: build-rubric
description: Build a transparent, criterion-referenced rubric for an assessment task.
argument-hint: "[assessment name or learning outcomes]"
---

# /build-rubric $ARGUMENTS

Build a rubric for **$ARGUMENTS**.

## Protocol

1. **Read the assessment specification** from `03-work/` if it exists
2. **Identify the criteria** derived from the learning outcomes
3. **Define performance levels** (typically 4-5 levels)
4. **Write descriptors** for each criterion at each performance level
5. **Assign weightings** that reflect the relative importance of each criterion
6. **Save the rubric** to `03-work/`

## Rubric Template

```markdown
# Rubric: [Assessment Name]

## How to Use This Rubric

This rubric shows exactly how your work will be assessed. Read it before you start.
Each criterion has [N] performance levels. Your mark for each criterion is based on
which level best describes your work. The weightings show how much each criterion
contributes to your overall mark.

## Rubric Table

| Criterion (Weight) | Excellent (90-100%) | Good (75-89%) | Satisfactory (50-74%) | Developing (25-49%) | Inadequate (0-24%) |
|---|---|---|---|---|---|
| **[Criterion 1]** ([X]%) | [Descriptor] | [Descriptor] | [Descriptor] | [Descriptor] | [Descriptor] |
| **[Criterion 2]** ([X]%) | [Descriptor] | [Descriptor] | [Descriptor] | [Descriptor] | [Descriptor] |

## Notes
[Any additional guidance for students or markers]
```

## Quality Checks

- Descriptors are behavioral and observable, not comparative ("demonstrates X" not "better than Y")
- Adjacent performance levels are distinguishable (a marker can tell them apart)
- Criteria are independent (no double-counting)
- Weightings sum to 100%
- All criteria trace back to stated learning outcomes
