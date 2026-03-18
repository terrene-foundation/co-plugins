---
name: prep-audit
description: Prepare audit documentation packages with organized evidence, control narratives, and request list responses.
argument-hint: "[audit scope, e.g., 'SOC 2 Type II audit', 'GDPR supervisory authority review']"
---

# /prep-audit $ARGUMENTS

Prepare audit documentation for **$ARGUMENTS**.

## Protocol

1. **Find the active workspace**
2. **Read all relevant work products** from `03-work/` (control mappings, gap analyses, reports)
3. **Determine audit scope and requirements** from the arguments
4. **Organize evidence** by control objective
5. **Draft control narratives** describing how controls operate
6. **Prepare request list responses** if auditor requests exist
7. **Identify evidence gaps** before auditors discover them
8. **Save the audit package** to `03-work/` (moves to 05-output when finalized)

## Output

Save to `03-work/audit-package-[scope-slug]/`:

```
audit-package-[scope-slug]/
  README.md                    # Package overview and index
  control-narratives/          # One file per control
    [control-id]-narrative.md
  evidence-index.md            # Master evidence list with locations
  request-responses/           # Responses to auditor requests
    [request-id]-response.md
  gaps-and-remediation.md      # Known gaps with remediation status
```

### Package README format:
```markdown
# Audit Documentation Package: $ARGUMENTS
Date prepared: [Date]
Audit period: [Date range]
Prepared by: [Names/roles]
Status: DRAFT - Pending compliance officer review

## Package Contents
[Index of all documents in this package]

## Scope
[What controls and requirements this package covers]

## Known Gaps
[Summary of gaps with remediation status - do not hide these]

## Evidence Not Available
[What evidence could not be located and why]
```

## Rules

- Never include evidence you have not verified exists
- Never fabricate evidence or create documentation for controls that do not exist
- Flag all evidence gaps proactively. Auditors finding gaps is worse than disclosing them.
- Organize by control objective, not by document type
- Include context with every piece of evidence

## Delegation

Delegate the detailed preparation to the **audit-preparer** agent.
