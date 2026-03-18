---
name: check-refs
description: Cross-reference and citation audit for a paper
arguments:
  - name: paper
    description: The paper file or directory to audit
    required: true
---

# /check-refs $paper

You are conducting a cross-reference audit of **$paper**. Every citation must resolve, every reference must be cited, and all formatting must be consistent.

## Protocol

1. **Find the active workspace** by checking `workspaces/` for the most recently modified project directory
2. **Load the paper**: Read the target file(s)
3. **Run the audit**: Check all citations and references

## Delegation

Spawn the **cross-reference-auditor** agent for the audit.

## Audit Phases

### Phase 1: Citation Extraction
- Extract every in-text citation with author, year, suffix, page number, and location
- Build a complete citation inventory

### Phase 2: Reference List Extraction
- Parse the reference section
- Build a complete reference inventory

### Phase 3: Cross-Match
- Orphan citations (cited in text, not in references)
- Uncited references (in references, not cited in text)
- Suffix inconsistencies
- Year mismatches
- Author name spelling inconsistencies

### Phase 4: Format Check
- Citation format consistency (Author, Year) vs (Author Year) vs numbered
- Reference format consistency (matching target venue style)
- Alphabetical ordering of reference list

### Phase 5: Scope Check (if multiple papers)
- Verify each paper stays within its declared scope
- Check companion paper cross-references are accurate

## Output

### Audit Report

Store in `04-validate/reviews/` named `ref-audit-[paper-slug].md`:

```markdown
# Cross-Reference Audit: $paper
Date: [today]

## Summary
- In-text citations: [N]
- Reference entries: [N]
- Orphan citations: [N]
- Uncited references: [N]
- Inconsistencies: [N]

## Issues Found
[Detailed list of each issue with location and suggested fix]
```

## Journal Entry

Produce a CONNECTION journal entry:

```yaml
---
type: CONNECTION
date: [today]
paper: [paper name from brief]
topic: cross-reference audit
tags: [relevant tags]
---
```
