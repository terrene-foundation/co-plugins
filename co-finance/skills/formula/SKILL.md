---
name: formula
description: "Quick reference for finance formulas"
---

## Purpose

Provide a quick, focused reference for a specific finance formula or set of formulas on a topic. Shows the formula, defines every variable, explains when to use it, and walks through a worked example. Designed for fast lookup during study or problem-solving.

## Input

`$ARGUMENTS` contains the formula name or topic. Examples: "CAPM", "Sharpe ratio", "bond pricing", "present value of an annuity", "Black-Scholes", "WACC", "Gordon growth model", "put-call parity".

If `$ARGUMENTS` is empty, ask the student: "Which formula do you need? You can name it directly ('WACC') or describe what you are trying to calculate ('how to find the present value of future cash flows')."

## Topic Routing

Route to the appropriate course tutor for domain expertise:

| Formula Area | Tutor Agent |
|---|---|
| TVM, annuities, perpetuities | **fnce101-tutor** |
| WACC, NPV, IRR, capital budgeting | **corporate-finance-tutor** |
| Exchange rates, interest rate parity, PPP | **international-finance-tutor** |
| CAPM, Sharpe, portfolio theory, options | **fmi-tutor** |

## Formula Reference Format

For each formula, present:

### Formula Name
The standard name used in textbooks.

### Formula
```
[The formula in clear mathematical notation]
```

### Variables
| Symbol | Name | Units | Description |
|---|---|---|---|
| ... | ... | ... | ... |

Define every variable. Include units. Note which variables are inputs vs. outputs.

### When to Use
One to three sentences describing the scenario where this formula applies. Include:
- What question it answers
- What assumptions it requires
- When it should NOT be used (common misapplication)

### Worked Example
A step-by-step calculation with realistic numbers:

```
Given:
  [List all known values]

Find: [What we are solving for]

Step 1: [Description]
  [Calculation]

Step 2: [Description]
  [Calculation]

Answer: [Result with units and interpretation]
```

### Common Mistakes
- [Mistake 1]: [Why it is wrong and what to do instead]
- [Mistake 2]: [Why it is wrong and what to do instead]

### Related Formulas
- [Formula A] — [When you would use this instead]
- [Formula B] — [How it connects to the current formula]

### Source
Cite the textbook or paper where the formula originates or is best explained.

## Multiple Formulas on a Topic

If the student asks for a topic (e.g., "bond pricing") rather than a single formula, present all relevant formulas in a compact reference card:

```
## Bond Pricing Formulas

### 1. Bond Price (Coupon Bond)
[formula, variables, one-line description]

### 2. Current Yield
[formula, variables, one-line description]

### 3. Yield to Maturity (approximation)
[formula, variables, one-line description]

### 4. Duration (Macaulay)
[formula, variables, one-line description]

### 5. Modified Duration
[formula, variables, one-line description]

### 6. Convexity
[formula, variables, one-line description]
```

Follow with one worked example that uses multiple formulas together.

## Critical Rules

1. **Accuracy is non-negotiable.** Every formula must be mathematically correct and match the standard textbook form. Cite the source.

2. **Define every variable.** No undefined symbols. A student looking up a formula should not need to look up what the letters mean.

3. **Include units.** Rates in decimal vs. percentage, time in years vs. months, prices in currency — ambiguity causes errors.

4. **Note assumptions.** Every formula has assumptions (continuous vs. discrete compounding, constant rates, no taxes). State them.

5. **Show the common mistake.** For every formula, there is at least one error students make repeatedly. Call it out.

## Agent Team

- Appropriate **course tutor** — Domain expertise and formula verification
- **quantitative-analyst** — Verify mathematical accuracy
- **financial-literacy-expert** — Plain-language description of when to use each formula

## Skill References

- `19-formula-reference/` — Formula reference data (if populated)
- Relevant domain module from `.claude/skills/` based on the formula's subject area
