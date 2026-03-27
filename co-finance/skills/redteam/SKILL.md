---
name: challenge
description: "Stress-test your arguments and analysis from a critical perspective"
---

## What This Phase Does (present to student)

Challenge your work the way a tough but fair professor would — testing the strength of your arguments, the quality of your evidence, the soundness of your methodology, and the credibility of your sources. This is academic rigor testing, not proofreading.

## Your Role (communicate to student)

Review the feedback and decide how to respond to it. Not every critique requires a change — sometimes the right response is to acknowledge a limitation. But every critique deserves consideration. You decide what to fix, what to address with a caveat, and what to leave as is.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a project name, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/` (excluding `instructions/`)
3. If no workspace exists, ask the student to create one first
4. Read all files in `workspaces/<project>/briefs/` for student context (assignment requirements, rubric, professor's expectations)

## Phase Check

- Verify that drafts exist in the workspace to review
- Read `workspaces/<project>/03-structure/` for the intended argument structure
- Feedback goes into `workspaces/<project>/04-feedback/`
- If significant gaps are found, document them and suggest revisions (use `/assignment` or `/thesis` to address)

## Workflow

### 1. Read all drafts in the workspace

Review everything the student has produced so far — all sections, data analysis, charts, citations, and supporting materials. Understand the full scope of the work before critiquing individual parts.

### 2. Challenge each major claim

For every significant argument or conclusion in the work:

- **Is the evidence sufficient?** Does the claim rest on enough credible sources, or is it thinly supported?
- **Are there counterarguments?** Has the student addressed what critics of this position would say?
- **Is the reasoning valid?** Does the conclusion actually follow from the evidence, or are there logical gaps?
- **Is the claim appropriately scoped?** Is the student overclaiming (saying more than the evidence supports) or underclaiming (missing implications)?

### 3. Check methodology

If the work involves data analysis, modeling, or empirical methods:

- **Is the methodology appropriate** for the research question?
- **Are assumptions stated** and justified?
- **Are limitations acknowledged** honestly?
- **Is the data reliable?** Are sources credible and correctly cited?
- **Are calculations correct?** Do the numbers add up? Are formulas applied correctly?
- **Are results interpreted carefully?** Correlation vs. causation, statistical significance vs. practical significance, sample size limitations

### 4. Verify citations and sources

- **Are sources credible?** Peer-reviewed journals, established textbooks, reputable institutions — not blog posts or Wikipedia
- **Is attribution correct?** Are ideas properly credited? Are direct quotes marked and cited?
- **Are sources current?** For empirical claims, is the data recent enough to be relevant?
- **Is there sufficient breadth?** Does the student rely too heavily on one or two sources?
- **Is the citation format correct?** Consistent style (APA, Chicago, etc.) as required

### 5. Report findings as professor's feedback

Present findings in the tone of constructive academic feedback. Organize by severity:

- **Major concerns** — Issues that significantly weaken the work and should be addressed before submission (weak central argument, missing key evidence, methodological problems)
- **Moderate suggestions** — Areas that would meaningfully improve the work (underdeveloped sections, missing counterarguments, imprecise language)
- **Minor refinements** — Polish items that would elevate the quality (better transitions, stronger topic sentences, tighter conclusions)
- **Strengths** — What the student has done well (always include this — it helps the student know what to preserve)

For each finding, explain:

- What the issue is (in plain language)
- Why it matters (how it affects the argument or grade)
- How to address it (specific, actionable suggestion)

### 6. Iterate until convergence

If the student revises based on feedback:

- Re-read the revised sections
- Check whether the revisions actually address the concerns
- Identify any new issues introduced by the revisions
- Continue until the work is as strong as it can be

## Agent Teams

Deploy these agents as a challenge team:

**Core review team (always):**

- **peer-reviewer** — Evaluate argument strength, evidence quality, logical consistency
- **deep-analyst** — Identify structural weaknesses, gaps in reasoning, unstated assumptions
- **citation-specialist** — Verify source credibility, attribution accuracy, citation formatting

**Domain specialists (deploy based on the topic):**

- **quantitative-analyst** — Challenge methodology and calculations for quantitative work
- **financial-engineer** — Challenge valuation models, pricing assumptions, financial modeling
- **regulatory-compliance** — Check disclaimer requirements for any investment-related content
- **curriculum-designer** — Evaluate whether the work meets the learning objectives of the course

**Course-specific tutors (deploy based on subject area):**

- For corporate finance topics — challenge capital structure arguments, valuation assumptions
- For international finance topics — challenge exchange rate analysis, macro reasoning
- For portfolio theory topics — challenge optimization assumptions, risk measurement
- For behavioral finance topics — challenge bias identification, debiasing logic

Run multiple review rounds. Converge when all agents find no remaining significant issues.
