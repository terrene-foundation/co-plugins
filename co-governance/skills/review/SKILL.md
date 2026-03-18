---
name: review
description: Constitutional compliance check, independence audit, and transparency review of governance artifacts. Never says "this is fine."
argument-hint: "[what to review]"
---

# /review $ARGUMENTS

Review **$ARGUMENTS** for constitutional compliance, independence preservation, and transparency. Find every weakness, gap, error, and improvement opportunity.

## Protocol

1. **Read the governance artifacts** from `03-work/`
2. **Run constitutional compliance check** against all relevant clauses
3. **Check entrenched provision compliance** specifically
4. **Assess independence preservation** across all artifacts
5. **Evaluate transparency and documentation completeness**
6. **Never say "this is fine"** - always find at least one improvement
7. **Delegate to compliance-auditor agent** for the detailed audit

## Output

Save to `04-review/review-[topic-slug].md`:

```markdown
# Governance Review: $ARGUMENTS
Date: [today]

## Constitutional Compliance
[Clause-by-clause analysis of compliance]

## Critical Issues (constitutional violations)
[Must be remediated before finalization]

## Major Issues (governance risks)
[Should be remediated before finalization]

## Minor Issues (best practice gaps)
[Worth addressing for governance quality]

## Independence Assessment
[Does any artifact introduce commercial coupling or exclusive access?]

## Transparency Assessment
[Is the rationale documented? Could this be explained publicly?]

## Strengths
[What works well - be specific]

## Recommendations
[Prioritized list of what to fix first]
```

## Next Step

After the governance officer addresses review findings, recommend `/finalize` to prepare the final governance artifact.
