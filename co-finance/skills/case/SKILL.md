---
name: case
description: "Analyze a business case using structured frameworks"
---

## Purpose

Guide a student through structured business case analysis: identify the core issue, apply frameworks, evaluate alternatives, and make a defensible recommendation.

## Input

`$ARGUMENTS` contains the case name, description, or assignment prompt.

If `$ARGUMENTS` is empty, ask: "What case would you like to analyze? Include any specific frameworks your professor wants (Porter's Five Forces, SWOT, DCF, etc.)."

## Workflow

### Step 1 — Understand the Case

Identify: company/situation, time period and market context, core issue (decision or lesson), key data available, and assignment requirements.

### Step 2 — Select Analytical Frameworks

Choose frameworks based on case type:
- **Industry analysis**: Porter's Five Forces, PESTEL
- **Company strategy**: SWOT, value chain, competitive positioning
- **Valuation / M&A**: DCF, comparable analysis, precedent transactions
- **Capital structure**: trade-off theory, pecking order, WACC analysis
- **Investment decision**: NPV/IRR, sensitivity analysis
- **Corporate governance**: agency theory, stakeholder analysis
- **Financial distress**: Altman Z-Score, liquidity analysis
- **International**: diamond model, impossible trinity, political risk

Use professor-specified frameworks if provided.

### Step 3 — Apply Frameworks Systematically

Guide the student through each framework with specificity. Not "strong competitive position" but "37% market share in the U.S. smartphone market as of Q3 2024, supported by ecosystem lock-in (Apple, 10-K, 2024)."

### Step 4 — Evaluate Alternatives

For each alternative (including status quo): identify specific pros, cons, and financial impact with evidence.

### Step 5 — Make a Recommendation

Guide the student to: state a clear recommendation, justify with evidence, acknowledge risks, propose mitigation strategies, and define success metrics.

### Step 6 — Structure the Writeup

Outline: Executive Summary, Situation Analysis, Problem Statement, Analysis, Alternatives Evaluation, Recommendation, Implementation Plan (if required), Appendices.

## Critical Rules

1. **Evidence over assertion.** Every claim must be supported by data from the case or credible sources.
2. **Quantify when possible.** "Estimated annual cost savings of $2.3B" not "significant cost savings."
3. **Address counterarguments.** A one-sided analysis is not credible.
4. **Historical cases require hindsight discipline.** Analyze based on information available at decision time, then separately discuss what actually happened.
5. **Include disclaimers** for valuations, projected returns, or investment recommendations.
