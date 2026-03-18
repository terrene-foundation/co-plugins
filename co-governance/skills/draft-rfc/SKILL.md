---
name: draft-rfc
description: Draft a Request for Comments (RFC) for a proposed governance change.
argument-hint: "[proposed change description]"
---

# /draft-rfc $ARGUMENTS

Draft an RFC for the proposed governance change: **$ARGUMENTS**

## Protocol

1. **Run a constitutional compliance pre-check** on the proposed change
2. **If non-compliant with entrenched provisions**: REFUSE to draft. Explain the conflict.
3. **If compliant or modifiable**: Proceed with drafting
4. **Identify the constitutional basis** for the proposed change
5. **Assess stakeholder impact** across all affected parties
6. **Draft the RFC** in the Foundation's standard format
7. **Include dissenting perspectives** even if the drafter disagrees with them
8. **Delegate to rfc-drafter agent** for the detailed draft

## Output

Save the RFC draft to `03-work/rfc-[slug].md` in the active workspace.

The RFC follows the Foundation's standard format:
- Summary, Motivation, Proposal
- Constitutional Impact (which clauses, whether entrenched)
- Stakeholder Impact
- Risks and Mitigations
- Dissenting Perspectives
- Implementation plan
- Decision Record (blank, to be filled after deliberation)

## Rules

- Never draft an RFC that contradicts an entrenched provision. Refuse and explain.
- Always run the constitutional compliance pre-check before drafting
- Always include dissenting perspectives, even for seemingly uncontroversial changes
- The RFC is a draft for officer review. It does not constitute a governance decision.

## Next Step

Present the draft RFC to the governance officer for review. Recommend `/review` to run a compliance audit on the draft before it enters the comment period.
