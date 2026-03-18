---
name: transparency-report
description: Generate a governance transparency report for a specified period or topic.
argument-hint: "[period or topic, e.g. 'Q1 2026' or 'membership decisions']"
---

# /transparency-report $ARGUMENTS

Generate a governance transparency report for: **$ARGUMENTS**

## Protocol

1. **Determine the scope** from the user's description (time period, topic area, or both)
2. **Gather governance records** from workspace artifacts, journal entries, and completed todos
3. **Compile all governance decisions** made during the period with their rationale
4. **List all RFCs** filed, decided, or pending during the period
5. **Document membership changes** if any
6. **Assess compliance status** based on available audit records
7. **Identify transparency gaps** where documentation is missing or incomplete
8. **Delegate to transparency-reporter agent** for report generation

## Output

Save the report to `03-work/transparency-report-[slug].md` in the active workspace.

The report follows the Foundation's standard transparency report format:
- Summary of governance activity
- Governance decisions table (with constitutional basis and rationale)
- RFC status table
- Membership changes table
- Compliance status summary
- Open items
- Known gaps

## Rules

- Reports must be factual. No spin, no marketing language.
- Every listed decision must have a documented rationale. Flag decisions that lack one.
- Reports must be suitable for public disclosure
- Identify and call out any transparency gaps explicitly

## Next Step

Present the report to the governance officer for review. Recommend `/review` for a compliance audit of the report before publication.
