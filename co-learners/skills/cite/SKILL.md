---
name: cite
description: "Citation formatting — APA, Chicago, Harvard, MLA. Verify and convert between styles."
---

## Purpose

Format citations correctly, verify existing citations, or convert between styles. Supports APA 7th, Chicago (Author-Date and Notes-Bibliography), Harvard, MLA, and other styles as needed.

## Input

`$ARGUMENTS` contains the citation style, source to cite, or action (e.g., "APA", "verify my citations", "convert to Chicago").

If `$ARGUMENTS` is empty, ask: "What would you like help with? I can format a new citation, verify existing citations in your draft, or convert between styles."

## Protocol

**If formatting a new citation:**

1. Identify the source type (journal article, book, chapter, website, etc.)
2. Format in the requested style (APA 7th, Chicago, Harvard, MLA)
3. Generate both in-text citation and reference list entry

**If verifying citations:**

1. Read the draft from `03-drafts/`
2. Check every citation for: correct format, consistent style, all required fields
3. Flag any citations that cannot be verified

**If converting between styles:**

1. Read existing citations
2. Convert to target style
3. Check consistency throughout

## Key Principle

Every citation must be verifiable. If a source cannot be confirmed to exist, flag it immediately. A single fabricated citation can mean automatic failure.
