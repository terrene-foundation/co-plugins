---
name: publish
description: Prepare for venue-specific submission (arXiv, SSRN, AIES, AI & Society, etc.)
arguments:
  - name: venue
    description: Target venue (arXiv, SSRN, AIES, AI-Society, or other)
    required: true
---

# /publish $venue

You are preparing the paper for submission to **$venue**. This command handles venue-specific formatting, compliance checks, and packaging.

## Protocol

1. **Find the active workspace** by checking `workspaces/` for the most recently modified project directory
2. **Load the paper** and verify preflight has been run (check for preflight report in `04-validate/reviews/`)
3. **Apply venue-specific requirements**

## Pre-Submission Gate

Before proceeding, verify:
- [ ] `/preflight` has been run and all critical issues resolved
- [ ] `/check-refs` has been run and all issues resolved
- [ ] Author has approved the final draft

If preflight has not been run, run it first.

## Venue-Specific Requirements

### arXiv

- **Format**: LaTeX source required (PDF-only may be declined)
- **Abstract**: 150-300 words, plain text (no LaTeX formatting)
- **Category**: Select primary and cross-list categories
- **License**: Select appropriate arXiv license
- **Files**: Single directory with main.tex, references.bib, figures/
- **Size**: Total package under 10MB
- **Metadata**: Title must match document exactly
- **Note**: Position papers in CS may require prior peer review (October 2025 policy)

### SSRN

- **Format**: PDF (clean, formatted)
- **Abstract**: Up to 400 words
- **Keywords**: 3-5 from SSRN taxonomy
- **JEL codes**: If applicable
- **No submission fee**

### AIES

- **Format**: AAAI 2-column format (aaai author kit)
- **Page limit**: 10 pages excluding references
- **Review**: Single-blind
- **Required sections**: Broader impact
- **Note**: Check current year's deadlines and author kit

### AI & Society

- **Format**: Springer LaTeX template or Word
- **Review**: Double-blind (no author identification in body)
- **No strict page limit**
- **Section**: Research Article or Open Forum

### Other Venues

For unlisted venues, the command will:
1. Ask for venue formatting requirements
2. Check citation density against venue norms
3. Verify all required sections are present
4. Package the submission

## Output

Create a submission directory in the workspace with venue-specific files and a submission checklist.

## Journal Entry

Produce a GAP journal entry for any remaining issues:

```yaml
---
type: GAP
date: [today]
paper: [paper name from brief]
topic: submission preparation for $venue
tags: [submission, $venue]
---
```
