---
name: audit-compliance
description: Audit governance actions and artifacts for constitutional compliance, independence preservation, and transparency.
argument-hint: "[what to audit, e.g. 'recent governance decisions' or 'membership process']"
---

# /audit-compliance $ARGUMENTS

Audit **$ARGUMENTS** for constitutional compliance, independence preservation, and transparency.

## Protocol

1. **Identify the audit scope** from the user's description
2. **Gather the governance artifacts** to be audited from workspace directories
3. **Check constitutional compliance** for each action or artifact
4. **Assess independence preservation** across all audited items
5. **Evaluate transparency** of documentation, rationale, and process
6. **Classify findings** by severity: Critical, Major, Minor
7. **Delegate to compliance-auditor agent** for the detailed audit

## Output

Save the audit report to `04-review/compliance-audit-[slug].md` in the active workspace.

The audit follows the Foundation's standard format:
- Critical Issues (constitutional violations, must remediate immediately)
- Major Issues (compliance risks, should remediate before next governance cycle)
- Minor Issues (best practice gaps, worth addressing)
- Independence Assessment
- Transparency Assessment
- Prioritized Recommendations

## Rules

- Never say "this is fine." Every audit finds at least one improvement.
- Be specific: cite clause numbers, name the exact risk, describe the precise gap
- Every finding includes a specific remediation recommendation
- Critical findings are reported immediately, not deferred to the report

## Next Step

Present the audit findings to the governance officer. For critical issues, recommend immediate remediation before any further governance actions.
