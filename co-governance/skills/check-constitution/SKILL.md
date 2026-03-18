---
name: check-constitution
description: Check a proposed governance action or decision against the Foundation's 77-clause constitution.
argument-hint: "[proposed action or decision]"
---

# /check-constitution $ARGUMENTS

Check the proposed governance action **$ARGUMENTS** against the Foundation's 77-clause constitution.

## Protocol

1. **Identify the proposed action** from the user's description
2. **Map to relevant constitutional clauses** covering this type of action
3. **Check entrenched provisions first** (11 provisions requiring 75% supermajority)
4. **Analyze ordinary clauses** that apply
5. **Identify ambiguities** where constitutional interpretation is needed
6. **Delegate to constitution-checker agent** for detailed analysis

## Output

Present a structured compliance assessment:

```markdown
# Constitutional Compliance Check
## Proposed Action: $ARGUMENTS
## Date: [today]
## Status: [Compliant | Non-compliant | Requires Interpretation]

## Entrenched Provisions
[Which of the 11 entrenched provisions are affected, if any. If none, state "No entrenched provisions affected."]

## Relevant Clauses
| Clause | Description | Compliance |
|--------|-------------|------------|
| [N] | [Brief description] | [Compliant / Non-compliant / Ambiguous] |

## Analysis
[Detailed analysis of how the proposed action interacts with constitutional provisions]

## Recommendations
[How to proceed. If non-compliant, how to modify the action to achieve compliance.]
```

## Rules

- Entrenched provisions are checked first, always
- If any entrenched provision is violated, the verdict is Non-compliant regardless of other factors
- Ambiguous cases must be flagged for officer interpretation, not resolved by the AI
- Every check must produce a written record saved to the workspace

## Next Step

If compliant, recommend proceeding with the governance action. If non-compliant, recommend modifications. If ambiguous, present the interpretive question to the governance officer.
