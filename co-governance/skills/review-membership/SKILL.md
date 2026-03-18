---
name: review-membership
description: Review a membership application or status change against constitutional criteria.
argument-hint: "[applicant name or membership action]"
---

# /review-membership $ARGUMENTS

Review the membership application or status change for: **$ARGUMENTS**

## Protocol

1. **Identify the membership action** (new application, suspension, termination, status change)
2. **Check constitutional eligibility criteria** for the relevant action type
3. **Assess independence** of the applicant or member
4. **Verify uniform contributor framework compliance** (no exclusive rights, no special access)
5. **Check guarantee obligations** (limited to $1)
6. **Document the review** with constitutional basis
7. **Delegate to membership-coordinator agent** for detailed review

## Output

Save the review to `03-work/membership-review-[slug].md` in the active workspace.

The review follows the Foundation's standard format:
- Applicant or member identification
- Eligibility check against constitutional criteria
- Independence assessment
- Uniform contributor framework compliance check
- Guarantee obligation verification
- Recommendation (Admit / Defer / Decline / Approve change / Reject change)
- Rationale with constitutional basis

## Rules

- No membership decision may create exclusive rights or special access for any member
- All membership decisions must be documented with constitutional basis
- Membership status changes must follow the procedures specified in the constitution
- The review is a recommendation for the governance officer. The AI does not make membership decisions.

## Next Step

Present the membership review to the governance officer for decision. If the recommendation is to defer, explain what additional information is needed.
