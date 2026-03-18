---
name: preflight
description: Pre-submission deep validation - references, claims, overclaims, formatting
arguments:
  - name: paper
    description: The paper file to validate before submission
    required: true
---

# /preflight $paper

You are conducting pre-submission validation of **$paper**. This is the final check before the paper goes to a venue. Every issue found here prevents a desk rejection or reviewer complaint.

## Protocol

1. **Find the active workspace** by checking `workspaces/` for the most recently modified project directory
2. **Load the paper** and the target venue from the brief
3. **Run all validation checks**

## Validation Checklist

### 1. Reference Integrity
- [ ] Every in-text citation has a matching reference entry
- [ ] Every reference entry is cited in text
- [ ] No orphan citations or uncited references
- [ ] All arXiv IDs resolve (if web access available)
- [ ] All DOIs resolve (if web access available)
- [ ] Citation format matches venue requirements

### 2. Claim Verification
- [ ] No `[UNVERIFIED]`, `[TODO]`, or `[TBD]` markers remain
- [ ] No overclaims: "first", "only", "novel" are qualified with "to our knowledge"
- [ ] Claims are proportional to evidence
- [ ] Design vs. reality distinctions are maintained

### 3. Writing Quality
- [ ] No em dashes (U+2014)
- [ ] No AI-signature words (delve, crucial, comprehensive, etc.)
- [ ] No mechanical paragraph-opening transitions
- [ ] Sentence length varies (burstiness)
- [ ] No internal file paths or workspace references
- [ ] No draft markers or collaborator comments

### 4. Venue Compliance
- [ ] Page limit respected (if applicable)
- [ ] Citation density meets minimum for venue
- [ ] Blind review compliance (if applicable)
- [ ] Required sections present (limitations, broader impact, etc.)
- [ ] Abstract within word limit
- [ ] Author block formatted per venue requirements

### 5. Structural Completeness
- [ ] Explicit contribution statement in introduction
- [ ] Limitations section present and honest
- [ ] AI use disclosure present (per venue requirements)
- [ ] Version and date present

### 6. Terminology Consistency
- [ ] Key terms used consistently throughout
- [ ] Defined terms match their definitions at each usage
- [ ] Abbreviations defined at first use

## Output

### Preflight Report

Store in `04-validate/reviews/` named `preflight-[paper-slug].md`:

```markdown
# Preflight Report: $paper
Date: [today]
Target venue: [venue]

## Status: PASS / FAIL / PASS WITH WARNINGS

## Critical Issues (must fix before submission)
[List]

## Warnings (should fix, not blocking)
[List]

## Passed Checks
[Summary of what passed]
```

## Journal Entry

Produce a GAP journal entry for any issues found:

```yaml
---
type: GAP
date: [today]
paper: [paper name from brief]
topic: preflight validation
tags: [relevant tags]
---
```
