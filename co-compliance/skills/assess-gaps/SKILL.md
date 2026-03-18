---
name: assess-gaps
description: Identify and prioritize gaps between regulatory requirements and current controls.
argument-hint: "[scope of gap assessment, e.g., 'GDPR assessment', 'all unmapped requirements']"
---

# /assess-gaps $ARGUMENTS

Assess compliance gaps for **$ARGUMENTS**.

## Protocol

1. **Find the active workspace**
2. **Read control mappings** from `03-work/` to identify "Partial" and "None" coverage items
3. **Assess each gap** for severity, risk, and remediation priority
4. **Identify compound gaps** where multiple individual gaps create a larger exposure
5. **Recommend remediation approaches** with effort estimates
6. **Save the gap analysis** to `03-work/`

## Output

Save to `03-work/gap-analysis-[scope-slug].md`:

```markdown
# Gap Analysis: $ARGUMENTS
Date: [today]
Scope: [What was assessed]
Source: [Reference to control mapping documents]

## Gap Summary
| Gap ID | Requirement | Severity | Remediation Effort | Priority |
|--------|------------|----------|-------------------|----------|
| GAP-001 | REQ-NNN | Critical | High | Immediate |
| GAP-002 | REQ-NNN | High | Medium | This cycle |

## Detailed Gap Assessments

### GAP-001: [Short description]
- **Requirement**: [Regulation, section, obligation]
- **Current state**: [What exists or does not exist]
- **Deficiency**: [What specifically is missing]
- **Severity**: [Critical | High | Medium | Low]
- **Regulatory exposure**: [Potential penalties or consequences]
- **Business impact**: [Operational/financial/reputational impact]
- **Remediation recommendation**: [Specific, actionable steps]
- **Effort estimate**: [Low | Medium | High]
- **Dependencies**: [What must happen first]
- **Target date**: [Recommended completion]

[Repeat for each gap]

## Compound Gaps
[Groups of gaps that together create larger exposure than individually]

## Summary Statistics
- Total gaps: [N]
- Critical: [N]
- High: [N]
- Medium: [N]
- Low: [N]
- Estimated total remediation effort: [Assessment]
```

## Rules

- The compliance officer decides risk acceptance and remediation priority. Present the analysis.
- Never downplay severity. If a gap is Critical, say so.
- Remediation recommendations must be specific and actionable.

## Delegation

Delegate the detailed assessment to the **gap-assessor** agent.
