# /co-research:preflight — Publication Pre-Flight Check

Run comprehensive pre-submission validation on a publication document.

## Usage

```
/co-research:preflight [paper-path]
```

If `$ARGUMENTS` specifies a paper path, use that as the target document.
If no arguments given, scan papers in the active workspace's drafts or submission directory.

## What This Does

1. **Reference Verification** — Checks every citation for existence and correctness
2. **Factual Claims** — Verifies numerical claims against cited sources
3. **Overclaim Detection** — Flags unsubstantiated novelty/superiority claims
4. **Design vs. Reality** — Catches aspirational claims presented as operational
5. **Venue Compliance** — Checks format, length, and required sections
6. **Cross-Paper Consistency** — Ensures shared facts match across papers
7. **Archival Safety** — Scans for internal paths, TODOs, sensitive content

## Instructions

When this command is invoked:

1. Read the publication-claims rule at `.claude/rules/publication-claims.md`
2. Identify the target paper(s)
3. Perform deep validation across all check categories
4. Present the structured report to the user
5. If BLOCK issues are found, do NOT proceed to submission without fixes

## Priority Order

Fix issues in this order:

1. **Fabricated references** — Career-ending. Verify every citation.
2. **Factual errors** — Wrong numbers, dates, section references
3. **Overclaims** — "First", "only", "novel" without qualification
4. **Missing sections** — Methodology, limitations, broader impact
5. **Venue compliance** — Page limits, format, keywords
6. **Style** — Voice consistency, citation formatting

## Critical Reminders

- A single fabricated reference = automatic desk rejection
- All self-citations need stable URLs
- Distinguish between specified, implemented, deployed, and validated claims
