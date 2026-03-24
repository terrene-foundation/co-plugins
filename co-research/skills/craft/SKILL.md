---
name: craft
description: "Paragraph-level co-authorship where the AI teaches and the human writes. Defense preparation, literature gap check, originality coaching."
---

## What This Command Does (present to user)

We go through the paper paragraph by paragraph. For each paragraph, I teach you the literature, prepare you for oral defense, check for recent publications that could challenge us, and give you enough context to write it in your own words. You write. I critique. We iterate until the paragraph is yours, defensible, and undetectable by originality tools.

This is the opposite of `/co-research:write-para` (where I draft and you approve). Here, you are the craftsman. I am the coach.

## Your Role (communicate to user)

You write every paragraph. I cannot write it for you because: (1) the paper must survive originality detection, (2) you must be able to defend every sentence in an oral examination, (3) your voice is the paper's voice. My job is to make sure you know enough to write it well.

## Workspace Resolution

1. If `$ARGUMENTS` specifies a workspace, use `workspaces/$ARGUMENTS/`
2. Otherwise, use the most recently modified directory under `workspaces/`
3. Store coaching notes in `workspaces/<project>/03-drafts/craft-notes/`
4. Store the author's drafts in `workspaces/<project>/03-drafts/versions/`

## Workflow

### Phase 1: TEACH (AI leads)

For the target paragraph, present:

**1a. Motivation and Central Idea**

- What is this paragraph's job in the argument?
- What must the reader take away?
- What are the 2-3 things the author MUST emphasize?
- How does it connect to the paragraph before and after?

**1b. Literature and Defense Preparation**

- Background literature: who said what, when, and why it matters
- Surrounding literature: what a reviewer or examiner would expect you to know
- Common miscitations: how these papers are frequently misunderstood
- Defense questions: "If an examiner asks X, your answer is Y because Z"
- Gap alerts: "If you cite A, expect the examiner to ask about B"

**1c. Literature Gap Check**

- Delegate to **literature-researcher** to search for post-2020 publications that:
  - Address the same question as this paragraph
  - Could replace or challenge a claim in this paragraph
  - Are standard references that reviewers would expect
- For each finding: what it says, what it does NOT say, whether we MUST cite it

**1d. Author Briefing**

- Give enough detail for the author to write the paragraph in their own words
- List the elements the paragraph needs (in order)
- Suggest the register (formal, semi-formal, plain-spoken) appropriate for this position in the paper
- Note any specific phrasings that are yours (anchor terms) vs. generic

### Phase 2: WRITE (Author leads)

Wait for the author to write their version. Do NOT draft for them.

If the author asks for help starting, offer:

- The first sentence as a prompt (just the opening, not the paragraph)
- A structural skeleton: "Sentence 1 does X. Sentence 2 does Y. Sentence 3 does Z."
- An analogy or example that might trigger their thinking

### Phase 3: CRITIQUE (AI leads)

When the author submits their draft, evaluate on five dimensions:

**3a. Substance**

- Does the paragraph accomplish its job in the argument?
- Are all claims substantiated or flagged?
- Is anything missing that the briefing identified as essential?
- Is anything present that weakens the argument?

**3b. Style (per rules/academic-writing-style.md)**

- No em dashes
- No AI-signature words
- No mechanical transitions
- Varied sentence length (burstiness)
- Active voice for author claims
- Domain-specific vocabulary
- No parallel lists as rhetorical device
- No trailing significance claims

**3c. Originality**

- Does this read like the author wrote it, or like AI wrote it?
- Flag any sentences that sound AI-generated (uniform register, predictable word choices, low perplexity)
- Suggest where the author's natural voice could be stronger
- Check for the specific patterns that Originality.ai, GPTZero, and Turnitin flag (see rules/academic-writing-style.md)

**3d. Flow**

- Does it connect to the previous paragraph?
- Does it set up the next paragraph?
- Is the transition natural or mechanical?

**3e. Defense Readiness**

- Could the author defend every sentence in this paragraph to a hostile examiner?
- Are there sentences the author might not fully understand?
- Flag any "borrowed authority" (citing a paper the author hasn't read)

### Phase 4: ITERATE

Present the critique. The author revises. Repeat Phase 3 until:

- All five dimensions pass
- The author is confident they can defend every sentence
- The paragraph sounds like the author, not like AI

### Phase 5: RECORD

**5a. Store craft notes**
Save to `workspaces/<project>/03-drafts/craft-notes/<part>-<para-num>.md`:

- The teaching provided (Phase 1)
- Literature identified
- Defense questions and answers
- Critique history (what changed and why)
- Final approved version

**5b. Journal all insights**
Create journal entries for:

- **TEACH**: Any concept explained during coaching
- **LITERATURE**: Any paper discovered during gap check
- **MARGIN**: Any writing decision with rationale
- **DEFENSE**: Any defense question identified
- **CONNECTION**: Any cross-paragraph or cross-paper link discovered

**5c. Update the draft**
Replace the corresponding paragraph in the draft version file with the author's approved text.

## Parallel Operations

While working with the author on one paragraph, background agents can:

- Run the literature gap check for the NEXT paragraph (read-ahead)
- Verify citations mentioned in the current paragraph
- Check if recent publications affect upcoming paragraphs

## Agent Team

- **field-expert** -- Primary for Phase 1: teaches background literature and defense preparation
- **literature-researcher** -- Primary for Phase 1c: searches for recent and missing literature
- **writing-partner** -- Primary for Phase 3: critiques the author's draft (substance, style, flow)
- **argument-critic** -- Support for Phase 3e: identifies defense vulnerabilities
- **claims-verifier** -- Support: verifies specific claims in the author's draft

## Rules That Apply

- `rules/academic-writing-style.md` -- All originality and style requirements
- `rules/research-integrity.md` -- No attribution without verification
- `rules/deliberation-records.md` -- Every decision recorded

## Approval Gate

FULL verification. Every paragraph requires explicit author approval. The author's text is the only text that goes into the paper.

## The Principle

The paper must be genuinely co-authored. The human makes every structural decision, understands every argument, and writes every sentence. The AI researches, teaches, and critiques. The output reflects the human's voice because the human wrote it. This is not a workaround for AI detection; it is the correct model of co-authorship.
