---
name: cite
description: "Format citations in APA, Chicago, or Harvard style"
---

## Purpose

Format citations and reference lists in the student's required citation style. Can format individual citations from source details, convert between styles, check existing citations for errors, or generate a complete reference list.

## Input

`$ARGUMENTS` contains source details and/or the desired citation style. Flexible formats accepted:

**Format a single citation:**
- "APA: Fama, Eugene. 1970. Efficient Capital Markets. Journal of Finance."
- "Chicago: Markowitz 1952 Portfolio Selection"

**Check existing citations:**
- "check my references in workspaces/thesis/drafts/chapter2.md"
- "check APA formatting" (with text pasted)

**Convert between styles:**
- "convert to Harvard: Sharpe, W.F. (1966). Mutual Fund Performance. Journal of Business, 39(1), 119-138."

If `$ARGUMENTS` is empty, ask the student: "What would you like to cite? You can give me source details (author, title, year, publication) and your required style (APA, Chicago, Harvard), or point me to a file to check for citation errors."

## Supported Citation Styles

### APA 7th Edition
The most common style in finance and business courses.

**Journal article:**
```
Author, A. A., & Author, B. B. (Year). Title of article. Title of Periodical, Volume(Issue), Page–Page. https://doi.org/xxxxx
```

**Book:**
```
Author, A. A. (Year). Title of work: Capital letter also for subtitle. Publisher.
```

**In-text:** (Author, Year) or Author (Year)

### Chicago (Author-Date, 17th Edition)
Common in economics and policy writing.

**Journal article:**
```
Author, First Name. Year. "Title of Article." Journal Title Volume, no. Issue (Month): Pages. https://doi.org/xxxxx.
```

**Book:**
```
Author, First Name. Year. Title of Book. Place: Publisher.
```

**In-text:** (Author Year, page) or Author (Year, page)

### Harvard
Common in UK and Australian universities.

**Journal article:**
```
Author, A.A. and Author, B.B. (Year) 'Title of article', Title of Journal, Volume(Issue), pp. Page–Page.
```

**Book:**
```
Author, A.A. (Year) Title of Book. Edition. Place: Publisher.
```

**In-text:** (Author, Year) or Author (Year)

## Capabilities

### 1. Format Individual Citations
Given source details (author, year, title, journal, volume, pages), produce the properly formatted citation in the requested style.

### 2. Generate Reference Lists
Given a set of sources or a document containing in-text citations, produce a complete, alphabetically sorted reference list.

### 3. Check Existing Citations
Scan a document for citation errors:
- In-text citations without corresponding reference list entries
- Reference list entries not cited in the text
- Formatting inconsistencies (e.g., mixing APA and Chicago styles)
- Missing required fields (year, volume, pages)
- Incorrect ordering (alphabetical by author surname)

### 4. Convert Between Styles
Given a citation in one style, convert it to another.

### 5. Common Finance Sources Quick Reference

For frequently cited finance sources, provide pre-formatted citations:

| Source | Key Reference |
|---|---|
| Markowitz portfolio theory | Markowitz, H. (1952). Portfolio Selection. Journal of Finance, 7(1), 77-91. |
| CAPM | Sharpe, W.F. (1964). Capital Asset Prices. Journal of Finance, 19(3), 425-442. |
| Efficient market hypothesis | Fama, E.F. (1970). Efficient Capital Markets. Journal of Finance, 25(2), 383-417. |
| Fama-French three-factor | Fama, E.F., & French, K.R. (1993). Common Risk Factors. Journal of Financial Economics, 33(1), 3-56. |
| Black-Scholes | Black, F., & Scholes, M. (1973). The Pricing of Options. Journal of Political Economy, 81(3), 637-654. |
| Modigliani-Miller | Modigliani, F., & Miller, M.H. (1958). The Cost of Capital. American Economic Review, 48(3), 261-297. |

## Critical Rules

1. **Precision matters.** A misformatted citation can cost marks. Double-check every element: author name order, year placement, italicization, punctuation, page ranges.

2. **Consistency is more important than perfection.** If the student is using a slightly non-standard variation of a style (e.g., their professor's custom requirements), maintain that variation consistently throughout.

3. **Flag suspicious sources.** If a cited source does not appear to exist (wrong year, wrong journal, misattributed author), flag it. Students sometimes cite sources they have not actually read.

4. **Respect the student's required style.** Do not impose a different style, even if you prefer it. Ask which style is required if not specified.

## Agent Team

- **citation-specialist** — Citation formatting, bibliography generation, error checking
- **academic-writer** — Integration of citations into prose (when reviewing in-text citation usage)

## Skill References

- `15-citation-guide/` — Detailed citation formatting rules and examples
