---
name: arxiv
description: "Prepare and validate a document for arXiv submission. Handles LaTeX conversion, metadata, preflight checks, and submission packaging."
---

## What This Command Does (present to user)

Prepare a publication for arXiv submission. This handles everything from converting your Markdown whitepaper to LaTeX, setting up metadata, running preflight checks, and packaging the submission. The goal is a clean first-time submission with no rejections.

## Your Role (communicate to user)

You'll need to confirm: the target arXiv category, author metadata, and any last-minute content decisions. Everything else is automated.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a file or project, use that
2. Otherwise, look for the most recent publication in the workspace's drafts or submissions directory
3. Submission workspace: `workspaces/<project>/05-arxiv/`

## Workflow

### 1. Preflight Validation

Before any conversion, run these checks on the source document:

**Content checks:**
- [ ] No TODO/TBD/placeholder markers
- [ ] No internal file path references (docs/, workspaces/, .claude/)
- [ ] No TeX comments with sensitive content (these are archival)
- [ ] All cross-references resolve (every "Section X" points to a real section)
- [ ] All citations have corresponding references
- [ ] Version number and date are current
- [ ] Disclosure section is present and accurate
- [ ] Honest limitations section is present and substantive
- [ ] No unfalsifiable claims
- [ ] License statement matches arXiv license selection (CC BY 4.0)

**Security checks:**
- [ ] No sensitive partnership details
- [ ] No financial projections
- [ ] No internal engagement timelines
- [ ] No personal contact information beyond published affiliations

### 2. LaTeX Conversion

Convert the Markdown source to LaTeX:

- Use a standard document class (`article` or `IEEEtran`)
- Preserve all section structure
- Convert Markdown tables to LaTeX `tabular` environments
- Convert code blocks to `lstlisting` or `minted` environments
- Convert Markdown links to `\url{}` or `\href{}`
- Add proper `\cite{}` references from the references section
- Generate `references.bib` from the References section

**LaTeX structure:**
```latex
\documentclass[11pt]{article}
\usepackage[utf8]{inputenc}
\usepackage{hyperref}
\usepackage{booktabs}
\usepackage{listings}
\usepackage{amsmath}

\title{...}
\author{...}
\date{...}

\begin{document}
\maketitle
\begin{abstract}
...
\end{abstract}
% Content sections
\bibliographystyle{plain}
\bibliography{references}
\end{document}
```

### 3. arXiv Metadata Preparation

Prepare the submission metadata:

- **Title**: Extract from document
- **Authors**: Extract from document, format as "FirstName LastName (Affiliation)"
- **Abstract**: Extract, ensure 150-300 words, no LaTeX commands
- **Primary category**: Select appropriate cs.* category
- **Cross-list**: Select if applicable
- **Comments**: "Version X.X. Y pages. Published under CC BY 4.0."
- **License**: arXiv Non-Exclusive License to Distribute (compatible with CC BY 4.0)
- **DOI**: Leave blank (preprint)

### 4. Package and Validate

Create the submission package:

```
workspaces/<project>/05-arxiv/
  main.tex
  references.bib
  figures/          (if any)
  README-arxiv.md   (submission instructions for the human)
```

**Final validation:**
- [ ] LaTeX compiles without errors (`pdflatex main.tex && bibtex main && pdflatex main.tex && pdflatex main.tex`)
- [ ] No overfull hboxes > 10pt
- [ ] All references resolve
- [ ] PDF renders correctly
- [ ] File size under 10MB
- [ ] No auxiliary files (.aux, .log, .bbl) included — arXiv generates these

### 5. Generate Submission Guide

Create `README-arxiv.md` with step-by-step instructions for the human to complete the submission:

1. Go to https://co-research:arxiv.org/submit
2. Select category
3. Upload: main.tex, references.bib, [figures if any]
4. Enter metadata (provided)
5. Preview and submit
6. Record the arXiv ID in the workspace

## Agent Teams

- **cross-reference-auditor** — Cross-reference and citation accuracy
- **claims-verifier** — Verify claims before archival submission
