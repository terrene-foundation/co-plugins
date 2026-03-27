---
name: case
description: "Analyze a business case using structured frameworks"
---

## Purpose

Guide a student through a structured business case analysis using appropriate analytical frameworks. Produces a case writeup that demonstrates analytical rigor — identifying the core issue, applying frameworks, evaluating alternatives, and making a defensible recommendation.

## Input

`$ARGUMENTS` contains the case name, description, or assignment prompt. Examples: "Tesla capital structure decision", "analyze JPMorgan's acquisition of Bear Stearns", "Enron corporate governance failure", "evaluate Apple's dividend initiation in 2012".

If `$ARGUMENTS` is empty, ask the student: "What case would you like to analyze? Provide the case name or description, and let me know if there are specific frameworks your professor wants you to use (Porter's Five Forces, SWOT, DCF, etc.)."

## Workflow

### Step 1 — Understand the Case

Read or receive the case details and identify:

- **Company/situation**: Who is involved? What is the context?
- **Time period**: When did this happen? What was the market/economic environment?
- **Core issue**: What decision needs to be made, or what went wrong/right?
- **Key data**: What financial data, market data, or qualitative information is available?
- **Assignment requirements**: What frameworks are required? What deliverables?

### Step 2 — Select Analytical Frameworks

Choose frameworks based on the case type:

| Case Type | Primary Framework | Supporting Frameworks |
|---|---|---|
| **Industry analysis** | Porter's Five Forces | PESTEL, industry lifecycle |
| **Company strategy** | SWOT Analysis | Value chain, competitive positioning |
| **Valuation / M&A** | DCF Analysis | Comparable analysis, precedent transactions |
| **Capital structure** | Trade-off theory / Pecking order | WACC analysis, financial flexibility |
| **Investment decision** | NPV / IRR analysis | Payback period, sensitivity analysis |
| **Corporate governance** | Agency theory | Stakeholder analysis, governance mechanisms |
| **Financial distress** | Altman Z-Score | Liquidity analysis, restructuring options |
| **International** | Diamond model / Impossible trinity | Political risk, exchange rate analysis |

If the professor specified frameworks, use those. Otherwise, recommend the most appropriate ones and explain why.

### Step 3 — Apply Frameworks Systematically

For each selected framework, guide the student through:

**Porter's Five Forces:**
1. Threat of new entrants (barriers to entry, capital requirements, regulation)
2. Bargaining power of suppliers
3. Bargaining power of buyers
4. Threat of substitutes
5. Competitive rivalry

**SWOT Analysis:**
1. Strengths (internal, positive)
2. Weaknesses (internal, negative)
3. Opportunities (external, positive)
4. Threats (external, negative)
5. Cross-analysis: How can strengths exploit opportunities? How do weaknesses amplify threats?

**DCF Valuation:**
1. Project free cash flows (with explicit assumptions)
2. Determine appropriate discount rate (WACC or cost of equity)
3. Calculate terminal value (perpetuity growth or exit multiple)
4. Discount to present value
5. Sensitivity analysis on key assumptions

For each framework, insist on specificity — not "strong competitive position" but "37% market share in the U.S. smartphone market as of Q3 2024, supported by ecosystem lock-in (Apple, 10-K, 2024)."

### Step 4 — Evaluate Alternatives

Help the student identify and evaluate decision alternatives:

```
Alternative A: [Description]
  Pros: [Specific benefits with evidence]
  Cons: [Specific risks with evidence]
  Financial impact: [Quantitative analysis if data is available]

Alternative B: [Description]
  Pros: [Specific benefits with evidence]
  Cons: [Specific risks with evidence]
  Financial impact: [Quantitative analysis if data is available]

Alternative C: [Status quo / do nothing]
  Pros: [Why this might be acceptable]
  Cons: [Risks of inaction]
```

### Step 5 — Make a Recommendation

Guide the student to:

1. State a clear recommendation (choose one alternative)
2. Justify it with evidence from the analysis
3. Acknowledge the risks of the chosen path
4. Propose mitigation strategies for those risks
5. Define success metrics — how would you know if this was the right decision?

### Step 6 — Structure the Case Writeup

Produce a structured outline for the case writeup:

```
1. Executive Summary (1 paragraph — conclusion first)
2. Situation Analysis (company background, industry context, timeline)
3. Problem Statement (the core issue in one clear sentence)
4. Analysis (framework application with evidence)
5. Alternatives Evaluation (structured comparison)
6. Recommendation (with justification, risks, and mitigation)
7. Implementation Plan (if required — timeline, key steps, milestones)
8. Appendices (financial exhibits, calculations, supporting data)
```

## Critical Rules

1. **Evidence over assertion.** Every claim in a case analysis must be supported by data from the case, public financial statements, or credible sources. "The company is well-positioned" is not analysis; "The company's 24% ROIC exceeds its 10% WACC, indicating value creation (Annual Report, 2024)" is.

2. **Quantify when possible.** "Significant cost savings" is vague. "Estimated annual cost savings of $2.3 billion from supply chain consolidation (Management presentation, 2024)" is analytical.

3. **Address counterarguments.** A case analysis that only supports the recommendation is not credible. Acknowledge what could go wrong and explain why the recommendation is still the best option.

4. **Historical cases require hindsight discipline.** If analyzing a past event, the student should analyze based on information available at the time of the decision, then separately discuss what actually happened and why.

5. **Include disclaimers.** If the analysis includes valuations, projected returns, or investment recommendations, include appropriate disclaimers per this project's compliance rules.

## Agent Team

- **case-study-analyst** — Framework selection, systematic analysis, structured writeup
- **academic-writer** — Argument construction, evidence integration, prose quality
- **financial-engineer** — DCF models, valuation calculations (when quantitative analysis is needed)
- **quantitative-analyst** — Financial ratio analysis, data verification
- Appropriate **course tutor** — Domain expertise for the case's subject area

## Skill References

- `18-case-study-framework/` — Case analysis frameworks and templates
- `10-corporate-finance/` — Corporate finance concepts for capital structure, M&A, valuation cases
- `13-academic-writing/` — Academic prose standards for the writeup
