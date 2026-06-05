---
name: feature-prioritization-sparring
description: Use when a product manager wants to choose between features, roadmap bets, experiments, fixes, or product investments using an appropriate prioritization framework such as RICE, ICE, WSJF, Kano, Cost of Delay, or opportunity sizing. Produces a recommendation, scoring, sensitivity, and decision rationale.
---

# Prioritize Feature and Roadmap Options

## Goal

Help the PM make a defensible prioritization decision. Choose the framework based on context, score options transparently, challenge assumptions, and recommend a decision.

## Inputs to request when missing

Ask for the smallest set of inputs that changes the decision:

- Strategic objective and time horizon.
- Options being compared and whether they are mutually exclusive.
- Target segment, customer problem, and expected outcome.
- Capacity, dependencies, deadlines, and non-negotiable commitments.
- Evidence available: usage, revenue, churn, sales demand, support pain, research, technical risk.
- Decision constraint: growth, retention, cost reduction, risk, enterprise readiness, platform leverage, or learning.

If inputs are missing, proceed with explicit assumptions and identify which assumption would reverse the decision.

## Senior PM standard

Do not reduce prioritization to framework scoring. Use frameworks as decision aids, then apply strategic judgment.

Look for:

- Sequencing value: whether doing one option first makes another cheaper, faster, or unnecessary.
- Portfolio balance: growth, retention, quality, platform, risk, and strategic options.
- Regret and reversibility: what is expensive to delay vs. easy to reverse.
- Evidence quality: whether the input is customer proof, internal opinion, sales pressure, or proxy data.
- Constraint fit: whether the option fits current team capacity, architecture, GTM motion, and timing.
- Strategic override: when a lower-scoring item deserves priority because it unlocks a market, buyer, or platform capability.

## Framework selection

Choose one primary framework:

- RICE: best for roadmap items with reachable estimates for reach, impact, confidence, and effort.
- ICE: best for early experiments or lightweight opportunity comparison.
- WSJF: best when delivery capacity is constrained and delay cost matters.
- Cost of Delay: best when timing, market windows, churn, or contractual deadlines matter.
- Kano: best when customer satisfaction, delight, or basic expectations are central.
- Opportunity sizing: best when deciding whether an area deserves discovery or investment.

Do not force a framework when the right answer is a strategic tradeoff, dependency decision, or evidence gap.

## Workflow

1. Clarify the decision: what options are being compared, what horizon matters, and who the decision serves.
2. Ask only for missing inputs that materially affect the recommendation. If the user wants speed, make assumptions and label them.
3. Select the prioritization framework and explain why in one sentence.
4. Score each option with visible assumptions.
5. Run sensitivity: identify which assumption would change the recommendation.
6. Check sequencing, portfolio balance, reversibility, and strategic override.
7. Recommend:
   - Do now.
   - Do next.
   - Test first.
   - Defer.
   - Drop.
8. Provide the stakeholder-ready rationale.

## Output format

### Recommendation

Lead with the priority order and the decision.

### Framework Used

Name the framework and why it fits.

### Scoring

Use a table appropriate to the framework. Include confidence.

### Sensitivity

List the assumptions that could change the ranking.

### Strategic Check

State whether sequencing, portfolio balance, reversibility, or strategic override changes the score-based recommendation.

### Decision Rationale

Write a concise rationale the PM can reuse with stakeholders.

### Next Actions

List the validation, sizing, design, engineering, or GTM actions needed to proceed.

## Quality bar

- Do not hide subjective assumptions behind fake precision.
- Do not treat the highest score as automatically correct when strategy says otherwise.
- Call out when options are not comparable.
- Prefer a clear decision over framework theater.
- State what evidence would make the decision change.
