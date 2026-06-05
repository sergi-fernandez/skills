---
name: codebase-quality-readout
description: Use when a product manager wants a PM-readable codebase health assessment without doing a pull request review, including maintainability, test confidence, release risk, architecture clarity, dependency risk, observability, and likely quality leverage points.
---

# Assess Codebase Quality for Product Planning

## Goal

Assess codebase health in language a PM can use for planning, risk management, and stakeholder conversations. This is not a PR review and should not produce a long list of style comments.

## Inputs to request when missing

Ask for context that determines the quality bar:

- Upcoming roadmap or launch that depends on this codebase.
- Risk tolerance: beta, GA, enterprise, regulated, internal, prototype, or revenue-critical.
- Team constraint: speed, onboarding, maintainability, reliability, compliance, or scaling.
- Known pain: flaky tests, slow releases, incidents, unclear ownership, costly changes, performance complaints.
- Whether the user wants a whole-repo readout or a focused area.

If no context is provided, assess general product-planning risk and state assumptions.

## Senior PM standard

Treat quality as a planning and option-value question. The output should help decide where to invest, what to delay, and what risk to communicate.

Look for:

- Quality debt that blocks specific roadmap options.
- Missing tests or observability that make outcomes hard to trust.
- Architecture patterns that increase marginal cost of future product changes.
- Release-safety gaps that change launch strategy.
- Dependencies or ownership patterns that create strategic fragility.
- Improvements that create leverage across multiple roadmap items, not only local cleanup.

## Assessment dimensions

Evaluate only dimensions supported by evidence:

- Maintainability: understandable structure, clear boundaries, duplication, complexity, dead code.
- Test confidence: meaningful unit, integration, e2e, regression, and fixture coverage.
- Release safety: build, deploy, migrations, feature flags, rollback, environments.
- Architecture clarity: module boundaries, domain model, service contracts, data flow.
- Dependency risk: outdated, abandoned, fragile, security-sensitive, or vendor-critical dependencies.
- Observability: logs, metrics, traces, alerts, dashboards, error handling.
- Product flexibility: how easily the codebase supports packaging, experiments, localization, permissions, analytics, and workflow changes.
- Team leverage: docs, onboarding, local setup, conventions, and reviewability.

## Workflow

1. Read repo orientation files and build/test configuration.
2. Inspect the source tree for architecture and ownership clues.
3. Inspect tests and CI clues before judging quality.
4. Sample representative implementation files rather than exhaustively reading everything.
5. Run safe commands only when helpful and available, such as test discovery, typecheck, lint, or dependency listing.
6. Convert findings into product implications: delivery speed, release risk, operational risk, planning confidence, and roadmap optionality.

## Output format

### Overall Readout

Give one of:

- Healthy enough to move fast.
- Generally sound with known weak spots.
- Manageable but slowing delivery.
- Risky for ambitious roadmap work.
- Not enough evidence.

### Scorecard

Use a compact scorecard:

| Dimension | Rating | Evidence | Product implication |
| --- | --- | --- | --- |

Ratings: strong, adequate, weak, unknown.

### Highest-Leverage Improvements

List the 3-5 improvements most likely to improve product delivery or reduce risk. Include the expected PM benefit.

### Roadmap Implications

State what the quality readout means for sequencing, scope, launch readiness, and stakeholder communication.

### Watchouts

List quality risks that should affect roadmap planning, launch readiness, or stakeholder communication.

## Quality bar

- Do not equate file count or framework choice with quality.
- Do not claim test coverage quality from presence of tests alone.
- Prefer concrete evidence over vibes.
- Keep recommendations scoped and pragmatic.
- Explain why each improvement matters for product outcomes, not only engineering hygiene.
