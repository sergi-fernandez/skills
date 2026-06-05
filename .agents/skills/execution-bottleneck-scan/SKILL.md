---
name: execution-bottleneck-scan
description: Use when a product manager wants to find likely execution bottlenecks in code, architecture, operations, delivery process, integrations, data flows, performance, scalability, or team dependencies. Produces a PM-readable bottleneck map with validation steps.
---

# Find Execution Bottlenecks That Could Slow Product Delivery

## Goal

Identify bottlenecks that could limit product execution: runtime performance, scaling, data throughput, external dependencies, release process, testing, decision latency, or team coordination. Translate each bottleneck into customer impact and PM action.

## Inputs to request when missing

Ask for context that identifies the binding constraint:

- User flow, service, process, or delivery workflow to inspect.
- Target scale, latency, throughput, reliability, or launch timeline.
- Known symptoms: slow page, delayed job, incident, missed milestone, blocked team, flaky release.
- Current volume or expected growth.
- Dependencies, SLAs, vendors, data pipelines, or team handoffs.
- Whether the concern is user experience, cost, reliability, or delivery speed.

If missing, infer likely bottlenecks and mark them as hypotheses.

## Senior PM standard

Find the binding constraint. Do not list every possible bottleneck.

Look for:

- Where throughput, latency, coordination, or decision speed actually limits the product outcome.
- Whether the bottleneck is technical, organizational, data-related, vendor-related, or policy-related.
- Whether the right action is optimization, instrumentation, scope reduction, sequencing, staffing, ownership change, or expectation-setting.
- Whether improving this bottleneck changes a customer metric, launch date, cost curve, or roadmap option.
- Whether the bottleneck is near-term launch risk or future scale risk.

## Modes

Use the mode that matches the request:

- Technical bottlenecks: latency, database access, synchronous work, background jobs, external APIs, queues, caching, file processing, model calls, build time, deploy time.
- Delivery bottlenecks: unclear ownership, slow reviews, fragile tests, missing environments, dependency sequencing, overloaded teams, release approvals, ambiguous decisions.
- Mixed bottlenecks: both technical and organizational constraints affect the same product outcome.

## Workflow

1. Define the product outcome or flow that matters.
2. Inspect the relevant files, docs, metrics, tests, or plan material.
3. Trace the work path: user action, service call, data access, integration, async work, deploy or release step.
4. Look for bottleneck patterns:
   - Sequential work that could block the user.
   - Repeated data access or unbounded loops.
   - Heavy work inside request paths.
   - External dependencies without timeout, retry, fallback, or queueing evidence.
   - Shared resources with unclear limits.
   - Tests or environments that make releases slow or risky.
   - Cross-team dependencies without decision gates.
5. Classify each bottleneck by evidence level:
   - Observed: directly visible in code, metrics, tests, logs, or docs.
   - Likely: inferred from architecture or patterns.
   - Unknown: needs measurement.
6. Recommend the cheapest validation step before recommending expensive remediation.
7. Identify the one or two constraints that most deserve PM attention.

## Output format

### Executive Summary

State the highest-leverage bottleneck and why it matters.

### Bottleneck Map

Use a table:

| Bottleneck | Evidence level | Product impact | How to validate | Likely owner | Fix horizon |
| --- | --- | --- | --- | --- | --- |

Fix horizon should be one of: now, next release, next quarter, monitor.

### Flow Notes

Briefly describe where the bottleneck appears in the user or delivery flow.

### PM Actions

List concrete actions:

- Questions to ask Engineering, Data, Design, Support, or GTM.
- Metrics or logs to request.
- Scope or sequencing changes.
- Release gates or rollout constraints.

### Binding Constraint

State the most important bottleneck, why it is binding, and what changes if it is fixed.

## Quality bar

- Do not label something a bottleneck without evidence or a clear inference.
- Avoid premature optimization. Prefer measuring first when confidence is low.
- Tie every bottleneck to product impact.
- Keep the output understandable to non-engineers.
- Distinguish launch blocker, scale blocker, cost blocker, and team-throughput blocker.
