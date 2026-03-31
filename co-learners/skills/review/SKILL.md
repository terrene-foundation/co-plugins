---
name: review
description: "Peer review — evaluate argument strength, evidence quality, citations"
---

## Purpose

Constructive peer review of the student's work. Evaluates argument strength, evidence quality, citation accuracy, and writing clarity. Provides actionable feedback.

## Input

`$ARGUMENTS` contains the assignment or topic name.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project, use `workspaces/$ARGUMENTS/`
2. Otherwise, use most recently modified under `workspaces/` (excluding `_template/`)

## Protocol

1. **Read the work** from `03-drafts/`
2. **Evaluate argument strength** — is the thesis clear? Does evidence support claims?
3. **Check evidence quality** — are sources credible? Is analysis sound?
4. **Verify citations** — delegate to citation-specialist agent
5. **Assess structure** — does the organization support the argument?
6. **Provide constructive feedback** — what to improve and how

## Output

Save to `04-review/review-[topic-slug].md`. Organize by: strengths, areas for improvement, specific suggestions.

## Journal Entry

Record significant findings in `journal/`. Type: RISK or GAP.
