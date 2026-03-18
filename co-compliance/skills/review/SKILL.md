---
name: review
description: Quality check and adversarial critique of compliance work. Finds missed requirements, incorrect mappings, and evidence gaps. Never says "this is fine."
argument-hint: "[what to review]"
---

# /review $ARGUMENTS

Review **$ARGUMENTS** with a critical eye. Find every missed requirement, incorrect mapping, evidence gap, and improvement opportunity.

## Protocol

1. **Read the work product** from `03-work/`
2. **Apply compliance quality standards**:
   - Are all applicable requirements captured?
   - Are regulatory citations accurate and current?
   - Do control mappings have clear rationale?
   - Is evidence referenced for every compliance claim?
   - Are gaps properly classified and prioritized?
3. **Cross-reference** against the requirements register to find missed items
4. **Never say "this is fine"** - always find at least one improvement

## Compliance-Specific Review Criteria

- **Completeness**: Are any requirements from applicable regulations missing?
- **Accuracy**: Are regulatory citations exact? Are section numbers correct?
- **Currency**: Are cited regulations the current version? Have any been amended?
- **Mapping quality**: Does each control mapping explain HOW the control satisfies the requirement?
- **Evidence sufficiency**: Is the evidence referenced actually sufficient to demonstrate compliance?
- **Gap severity**: Are gaps classified appropriately? Is a "Medium" really not a "High"?
- **Consistency**: Does the report contradict itself? Are the same requirements rated differently in different sections?

## Output

Save to `04-review/review-[topic-slug].md`:

```markdown
# Compliance Review: $ARGUMENTS
Date: [today]

## Critical Issues (must fix before any report is issued)
[Missed requirements, incorrect citations, misrepresented compliance status]

## Major Issues (should fix before audit)
[Weak control mappings, insufficient evidence, inconsistent ratings]

## Minor Issues (worth fixing)
[Formatting, clarity, organizational improvements]

## Strengths
[What works well - be specific]

## Recommendations
[Prioritized list of what to address first]
```

## Next Step

After the compliance officer addresses review findings, recommend `/finalize` to prepare the final deliverables.
