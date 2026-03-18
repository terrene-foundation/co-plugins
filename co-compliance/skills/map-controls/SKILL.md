---
name: map-controls
description: Map regulatory requirements to organizational controls. Assess coverage and identify partial or missing mappings.
argument-hint: "[requirement area or regulation to map, e.g., 'GDPR data subject rights', 'SOC 2 availability']"
---

# /map-controls $ARGUMENTS

Map the requirements for **$ARGUMENTS** to organizational controls.

## Protocol

1. **Find the active workspace**
2. **Read the relevant requirements register** from `03-work/`
3. **Identify the organization's control framework** (NIST, ISO 27001, SOC 2, or internal). Ask if not yet established.
4. **Map each requirement to existing controls** with coverage assessment
5. **Identify shared controls** that satisfy multiple requirements
6. **Document mapping rationale** for each connection
7. **Save the control mapping** to `03-work/`

## Output

Save to `03-work/control-mapping-[area-slug].md`:

```markdown
# Control Mapping: $ARGUMENTS
Date: [today]
Framework: [Organization's control framework]
Requirements source: [Reference to requirements register]

## Mapping Summary
| Requirement | Control | Coverage | Notes |
|------------|---------|----------|-------|
| REQ-001 | [Control ID] | Full | [Brief rationale] |
| REQ-002 | [Control ID] | Partial | [What is covered/uncovered] |
| REQ-003 | None | None | [Gap - no existing control] |

## Detailed Mappings

### REQ-001: [Requirement description]
- **Mapped to**: [Control ID] - [Control name]
- **Coverage**: [Full | Partial | None | Compensating]
- **Rationale**: [How the control satisfies the requirement]
- **Evidence**: [What demonstrates the control operates]

[Repeat for each requirement]

## Shared Controls
[Controls that map to multiple requirements - these are efficiency points for audit]

## Unmapped Requirements
[Requirements with no corresponding control - these become gaps]

## Coverage Statistics
- Total requirements: [N]
- Fully mapped: [N] ([%])
- Partially mapped: [N] ([%])
- Unmapped: [N] ([%])
```

## Rules

- Every mapping must explain HOW the control satisfies the requirement
- Ask the compliance officer to confirm the organization's control framework before mapping
- Flag when a requirement cannot be mapped because the organization's control inventory is incomplete

## Delegation

Delegate the detailed mapping to the **control-mapper** agent.
