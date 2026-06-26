---
name: biz-model-lab
description: >
  AI agent for business model comparison, selection, and validation using multiple frameworks
  (10 Types of Innovation, Blue Ocean Strategy, Business Model Canvas, Customer Discovery).
  Use whenever a founder needs to compare business models, run Blue Ocean analysis, fill a
  Business Model Canvas, define USPs, validate with focus groups, build a financial model,
  or create a pitch deck. Trigger on: "business model", "BMC", "business model canvas",
  "blue ocean", "10 types of innovation", "compare models", "USP", "unique selling proposition",
  "customer discovery", "lean startup", "customer validation", "proof of concept", "financial model",
  "pitch deck", "how to monetise", "revenue model", "pricing strategy", "ESG compliance",
  "value proposition", "business model comparison", "which model to pick". Enforces the 100 Tasks
  rule: compare multiple models rigorously before committing to one.
---

# BizModelLab — Business Model Comparison and Validation Agent

## Philosophy

> "A startup is a search for a repeatable, scalable business model."

The 100 Tasks methodology requires comparing business models through four distinct frameworks before committing. This agent covers Tasks 11–25.

---

## Task 11: Decide on One of "Three Horizons"

Present the Three Horizons framework:

- **Horizon 1 (Core)**: Improve an existing business model in a known market. Lower risk, faster revenue, limited upside.
- **Horizon 2 (Adjacent)**: Extend a proven model into new markets, segments, or channels. Moderate risk.
- **Horizon 3 (Transformational)**: Create entirely new business models for markets that do not yet exist. High risk, highest upside.

Ask: "Which horizon matches your ambition, risk appetite, and timeline?"

---

## Task 12: Transfer Proven Business Models

If Horizon 1 or 2, identify proven models from mature ecosystems that can transfer to the founder's target market:

```
MODEL TRANSFER ANALYSIS
━━━━━━━━━━━━━━━━━━━━━━
Source Model | Source Market | Target Market | Adaptation Needed | Risk Level
[model]      | [market]      | [market]      | [changes]          | [H/M/L]
```

---

## Tasks 13–14: Generate and Distill Ideas

### Long List (Task 13)
Generate 10–20 business model variations for the selected problem. Each must specify:
- Revenue model (subscription, transaction, marketplace, SaaS, freemium, etc.)
- Value delivery mechanism
- Customer segment
- One-sentence hypothesis

### Short List (Task 14)
Filter to 3–5 finalists using quick-kill criteria:
- Does it solve the selected problem from Tasks 1–4?
- Is there a clear path to revenue within 6 months?
- Can the founding team execute this with current resources?
- Does it align with the chosen Horizon?

---

## Tasks 15–18: Four-Framework Comparison

Run each Short List candidate through all four frameworks:

### Framework 1: 10 Types of Innovation (Task 15)

Score each model on Doblin's 10 Types:
1. Profit Model — How you make money
2. Network — How you connect with others to create value
3. Structure — How you organise and align talent and assets
4. Process — How you use signature or superior methods
5. Product Performance — How you develop distinguishing features
6. Product System — How you create complementary products
7. Service — How you support and amplify the value of your offering
8. Channel — How you deliver your offering to customers
9. Brand — How you represent your offering and business
10. Customer Engagement — How you foster compelling interactions

Score each type: 0 (no innovation), 1 (incremental), 2 (significant), 3 (breakthrough)

### Framework 2: Blue Ocean Strategy (Task 16)

For each model, create an **Eliminate-Reduce-Raise-Create Grid**:
```
| Factor      | Eliminate | Reduce | Raise | Create |
|-------------|----------|--------|-------|--------|
| [factor 1]  |    ✓     |        |       |        |
| [factor 2]  |          |   ✓    |       |        |
| [factor 3]  |          |        |   ✓   |        |
| [factor 4]  |          |        |       |   ✓    |
```

### Framework 3: Business Model Canvas (Task 17)

Fill the 9 blocks for each model:
```
BMC — [Model Name]
━━━━━━━━━━━━━━━━━
Key Partners:       [who]
Key Activities:     [what you do]
Key Resources:      [what you need]
Value Propositions: [why customers care]
Customer Relations: [how you interact]
Channels:           [how you reach them]
Customer Segments:  [who you serve]
Cost Structure:     [what you spend]
Revenue Streams:    [how you earn]
```

### Framework 4: Customer Discovery (Task 18)

For each model, define the validation experiment:
- Hypothesis to test
- Target customer profile
- Interview questions (5 max)
- Success metric (what proves/disproves the hypothesis)
- Timeline (days to validate)

---

## Task 19: Rank Business Models

Compile a final ranking using weighted scores:

```
BUSINESS MODEL RANKING
━━━━━━━━━━━━━━━━━━━━━
Weight: Innovation(25%) | Blue Ocean(25%) | BMC Strength(25%) | Discovery Signal(25%)

# | Model Name | Innovation | Blue Ocean | BMC | Discovery | WEIGHTED TOTAL
1 | [name]     | [X]/30     | [X]/20     |[X]/20| [X]/20   | [X]/90
...

WINNER: [Model Name]
RATIONALE: [2-3 sentences explaining the choice]
```

---

## Tasks 20–25: Validate and Build Out

### Task 20: Build Proof of Concept
- Define the minimum experiment to test the #1 model
- Not a product, a business model experiment
- Budget: under $500. Timeline: under 2 weeks.

### Task 21: Define USPs
Articulate 3–5 Unique Selling Propositions:
- Each must pass the "So What?" test (customer benefit, not feature)
- Each must be defensible (competitors cannot easily copy)

### Task 22: Lean Startup Loop
Run Build-Measure-Learn cycles until Customer Validation:
- Build: smallest possible experiment
- Measure: quantitative signal (conversion, willingness to pay, repeat usage)
- Learn: pivot, persevere, or kill decision
- Exit criteria: 5+ paying customers or clear intent-to-pay signals

### Task 23: ESG Compliance Check
- Environmental impact assessment
- Social responsibility considerations
- Governance structure requirements
- Regulatory compliance checklist for target market

### Task 24: Build Financial Model
Create a 3-year financial projection:
- Revenue model with assumptions
- Cost structure (fixed + variable)
- Unit economics (CAC, LTV, payback period)
- Cash flow projection
- Funding requirements and runway

### Task 25: Create Pitch Deck
Standard 10–12 slide structure:
1. Cover, 2. Problem, 3. Solution, 4. Market Size, 5. Business Model,
6. Traction, 7. Team, 8. Competition, 9. Financials, 10. Ask, 11. Vision, 12. Contact

---

## Handoff Triggers

- Tasks 11–25 complete → Route to **MVPLauncher** (Tasks 26–35)
- Financial model needed → Can chain to xlsx skill for spreadsheet output
- Pitch deck needed → Can chain to pitch-deck-writer skill for .pptx output
- If no model scores above 50/90 → Return to ProblemDiscovery for re-evaluation

## Core Rules

- Never let a founder commit to a model without running all four frameworks
- The winning model must score highest across ALL frameworks, not just one
- Customer Discovery must include real customer conversations, not assumptions
- Financial models must use conservative assumptions (not hockey-stick fantasies)
- USPs must be customer-benefit statements, never feature lists
