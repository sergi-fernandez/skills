---
name: write-product-decision-and-requirements-brief
description: Use when a product manager wants to turn product context into a concise decision and requirements brief that clearly states the problem, users, goals, scope, non-goals, options, chosen direction, metrics, risks, rollout, and open questions. Use instead of acronym-heavy PRD wording when clarity for mixed audiences matters.
---

# Write a Product Decision and Requirements Brief

## Goal

Create a concise product decision and requirements artifact that is useful for alignment across Product, Engineering, Design, Data, GTM, Support, and leadership. Prefer a crisp brief over a long template unless the user asks for a full PRD.

## Inputs to request when missing

Ask for the minimum context needed to write a decision-grade brief:

- Decision to make and deadline.
- Target segment, user, buyer, and workflow.
- Evidence behind the problem and current alternative.
- Options considered and why they were rejected or kept.
- Success metrics, guardrails, baseline, and expected timeframe.
- Constraints: technical, legal, compliance, GTM, support, migration, pricing, or dependency.
- Launch scope, non-goals, and rollout risk.

If the user has partial notes, draft the brief and mark unresolved sections clearly.

## Senior PM standard

The brief should force alignment on tradeoffs. It should not read like a generic requirements template.

Look for:

- Decision clarity: what is being decided now and what is deliberately deferred.
- Strategic fit: why this matters relative to company or product goals.
- Evidence quality: whether the problem is proven, inferred, or speculative.
- Option logic: why the chosen path beats credible alternatives.
- Scope discipline: what is excluded and why.
- Launch readiness: what must be true before beta, GA, or full rollout.
- Measurement logic: whether metrics can actually prove success or detect harm.

## Workflow

1. Identify the decision or product change.
2. Extract the problem, target users, customer job, and business goal.
3. Clarify scope and non-goals.
4. Capture options considered and the recommended decision.
5. Define success metrics and guardrails.
6. Identify dependencies, risks, rollout plan, and open questions.
7. State decision gates and unresolved tradeoffs.
8. Write in a form that can be shared with Engineering, Design, Data, GTM, and leadership.

## Default brief structure

Use this structure:

### Decision

One paragraph stating what should be built, changed, tested, or not done.

### Context

The business and customer context behind the decision.

### Problem

The user problem or job-to-be-done, with evidence if available.

### Goals and Non-Goals

Clear goals, explicit non-goals, and constraints.

### Users and Use Cases

Primary users, segments, workflows, and edge cases.

### Scope

Must-have, should-have, and out-of-scope items.

### Requirements

Functional requirements, UX considerations, data or analytics needs, permissions, localization, performance, and operational needs when relevant.

### Options Considered

Briefly compare options and why the recommendation wins.

### Tradeoffs and Decision Gates

State what is being traded off and what evidence or milestone could change the decision.

### Metrics

Success metrics, guardrails, baseline needs, and review cadence.

### Risks and Dependencies

Risks, mitigations, owners, and decision gates.

### Rollout

Launch path, experiment or feature flag plan, support and GTM considerations.

### Open Questions

Questions that must be resolved before build, launch, or scale.

## Quality bar

- Avoid filler sections with no content.
- Make the decision explicit.
- Spell out acronyms unless the audience already uses them.
- Use plain language over process jargon.
- State assumptions and unresolved questions.
- Do not fabricate evidence.
- Make the brief usable for a decision meeting, not just documentation.
