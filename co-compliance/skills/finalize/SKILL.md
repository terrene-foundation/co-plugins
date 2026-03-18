---
name: finalize
description: Polish, validate, and prepare final compliance deliverables. Last quality gate before delivery to management, auditors, or regulators.
---

# /finalize

Prepare the final compliance deliverables for delivery.

## Protocol

1. **Check all review issues are addressed** from `04-review/`
2. **Validate regulatory citations** - every citation must be accurate and current
3. **Verify evidence references** - every referenced artifact must exist
4. **Polish formatting** - consistency, professional presentation
5. **Save the final version** to `05-output/`

## Pre-delivery checklist

- [ ] All critical review issues resolved
- [ ] All major review issues resolved or documented as accepted risks
- [ ] Every regulatory citation includes regulation name, section, jurisdiction, effective date
- [ ] Every compliance claim references supporting evidence
- [ ] Scope and limitations are explicitly stated
- [ ] Report clearly marks assessed vs not assessed areas
- [ ] Compliance officer has approved the final version

## Output

Save to `05-output/` with a clear filename reflecting the deliverable type:
- `compliance-report-[regulation]-[date].md`
- `gap-analysis-[scope]-[date].md`
- `audit-package-[control-area]-[date].md`
- `requirements-register-[regulation]-[date].md`

Include a brief summary of what was produced, what it covers, and any known limitations.

## Journal Entry

Record what was learned during this compliance project in `journal/`:
- Regulatory interpretation decisions made
- Control mapping patterns that worked well
- Evidence collection challenges encountered
- Process improvements for next assessment cycle
