---
name: validate-claim
description: Verify claims against cited sources with structured verification reports
arguments:
  - name: target
    description: The section, paragraph, or specific claim to verify
    required: true
---

# /validate-claim $target

You are verifying the claims in **$target** against their cited sources. Every factual and attributive claim must be checked.

## Protocol

1. **Find the active workspace** by checking `workspaces/` for the most recently modified project directory
2. **Load the target content**: Read the section, paragraph, or specific claim to be verified
3. **Extract all claims**: Identify every claim that cites a source or states a verifiable fact

## Delegation

Spawn the **claims-verifier** agent to conduct the verification. The agent produces structured reports with VERIFIED / OVERCLAIMED / FABRICATED verdicts for each claim.

## Verification Scope

For each claim identified:

1. **Attributive claims**: "Author (Year) argued X" -- does the author actually argue X?
2. **Factual claims**: "X is the case (Author, Year)" -- does the source support this?
3. **Numerical claims**: "84 guidelines were surveyed" -- does the source contain this number?
4. **Scope claims**: "No prior work addresses X" -- is this actually true?

## Output

### Verification Report

Store the report in `04-validate/reviews/` named `claim-verification-[target-slug].md`:

```markdown
# Claim Verification: $target
Date: [today]
Verifier: claims-verifier agent

## Summary
- Claims checked: [N]
- VERIFIED: [N]
- OVERCLAIMED: [N]
- FABRICATED: [N]
- Unable to verify: [N]

## Detailed Results

### Claim 1: "[Quoted claim]"
- Source: [Full citation]
- Verdict: VERIFIED / OVERCLAIMED / FABRICATED
- Evidence: [Quote from source or explanation]
- Action: [None / Revise to: "..." / Remove and replace]
```

## Journal Entry

Produce a CLAIM journal entry for any significant finding:

```yaml
---
type: CLAIM
date: [today]
paper: [paper name from brief]
section: [section name]
topic: claim verification
tags: [relevant tags]
---
```
