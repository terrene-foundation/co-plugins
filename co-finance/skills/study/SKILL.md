---
name: study
description: "Generate a structured study guide for a finance topic"
---

## Purpose

Create a comprehensive study guide for a finance topic. The guide follows progressive difficulty — starting with definitions and intuition, building to formulas and worked examples, and finishing with practice problems and common mistakes.

## Input

`$ARGUMENTS` contains the topic to study. Examples: "time value of money", "CAPM", "bond pricing", "options Greeks", "balance of payments".

If `$ARGUMENTS` is empty, ask the student: "What finance topic would you like to study? You can name a concept (e.g., 'present value'), a course area (e.g., 'corporate finance'), or a specific formula (e.g., 'Black-Scholes')."

## Topic Routing

Route to the appropriate course tutor based on the topic:

| Topic Area | Tutor Agent | Examples |
|---|---|---|
| Introductory finance, TVM, financial statements, basics | **fnce101-tutor** | Present value, compound interest, financial ratios |
| Corporate finance, capital structure, M&A, valuation | **corporate-finance-tutor** | WACC, NPV, capital budgeting, dividend policy |
| International finance, FX, balance of payments | **international-finance-tutor** | Exchange rates, PPP, interest rate parity, currency crises |
| All other topics (portfolio theory, derivatives, risk) | **fmi-tutor** | CAPM, Black-Scholes, VaR, efficient frontier |

Always also engage the **concept-explainer** (financial-literacy-expert) to ensure plain-language explanations and analogies are included.

## Study Guide Structure

Generate the study guide in this order:

### 1. What Is It? (Definition)
- Plain-language definition — no jargon without immediate explanation
- One-sentence summary a student could use on a flashcard

### 2. Why Does It Matter? (Intuition and Motivation)
- Real-world context: when and why professionals use this concept
- Analogy to anchor the abstract idea in everyday experience
- Connection to prerequisites — what the student should already know

### 3. The Formula (if applicable)
- Formula with every variable clearly defined
- Units for each variable
- Source citation (textbook or paper)
- Special cases and boundary conditions

### 4. Worked Example
- Step-by-step calculation with real-world context
- Show intermediate steps — do not skip from setup to answer
- Explain what each step accomplishes
- State the result in a complete sentence with interpretation

### 5. Practice Problems (Progressive Difficulty)
- **Level 1 — Direct application**: Plug numbers into the formula (2-3 problems)
- **Level 2 — Conceptual twist**: Requires understanding, not just calculation (2-3 problems)
- **Level 3 — Exam-style**: Multi-step problems combining this topic with related concepts (1-2 problems)
- Provide answers separately so the student can attempt before checking

### 6. Common Mistakes
- List the 3-5 most frequent errors students make with this topic
- For each mistake, explain why it is wrong and what the correct approach is
- Include relevant behavioral biases if applicable

### 7. Quick Reference Card
- Formula(s) in compact form
- Key assumptions
- Related concepts with brief descriptions
- Suggested next topics to study

## Presentation

- Use clear headings and formatting for easy scanning
- Include a disclaimer on any content showing returns or performance data
- Keep language accessible — explain jargon on first use
- Use specific numbers in examples, not abstract variables

## Agent Team

- Appropriate **course tutor** (based on routing above)
- **financial-literacy-expert** (concept-explainer) — plain-language explanations and analogies
- **quantitative-analyst** — verify formula accuracy and numerical examples

## Skill References

- Relevant module from `.claude/skills/` based on topic area
- `19-formula-reference/` for formula quick-reference data (if populated)
