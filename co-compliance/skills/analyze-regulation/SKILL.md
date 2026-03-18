---
name: analyze-regulation
description: Analyze a specific regulation or standard and extract actionable requirements into a structured register.
argument-hint: "[regulation name, e.g., 'GDPR', 'HIPAA', 'PCI DSS v4.0']"
---

# /analyze-regulation $ARGUMENTS

Analyze **$ARGUMENTS** and extract a structured requirements register.

## Protocol

1. **Find the active workspace**
2. **Identify the regulation**: full name, jurisdiction, effective date, current version
3. **Determine applicability**: who it applies to, what triggers it, exemptions
4. **Extract requirements**: read the regulatory text and extract every specific obligation as a testable requirement
5. **Classify requirements**: mandatory vs conditional vs recommended
6. **Identify cross-references**: where this regulation references other regulations or standards
7. **Flag ambiguities**: requirements that could be interpreted multiple ways
8. **Save the requirements register** to `03-work/`

## Output

Save to `03-work/requirements-register-[regulation-slug].md`:

```markdown
# Requirements Register: $ARGUMENTS
Jurisdiction: [Country/Region]
Effective Date: [Date]
Last Amended: [Date]
Status: [Active | Pending | Superseded]
Source: [Official publication reference]

## Applicability
- **Applies to**: [Entity types, sectors, activities]
- **Triggers**: [What brings an organization into scope]
- **Exemptions**: [Conditions for exemption]
- **Extraterritorial scope**: [If applicable]

## Requirements

### REQ-001: [Short description]
- **Source**: $ARGUMENTS Art./Sec. [Number]
- **Exact text**: "[Quoted regulatory text]"
- **Obligation type**: [Mandatory | Conditional | Recommended]
- **Subject**: [Who must comply]
- **Action**: [What must be done]
- **Conditions**: [When/if applicable]
- **Deadline**: [Timeframe if specified]
- **Penalty for non-compliance**: [If specified]

[Repeat for each requirement]

## Cross-References
[Where this regulation references other regulations or standards]

## Ambiguities
[Requirements with unclear or multiple interpretations - recommend legal counsel review]

## Summary Statistics
- Total requirements extracted: [N]
- Mandatory: [N]
- Conditional: [N]
- Recommended: [N]
```

## Rules

- Quote exact regulatory text. Do not paraphrase obligations.
- Every requirement gets a unique ID (REQ-NNN) for traceability throughout the compliance process.
- Flag when your knowledge of this regulation may be outdated. Regulations change; recommend verification against the official source.
- The compliance officer determines applicability to their specific organization. Present the criteria; let them decide.

## Delegation

Delegate the detailed analysis to the **regulation-analyst** agent.
