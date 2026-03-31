---
name: formula
description: "Quick reference for finance formulas"
---

## Purpose

Provide a quick, focused reference for a finance formula or set of formulas. Shows the formula, defines every variable, explains when to use it, and walks through a worked example.

## Input

`$ARGUMENTS` contains the formula name or topic (e.g., "CAPM", "bond pricing", "WACC", "Black-Scholes").

If `$ARGUMENTS` is empty, ask: "Which formula do you need? Name it directly ('WACC') or describe what you are trying to calculate."

## Topic Routing

Route to the appropriate tutor:
- TVM, annuities, perpetuities: **fnce101-tutor**
- WACC, NPV, IRR, capital budgeting: **corporate-finance-tutor**
- Exchange rates, interest rate parity, PPP: **international-finance-tutor**
- CAPM, Sharpe, portfolio theory, options: **fmi-tutor**

## Formula Reference Format

For each formula, present:

1. **Formula Name** — standard textbook name
2. **Formula** — clear mathematical notation
3. **Variables** — every symbol defined with units, noting inputs vs. outputs
4. **When to Use** — what question it answers, required assumptions, and when it should NOT be used
5. **Worked Example** — step-by-step calculation with realistic numbers, showing intermediate steps, result with units and interpretation
6. **Common Mistakes** — why each is wrong and what to do instead
7. **Related Formulas** — when to use alternatives and how they connect
8. **Source** — textbook or paper reference

## Multiple Formulas on a Topic

If the student asks for a topic (e.g., "bond pricing") rather than a single formula, present all relevant formulas in a compact reference card with formula, variables, and one-line description for each. Follow with one worked example using multiple formulas together.

## Critical Rules

1. **Accuracy is non-negotiable.** Every formula must match the standard textbook form. Cite the source.
2. **Define every variable.** No undefined symbols.
3. **Include units.** Rates in decimal vs. percentage, time in years vs. months — ambiguity causes errors.
4. **Note assumptions.** Continuous vs. discrete compounding, constant rates, no taxes — state them.
5. **Show the common mistake.** Every formula has at least one frequent student error. Call it out.
