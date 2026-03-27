---
name: explain
description: "Get a clear explanation of a finance concept"
---

## Purpose

Provide a clear, accessible explanation of a finance concept at the appropriate level for the student. Uses plain language, real-world analogies, and worked examples. Proactively addresses common misconceptions.

## Input

`$ARGUMENTS` contains the concept and optionally the desired level. Format: `<concept>` or `<concept> <level>`.

Examples:
- "CAPM" — defaults to intermediate
- "bond duration beginner" — explains at introductory level
- "Black-Scholes advanced" — explains with full mathematical detail
- "what is beta" — infers beginner from the phrasing

**Levels**:
- **beginner** — No assumed knowledge. Uses analogies and everyday language. Avoids formulas.
- **intermediate** — Assumes basic finance literacy. Includes formulas with full variable definitions.
- **advanced** — Assumes solid quantitative background. Covers edge cases, assumptions, and limitations in depth.

If `$ARGUMENTS` is empty, ask the student: "What finance concept would you like me to explain? You can also say what level you want — beginner, intermediate, or advanced."

If no level is specified, default to **intermediate** unless the phrasing suggests otherwise ("what is..." implies beginner, "derive the..." implies advanced).

## Explanation Structure

### 1. One-Sentence Definition
A single sentence that captures the essence of the concept. No jargon — or if jargon is unavoidable, define it in the same sentence.

### 2. Why It Matters
- Who uses this concept and when?
- What problem does it solve?
- What would go wrong without it?

### 3. Analogy
A real-world analogy to anchor the abstract idea. The analogy must be accurate — note where it breaks down.

Example: "Duration is like the 'center of gravity' of a bond's cash flows. A bond with longer duration is more sensitive to interest rate changes, just as a longer seesaw amplifies small movements at the fulcrum."

### 4. How It Works (Level-Appropriate)

**Beginner**: Explain the mechanics in plain language with a concrete scenario. No formulas.

**Intermediate**: Introduce the formula with clear variable definitions and units. Walk through a simple numerical example.

**Advanced**: Present the full mathematical derivation or proof. Discuss assumptions, edge cases, and when the concept fails. Compare with alternative approaches.

### 5. Worked Example
A step-by-step calculation (intermediate and advanced) or a narrative walkthrough (beginner) using specific numbers and a realistic scenario.

### 6. Common Misconceptions
List 2-3 things students frequently get wrong about this concept, and explain the correct understanding.

### 7. Connections
- **Prerequisites**: What the student should already understand
- **Builds to**: What this concept enables them to learn next
- **Related concepts**: Nearby ideas that are often confused with this one

## Tone and Style

- Warm, encouraging — the student is learning, not being tested
- Specific numbers in examples (not abstract variables)
- Define every term on first use
- No condescension — "This is actually simpler than it sounds" is fine; "This is basic stuff" is not
- Use formatting (headers, bold, bullet points) for easy scanning

## Agent Team

- **financial-literacy-expert** (concept-explainer) — Plain-language explanations, analogies, misconception correction
- Appropriate **course tutor** — Domain expertise for the specific concept
- **quantitative-analyst** — Verify formula accuracy and numerical examples (for intermediate/advanced)

## Skill References

- Relevant module from `.claude/skills/` based on the concept's domain
- `19-formula-reference/` for formula data (if populated)
