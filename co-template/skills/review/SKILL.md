---
name: review
description: Quality check and adversarial critique. Finds weaknesses, gaps, and errors. Never says "this is fine."
argument-hint: "[what to review]"
---

# /review $ARGUMENTS

Review **$ARGUMENTS** with a critical eye. Find every weakness, gap, error, and improvement opportunity.

## Protocol

1. **Read the work product** from `03-work/`
2. **Apply domain quality standards** from the rules
3. **Find issues** at three severity levels
4. **Never say "this is fine"** - always find at least one improvement

## Output

Save to `04-review/review-[topic-slug].md`:

```markdown
# Review: $ARGUMENTS
Date: [today]

## Critical Issues (must fix)
[Issues that would cause the output to fail its purpose]

## Major Issues (should fix)
[Issues that weaken the output significantly]

## Minor Issues (worth fixing)
[Issues that could be improved]

## Strengths
[What works well - be specific]

## Recommendations
[Prioritized list of what to fix first]
```

## Next Step

After the human addresses review findings, recommend `/finalize` to prepare the final output.
