---
name: map-outcomes
description: Map learning outcomes across a course or program, identifying gaps and alignment issues.
argument-hint: "[course or program name]"
---

# /map-outcomes $ARGUMENTS

Map learning outcomes for **$ARGUMENTS**.

## Protocol

1. **Gather learning outcomes** from course outlines, program specifications, or accreditation standards
2. **Build the outcome matrix** showing coverage across courses or assessments
3. **Identify gaps** where outcomes are not assessed
4. **Identify redundancies** where outcomes are assessed multiple times without progression
5. **Check progression** (Introduce, Develop, Master) across the program
6. **Save the map** to `03-work/`

## Output

Save to `03-work/outcome-map-[name].md`:

```markdown
# Learning Outcome Map: $ARGUMENTS
Date: [today]

## Program-Level Outcomes
1. [PLO1]
2. [PLO2]
...

## Coverage Matrix

| Program Outcome | Course 1 | Course 2 | Course 3 | ... |
|---|---|---|---|---|
| PLO1 | I | D | M | |
| PLO2 | | I | D | M |

Legend: I = Introduce, D = Develop, M = Master, blank = not addressed

## Gap Analysis
[Outcomes with no M-level coverage]

## Redundancy Analysis
[Outcomes assessed at the same level in multiple courses]

## Recommendations
[Specific suggestions for addressing gaps and redundancies]
```

## Next Step

After mapping outcomes, recommend `/design-assessment` to design assessments for any gaps, or `/design-course` to restructure the course architecture.
