---
name: cite
description: "Format citations in APA, Chicago, or Harvard style"
---

## Purpose

Format citations and reference lists in the student's required style. Can format individual citations, convert between styles, check existing citations for errors, or generate a complete reference list.

## Input

`$ARGUMENTS` contains source details and/or desired citation style. Accepts flexible formats:
- Format a citation: "APA: Fama, Eugene. 1970. Efficient Capital Markets. Journal of Finance."
- Check citations: "check my references in workspaces/thesis/drafts/chapter2.md"
- Convert: "convert to Harvard: Sharpe, W.F. (1966). Mutual Fund Performance..."

If `$ARGUMENTS` is empty, ask: "What would you like to cite? Give me source details and your required style (APA, Chicago, Harvard), or point me to a file to check."

## Supported Styles

- **APA 7th** — most common in finance/business. In-text: (Author, Year)
- **Chicago Author-Date 17th** — common in economics/policy. In-text: (Author Year, page)
- **Harvard** — common in UK/Australian universities. In-text: (Author, Year)

## Capabilities

1. **Format individual citations** — given source details, produce properly formatted citation
2. **Generate reference lists** — from sources or a document with in-text citations, produce alphabetically sorted list
3. **Check existing citations** — scan for: in-text without reference entry (and vice versa), formatting inconsistencies, missing fields, incorrect ordering
4. **Convert between styles** — reformat from one style to another

## Critical Rules

1. **Precision matters.** Check every element: author name order, year placement, italicization, punctuation, page ranges.
2. **Consistency over perfection.** If the professor uses a custom variation, maintain it consistently throughout.
3. **Flag suspicious sources.** If a cited source does not appear to exist, flag it.
4. **Respect the required style.** Do not impose a different style. Ask if not specified.
