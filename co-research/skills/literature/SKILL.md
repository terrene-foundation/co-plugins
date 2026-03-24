---
name: literature
description: "Systematic literature search on a topic. Find, assess, and organize relevant papers."
---

## What This Command Does (present to user)

Systematic search for academic papers on a topic. You'll get an organized list of relevant papers, grouped by approach, with quality assessment and gap identification.

## Your Role (communicate to user)

Review the papers found and decide which ones to include in your working bibliography. You know your argument better than anyone — you decide what's relevant.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a workspace, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/`
3. Store results in `workspaces/<project>/01-analysis/literature/`

## Workflow

### 1. Parse search terms

Extract search terms from `$ARGUMENTS`.

### 2. Systematic search

Delegate to **literature-researcher**:

- Search across arXiv, Google Scholar, Semantic Scholar, DBLP
- Use specific queries, not broad terms
- Find 10-20 papers per search, prioritizing:
  - Foundational works (high citation count)
  - Recent high-impact papers (last 3 years)
  - Direct competitors or alternative approaches
  - Papers reviewers at target venue would expect

### 3. Assess and organize

For each paper found:

- Title, authors, year, venue
- Relevance score (HIGH/MEDIUM/LOW)
- One-sentence summary
- Verification status (VERIFIED/UNVERIFIED)

Group by approach:

- Foundational / Canonical
- Contemporary / Recent
- Competing / Alternative
- Governance / Policy
- Methodology / Design Science

### 4. Identify gaps

Flag topics where no papers were found but reviewers would expect coverage. "You have nothing on X — a reviewer will notice."

### 5. Store results

Save in `workspaces/<project>/01-analysis/literature/<search-slug>.md`.

### 6. Journal findings

For each paper assessed, create a LITERATURE journal entry in `workspaces/<project>/journal/NNNN-LITERATURE-<author-topic>.md`. For each gap identified, create a GAP entry. Include frontmatter with tags for sub-field, relevance, and concepts connected.

### 7. Present to user

Show the organized list with recommendations. Ask: "Which of these should we include in the working bibliography? Any areas you want me to search deeper?"

## Approval Gate

User confirms which papers to include. Literature selection is a STANDARD verification decision — the user evaluates, but the AI presents options.

## Agent Team

- **literature-researcher** — Primary: searches and assesses
- **field-expert** — Support: provides context for papers found
