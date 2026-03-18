---
name: draft-report
description: Draft a compliance report with citations, evidence references, and actionable findings.
argument-hint: "[report type and scope, e.g., 'executive summary for GDPR assessment', 'detailed SOC 2 readiness report']"
---

# /draft-report $ARGUMENTS

Draft a compliance report for **$ARGUMENTS**.

## Protocol

1. **Find the active workspace**
2. **Read all relevant work products** from `03-work/` (requirements registers, control mappings, gap analyses)
3. **Determine report type and audience** from the arguments
4. **Draft the report** with appropriate structure, detail level, and tone for the audience
5. **Include citations and evidence references** for every compliance claim
6. **Save the draft** to `03-work/` (drafts go to 03-work until finalized)

## Report Types

| Type | Audience | Focus |
|------|----------|-------|
| Executive Summary | Board, C-suite | Overall posture, critical gaps, resource needs |
| Detailed Assessment | Compliance team, management | Requirement-by-requirement analysis |
| Regulatory Filing | Regulatory body | Specific obligations, evidence of compliance |
| Audit Readiness | Auditors | Control descriptions, evidence availability |

## Output

Save to `03-work/report-draft-[type-slug]-[date].md`:

```markdown
# [Report Type]: [Subject]
Date: [Date]
Status: DRAFT - Pending compliance officer review
Scope: [What was assessed]
Period: [Assessment period]

## Executive Summary
[High-level findings appropriate for the audience]

## Scope and Methodology
[What was assessed, how, what was excluded]

## Findings
[Structured findings with severity, citations, evidence, recommendations]

## Remediation Status
[Current state of gap closure efforts]

## Limitations
[What this report does not cover]
```

## Rules

- Mark all drafts clearly as DRAFT until the compliance officer approves
- Every compliance claim must reference evidence
- Every regulatory citation must include regulation, section, jurisdiction, effective date
- Never use language that could be construed as legal advice
- Distinguish between: compliant (evidence exists), non-compliant (gap identified), not assessed (out of scope)

## Delegation

Delegate the detailed drafting to the **report-drafter** agent.
