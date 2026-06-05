---
name: product-risk-radar
description: Use when a product manager wants to identify practical product, technical, operational, data, rollout, compliance, dependency, or customer-experience risks in a feature, plan, roadmap item, architecture, or code area. Produces a ranked risk radar with mitigations.
---

# Identify Product Risks in a Feature, Plan, or Code Area

## Goal

Turn a product idea, plan, feature, or code area into a ranked risk radar that a PM can act on. Focus on risks that could change scope, sequencing, confidence, launch readiness, or stakeholder communication.

## Inputs to request when missing

Ask for risk-shaping context:

- Decision, feature, launch, or code area being assessed.
- Target user, buyer, segment, and workflow.
- Current plan, scope, non-goals, launch date, and rollout model.
- Evidence available: analytics, research, support, sales, technical design, dependency list, legal/compliance review.
- Risk tolerance: prototype, beta, GA, enterprise, regulated, revenue-critical, or internal.

If missing, proceed with assumptions and make the missing risk drivers explicit.

## Senior PM standard

Risk analysis should change a plan. It should not be a long list of things that might go wrong.

Look for:

- Risks that should change sequencing, scope, rollout, staffing, dependency management, or stakeholder messaging.
- Risks where detection will be hard until after launch.
- Risks that are irreversible or expensive to unwind.
- Risks created by weak evidence, hidden dependencies, ambiguous ownership, or optimistic adoption assumptions.
- Risks that compound across product, technical, data, legal, support, and GTM workstreams.

## Risk lenses

Check these lenses and keep only the ones that matter:

- Customer promise: the feature may not solve the stated problem or may create confusing behavior.
- Workflow edge cases: important user paths, roles, permissions, locales, devices, or states are not covered.
- Data integrity: data could be missing, stale, duplicated, misclassified, or hard to migrate.
- Dependencies: another team, vendor, API, model, data pipeline, platform, or policy blocks success.
- Operational readiness: support, monitoring, rollback, incident handling, or migration plans are weak.
- Release strategy: rollout, experiments, flags, eligibility, or communications are under-specified.
- Security, privacy, and compliance: sensitive handling needs specialist review.
- Maintainability: the implementation path creates future delivery drag.
- Measurement: success metrics, guardrails, or baseline data are missing.

## Workflow

1. Identify the decision being made and the scope of the feature or plan.
2. Gather evidence from the prompt, documents, code, specs, analytics, or roadmap material.
3. Convert assumptions into explicit risk statements.
4. Score each meaningful risk on:
   - Impact: low, medium, high.
   - Likelihood: low, medium, high.
   - Detectability: easy, moderate, hard.
   - Reversibility: easy, moderate, hard.
5. Rank risks by practical actionability, not theoretical severity alone.
6. Recommend mitigations, owners, and decision gates.
7. State which risks should change the plan now.

## Output format

### Verdict

State whether the plan is low-risk, manageable with mitigations, risky but worth pursuing, or not ready.

### Top Risks

For each top risk:

- Risk.
- Evidence.
- Product impact.
- Mitigation.
- Owner or function.
- Decision gate or validation step.

### Risk Register

Use a compact table:

| Risk | Impact | Likelihood | Detectability | Reversibility | Mitigation | Owner |
| --- | --- | --- | --- | --- | --- | --- |

### Missing Information

List the minimum additional context needed to improve confidence.

### Plan Changes Required

State which scope, sequencing, rollout, ownership, or validation changes should happen because of the risk analysis.

## Quality bar

- Do not list generic risks unless they apply.
- Do not overstate compliance, security, or financial conclusions.
- Make mitigations concrete enough to assign.
- Call out risks that should change sequencing.
- Include detection and reversibility, not only impact.
