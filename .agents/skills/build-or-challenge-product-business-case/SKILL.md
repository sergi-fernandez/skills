---
name: build-or-challenge-product-business-case
description: Use when a product manager wants to build, draft, critique, or improve a product business case for a feature, product, pricing change, roadmap bet, or investment. Covers financial levers, missing data, internal data to request, market benchmarks, revenue, cost, margin, payback, unit economics, break-even, sensitivity, cannibalization, and financial risks. Not a substitute for finance, tax, legal, or investment advice.
---

# Build or Challenge a Product Business Case

## Goal

Help a PM build or pressure-test the financial case behind a product decision. The user may already have a business case, or may only have an idea and a few numbers. In both cases, identify the commercial levers, missing data, assumptions, sensitivities, and decision implications. Do not present the result as formal financial advice.

## Modes

Choose the mode that fits the request:

- Challenge an existing business case: inspect the user's model, assumptions, formulas, source data, scenarios, and conclusion. Find weak assumptions, missing levers, sensitivity, optimistic bias, and decision risks.
- Build a first business case: create a draft model from the available context, identify the missing inputs, use ranges where needed, and show which data would improve confidence.
- Data discovery: point the user to internal and external data sources that could support or falsify the case.
- Business plan draft: turn the model into a concise plan with recommendation, assumptions, go-to-market implications, risks, and next validation steps.

## Inputs to request when missing

Ask only for inputs that materially change the model. Prioritize:

- Decision: approve investment, size opportunity, price, sequence, defend roadmap, or kill idea.
- Eligible base: customers, accounts, seats, users, transactions, or usage units.
- Current monetization: ARR, ARPA, ACV, gross margin, plan mix, discounting, expansion, churn.
- Adoption logic: expected attach, conversion, ramp curve, buyer segment, sales motion, implementation friction.
- Price logic: current willingness-to-pay evidence, competitor pricing, packaging constraints, procurement limits.
- Cost logic: build capacity, ongoing engineering, support, infra, vendor, data/model/API, onboarding, and compliance costs.
- Time horizon and hurdle: payback target, margin target, strategic rationale, opportunity cost.

If these are unavailable, proceed with ranges and make the missing data request explicit.

## Senior PM standard

Build a driver tree before presenting numbers. Identify the few assumptions that dominate the business case and test whether the recommendation survives conservative, base, and upside cases.

Look for:

- Whether the business case depends more on adoption, price, margin, retention, or speed to launch.
- Whether upside is incremental or cannibalizes existing revenue.
- Whether the investment creates strategic option value even if near-term revenue is modest.
- Whether costs are one-time, variable, or recurring operating drag.
- Whether the case is finance-led, strategy-led, customer-retention-led, or risk-reduction-led.
- Whether the user's current evidence is sufficient for approval or only for further discovery.

## Financial lenses

Use the relevant lenses:

- Revenue: price, volume, conversion, expansion, retention, attach rate, usage, seasonality.
- Cost: build cost, support cost, infrastructure cost, data/model cost, operations, onboarding, maintenance.
- Margin: gross margin, contribution margin, variable cost, fixed cost allocation.
- Payback: time to recover investment.
- Unit economics: customer-level or transaction-level value and cost.
- Cannibalization: revenue displaced from existing products or plans.
- Opportunity cost: what roadmap capacity is displaced.
- Risk: uncertainty, dependency, compliance, market, pricing, and adoption risks.

## Common business-case levers

Consider these levers and keep only the relevant ones:

- Addressable base: total customers, eligible customers, active users, accounts, seats, transactions, or usage volume.
- Adoption: conversion rate, attach rate, migration rate, activation rate, trial-to-paid, seat expansion, usage growth.
- Pricing: list price, discounting, packaging, metering, seat count, overage, enterprise minimums, price increases, contract length.
- Retention: churn, renewal rate, expansion, contraction, reactivation, cohort behavior.
- Sales motion: self-serve, product-led growth, sales-led, channel, partner, customer success assisted.
- Cost to serve: infrastructure, data/model/API cost, support tickets, onboarding, implementation, vendor fees, operations.
- Build and maintenance: engineering, design, data, security, legal, support enablement, ongoing maintenance.
- Time: launch date, ramp curve, payback period, seasonality, market window, competitive timing.
- Cannibalization and substitution: revenue displaced from existing plans, services, or adjacent products.
- Risk adjustment: confidence haircut, adoption range, cost overrun, delayed launch, slower ramp.

## Data to request or search for

Start with internal sources when available:

- Billing, CRM, data warehouse, product analytics, usage logs, support tickets, customer success notes, sales pipeline, win-loss notes, renewal data, pricing history, discounting reports, infrastructure cost reports, roadmap capacity, incident or support cost data.

If internal data is missing or market assumptions matter, use web research when allowed and needed. Look for current and credible sources such as company reports, public benchmarks, market research, pricing pages, competitor packaging, analyst reports, government or industry data, and reputable financial filings.

When using web data:

- Prefer recent sources and state the source date.
- Treat market benchmarks as ranges, not truth.
- Separate external market evidence from internal company evidence.
- Do not overfit public averages to a specific product without explaining why they apply.

## Workflow

1. Identify the decision and financial question.
2. Determine whether the user is asking to build a new business case, challenge an existing one, or both.
3. Extract known numbers and label missing numbers.
4. Build a driver tree of the business levers that drive the case.
5. Point the user to relevant internal data sources and, when useful, current external sources to research.
6. Build or critique the assumption model in plain language.
7. Calculate or estimate:
   - Base case.
   - Conservative case.
   - Upside case.
   - Break-even point when possible.
   - Risk-adjusted case when uncertainty is high.
8. Identify the assumptions with the biggest effect on the decision.
9. State the approval threshold or kill criteria.
10. Draft the business plan narrative if requested.
11. Recommend what to do next: approve, test pricing, narrow scope, collect data, involve Finance, sequence later, or stop.

## Output format

### Recommendation

State the business-case verdict and decision implication.

### Known Inputs, Missing Inputs, and Data Sources

List:

- Known inputs.
- Assumed ranges.
- Missing inputs.
- Where to look internally.
- What to research externally, if needed.

### Business-Case Model

Use a compact table:

| Case | Key assumptions | Revenue or value | Cost | Margin or payback | Interpretation |
| --- | --- | --- | --- | --- | --- |

### Driver Tree

Show the formula or logic chain behind the model, for example: eligible base x adoption x price x retention minus variable and fixed costs.

### Sensitivity

List the variables that matter most and what would change the decision.

### Decision Threshold

State what must be true for this to be worth doing, and what evidence would make you stop or defer.

### Business Plan Draft

When useful, provide a concise plan:

- Opportunity.
- Target customer or segment.
- Commercial mechanism.
- Investment required.
- Expected upside and downside.
- Key risks.
- Validation plan.
- Decision gate.

### Risks and Follow-Up

List financial risks, data to collect, and when to involve Finance, Legal, or Compliance.

## Quality bar

- Do not invent precise numbers when ranges are more honest.
- State formulas when doing calculations.
- Use conservative assumptions when evidence is weak.
- Tell the user exactly which missing numbers would most improve the case.
- Use web research only when current external benchmarks or market direction are relevant.
- Flag specialist review for accounting, tax, securities, legal, or regulated claims.
- Do not present a spreadsheet-shaped answer without a recommendation.
