---
name: check-refs
description: "Audit all cross-references and citations in a paper or across papers."
---

## What This Command Does (present to user)

Checks every citation in your paper for integrity: does every in-text citation have a reference entry? Is every reference entry actually cited? Are cross-paper citation suffixes consistent? Are scope boundaries respected?

## Your Role (communicate to user)

Review the report. Orphan citations need reference entries. Phantom references should be cited or removed. Scope violations need content moved to the right paper.

## Workspace Resolution

1. Parse `$ARGUMENTS` for target paper or workspace
2. If no argument, use the most recently modified workspace under `workspaces/`
3. Store results in `workspaces/<project>/04-validate/reviews/`

## Workflow

### 1. Parse target

Determine which paper(s) to audit.

### 2. Run audits

Delegate to **cross-reference-auditor**:

1. **Orphan citations** — `(Author, Year)` without reference entry
2. **Phantom references** — Reference entry never cited in text
3. **Suffix consistency** — Multi-paper citation suffixes (a, b, c) consistent across documents
4. **Shared fact consistency** — License terms, version numbers, key claims consistent across papers
5. **Scope violations** — Content that belongs in a different paper or section

### 3. Store results

Save in `workspaces/<project>/04-validate/reviews/refs-<date>.md`.

### 4. Present to user

Structured report with PASS/FAIL per item. Highlight items needing attention.

## Agent Team

- **cross-reference-auditor** — Primary: runs all checks
