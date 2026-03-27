---
name: explain
description: "Get a clear explanation of a finance concept"
---

## Purpose

Provide a clear explanation of a finance concept at the appropriate level. Uses plain language, analogies, and worked examples. Addresses common misconceptions.

## Input

`$ARGUMENTS` contains the concept and optionally the level (beginner/intermediate/advanced).

If `$ARGUMENTS` is empty, ask: "What finance concept would you like me to explain? You can also specify beginner, intermediate, or advanced."

Default to **intermediate** unless phrasing suggests otherwise ("what is..." = beginner, "derive the..." = advanced).

## Explanation Structure

### 1. One-Sentence Definition
No jargon, or define jargon in the same sentence.

### 2. Why It Matters
Who uses it, what problem it solves, what goes wrong without it.

### 3. Analogy
Real-world analogy to anchor the idea. Note where it breaks down.

### 4. How It Works (Level-Appropriate)
- **Beginner**: plain language, concrete scenario, no formulas
- **Intermediate**: formula with variable definitions, simple numerical example
- **Advanced**: full derivation, assumptions, edge cases, alternative approaches

### 5. Worked Example
Step-by-step with specific numbers and realistic scenario.

### 6. Common Misconceptions
2-3 frequent errors with correct understanding.

### 7. Connections
Prerequisites, what this enables next, related concepts often confused with this one.
