---
name: analyze
description: Research the regulatory landscape. Identify applicable regulations, gather requirements, map the compliance environment.
argument-hint: "[regulation, framework, or compliance topic]"
---

# /analyze $ARGUMENTS

Research and analyze the regulatory compliance landscape for **$ARGUMENTS**.

## Protocol

1. **Find the active workspace** by checking `workspaces/` for the most recently modified project
2. **Read the project brief** if one exists in the workspace
3. **Research the regulatory landscape**: identify applicable regulations, frameworks, and standards
4. **Determine applicability**: which regulations apply to the organization based on jurisdiction, industry, data types, and activities
5. **Map regulatory overlaps**: where multiple regulations address the same area
6. **Document findings** in `01-research/`

## Output

Save a structured analysis to `01-research/analysis-[topic-slug].md`:

```markdown
# Regulatory Analysis: $ARGUMENTS
Date: [today]
Jurisdiction: [applicable jurisdictions]

## Applicable Regulations
[List with jurisdiction, effective date, and applicability rationale]

## Key Requirements Summary
[High-level requirement areas by regulation]

## Regulatory Overlaps
[Where requirements from different regulations address the same area]

## Pending Changes
[Upcoming amendments, new regulations, or regulatory guidance]

## Recommendations
[What the compliance officer should consider for the assessment plan]
```

## Next Step

After analysis, recommend `/plan` to create a structured compliance assessment plan based on findings.
