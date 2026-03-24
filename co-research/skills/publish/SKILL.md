---
name: publish
description: "Prepare a publication for submission to any academic venue (arXiv, SSRN, AIES, AI & Society). Handles quality checks, format conversion, packaging, and submission guides."
---

## What This Command Does (present to user)

Prepare a publication for submission to an academic venue. This handles the full lifecycle: quality checks against venue requirements, citation audit, format conversion, packaging, and step-by-step submission instructions. Works for arXiv, SSRN, AIES, AI & Society, and other venues.

For arXiv-specific work, this command subsumes `/co-research:arxiv` with additional multi-venue capabilities.

## Your Role (communicate to user)

You'll need to confirm: which paper, which venue, and any last-minute content decisions. Everything else is automated.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a paper and/or venue, use that (e.g., `/co-research:publish arXiv`, `/co-research:publish SSRN`)
2. If only a paper is specified, check the workspace brief for the target venue
3. If nothing specified, show the paper status and ask
4. Submission workspace: `workspaces/<project>/05-submit/<venue>/`
5. For arXiv: use existing `workspaces/<project>/05-arxiv/` if it exists

## Workflow

### 1. Paper and Venue Identification

Read the workspace brief for context. Identify:

- Which paper
- Which venue (arXiv, SSRN, AIES, AI & Society)
- Current status and any blockers
- Venue deadline (if applicable)

Present status to user and confirm the target.

### 2. Version Check

Before any content changes:

- [ ] Current version number matches the Version History table's latest entry
- [ ] If this submission involves content changes, bump the version:
  1. Copy current file to `archive/versions/{Name}-v{X.Y}.md`
  2. Update version number and date in frontmatter
  3. Add a row to the Version History table
  4. Update `archive/versions/README.md`
- [ ] License line (CC BY 4.0) present in frontmatter

### 3. Source Quality Preflight

Run these checks on the source document:

**Content checks:**

- [ ] No TODO/TBD/placeholder markers
- [ ] No internal file path references (docs/, workspaces/, .claude/)
- [ ] All cross-references resolve (every "Section X" points to a real section)
- [ ] All citations have corresponding references
- [ ] Version number and date are current
- [ ] Version History table present at end of document
- [ ] Disclosure section present and accurate
- [ ] Honest limitations section present and substantive
- [ ] No unfalsifiable claims without citation

**Delegate to agents:**

- **cross-reference-auditor** — Citation accuracy, cross-reference integrity
- **claims-verifier** — Verify all factual claims before archival submission

**Venue-specific checks:**

- arXiv: Category fit, contribution statement clear
- SSRN: Abstract 150-400 words, keywords selected
- AIES: Max 10 pages (estimate), broader impact section, single-blind compliance
- AI & Society: Double-blind compliance, no author identification in body

### 4. Citation Audit

Count references and compare against venue minimum:

| Venue        | Minimum | Action if Below                     |
| ------------ | ------- | ----------------------------------- |
| arXiv        | 15      | Add foundational/competitor refs    |
| SSRN         | 10      | Usually sufficient                  |
| AIES         | 25      | Major related work expansion needed |
| AI & Society | 30      | Major related work expansion needed |

For each missing category, identify specific papers to add:

- Foundational works in the field
- Contemporary competitors (search arXiv recent years)
- Governance and regulatory frameworks (if applicable)
- Methodology (if applicable — HCI, design science, case study)

### 5. Format Conversion

Convert the Markdown source to the venue's required format:

**arXiv**: Markdown to LaTeX (article class)

- Generate `references.bib` from the References section
- Verify all `\cite{}` keys resolve

**SSRN**: Markdown to Formatted PDF

- Clean formatting with proper headings, tables, references
- Title page with abstract, keywords, JEL codes
- Can be generated from LaTeX or directly formatted

**AIES**: Markdown to LaTeX (AAAI 2-column)

- Use `aaai25.sty` author kit
- 10-page limit enforcement
- natbib bibliography style

**AI & Society**: Markdown to LaTeX (Springer)

- Springer svjour3 template
- Double-blind: remove author block from body

### 6. Package and Validate

Create the submission package:

```
workspaces/<project>/05-submit/<venue>/
  main.tex (or main.pdf for SSRN)
  references.bib
  figures/ (if any)
  README-submit.md (step-by-step human instructions)
```

**Validation:**

- [ ] Format compiles/renders without errors
- [ ] All references resolve
- [ ] Page count within venue limit (if applicable)
- [ ] Blind review compliance (if applicable)
- [ ] No archival-unsafe content
- [ ] File size under venue limit

### 7. Generate Submission Guide

Create `README-submit.md` with venue-specific step-by-step instructions:

- Account creation (if first time)
- Exact URL to submit
- What to upload and in what order
- Metadata to enter (title, abstract, keywords, category)
- License selection
- What to expect after submission (timeline, IDs)

### 8. Track Submission

Update the workspace brief or tracking document with:

- Submission date
- Venue
- Assigned ID (when available)
- Status (submitted, under review, accepted, revision requested)

## Agent Teams

- **cross-reference-auditor** — Cross-reference and citation accuracy
- **claims-verifier** — Verify all claims before archival submission
- **literature-researcher** — Identify missing references for citation density
- **field-expert** — Content accuracy for the research domain
