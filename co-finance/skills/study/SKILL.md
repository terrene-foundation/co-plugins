---
name: study
description: "Generate a structured study guide for a finance topic"
---

## Purpose

Create a structured study guide following progressive difficulty — definitions and intuition, formulas and worked examples, practice problems and common mistakes.

## Input

`$ARGUMENTS` contains the topic (e.g., "time value of money", "CAPM", "options Greeks").

If `$ARGUMENTS` is empty, ask: "What finance topic would you like to study?"

## Topic Routing

Route to the appropriate tutor:
- Introductory finance, TVM, financial statements: **fnce101-tutor**
- Corporate finance, capital structure, M&A, valuation: **corporate-finance-tutor**
- International finance, FX, balance of payments: **international-finance-tutor**
- Portfolio theory, derivatives, risk: **fmi-tutor**

## Study Guide Structure

### 1. What Is It?
Plain-language definition, no jargon without explanation. One-sentence flashcard summary.

### 2. Why Does It Matter?
Real-world context, analogy to anchor the concept, connection to prerequisites.

### 3. The Formula (if applicable)
Formula with every variable defined (with units), source citation, special cases and boundary conditions.

### 4. Worked Example
Step-by-step calculation with real-world context. Show intermediate steps. State result with interpretation.

### 5. Practice Problems
- **Level 1**: Direct formula application (2-3 problems)
- **Level 2**: Conceptual twist requiring understanding (2-3 problems)
- **Level 3**: Multi-step exam-style combining related concepts (1-2 problems)
- Answers provided separately

### 6. Common Mistakes
3-5 most frequent errors with explanations of why they are wrong and the correct approach.

### 7. Quick Reference Card
Compact formulas, key assumptions, related concepts, suggested next topics.
