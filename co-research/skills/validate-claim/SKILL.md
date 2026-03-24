---
name: validate-claim
description: "Verify a specific claim or section against cited sources. Is this what the paper actually says?"
---

## What This Command Does (present to user)

Checks whether the claims in your paper are actually supported by the sources you cite. Every attribution gets verified — we check if the cited paper really says what you say it says.

## Your Role (communicate to user)

Review the verification report. For any claim marked OVERCLAIMED or worse, decide whether to fix the attribution, soften the claim, or find a better source.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a workspace, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/`
3. Store results in `workspaces/<project>/04-validate/reviews/`

## Workflow

### 1. Parse target

If `$ARGUMENTS` is a quoted claim — verify that specific claim.
If `$ARGUMENTS` is a section reference (e.g., "Part III") — verify all claims in that section.
If `$ARGUMENTS` is "full-paper" — verify every claim.

### 2. Extract claims

Read the target text and extract every factual or attributive claim:

- "Author (Year) argued/showed/demonstrated X"
- "Research shows that X"
- Quantitative claims (counts, percentages, dates)
- Self-citations referencing companion papers

### 3. Verify each claim

Delegate to **claims-verifier** for each claim. Produce a verdict:

- **VERIFIED** — Source confirms the claim
- **PARTIALLY_CORRECT** — Similar but oversimplified
- **OVERCLAIMED** — Source is more nuanced
- **MISATTRIBUTED** — Source doesn't make this claim
- **UNVERIFIABLE** — Can't access source
- **FABRICATED** — No evidence paper exists (FATAL)

### 4. Store results

Save verification report in `workspaces/<project>/04-validate/reviews/claims-<date>.md`.

### 5. Present to user

Show each claim with its verdict. For non-VERIFIED claims, explain what the source actually says and suggest a correction.

## Approval Gate

FABRICATED claims are FATAL — block all further writing on that section until resolved. OVERCLAIMED and MISATTRIBUTED claims should be addressed before submission.

## Agent Team

- **claims-verifier** — Primary: verifies each claim against sources
- **cross-reference-auditor** — Support: checks citation format and reference list
