---
name: audit-frontend-performance-responsiveness-and-loading-states
description: Use when a product manager wants a frontend repo or web app audited for performance, responsiveness, loading states, skeletons, perceived speed, bundle or rendering issues, network behavior, accessibility basics, and product-impacting technical UX quality. Produces prioritized findings with validation steps.
---

# Audit Frontend Performance, Responsiveness, and Loading States

## Goal

Assess whether a frontend is likely to feel fast, responsive, stable, and trustworthy for users. Focus on product-impacting technical UX quality rather than deep implementation refactoring.

## Inputs to request when missing

Ask for the inputs that change performance judgment:

- Critical routes, workflows, and conversion or activation points.
- Target users, devices, browsers, regions, and network conditions.
- Current performance complaints, analytics, Core Web Vitals, or support evidence.
- Product stage: prototype, beta, GA, enterprise procurement, mobile-heavy, internal tool.
- Performance budget or business threshold, if one exists.

If missing, test representative routes and state the assumptions.

## Senior PM standard

Translate frontend performance into product risk and prioritization.

Look for:

- Perceived performance, not only measured speed.
- Whether loading behavior preserves user trust and orientation.
- Whether slow paths affect acquisition, activation, conversion, retention, support cost, or enterprise credibility.
- Whether the fix is product scope, UX state design, instrumentation, API work, rendering optimization, or asset hygiene.
- Whether missing field metrics make the team blind to real user experience.

## Inputs

Use what is available:

- Frontend codebase.
- Running local app.
- Production or staging URL the user is authorized to inspect.
- Screenshots, traces, Lighthouse output, Core Web Vitals, analytics, or bug reports.

When practical, run the app and inspect behavior at realistic viewports and network conditions. Use browser tooling or available scripts when useful.

## Audit lenses

Evaluate:

- Responsiveness: layout stability, mobile fit, horizontal scroll, text overflow, touch targets, viewport-specific navigation.
- Loading experience: skeletons, spinners, progressive loading, optimistic states, route transitions, slow network behavior.
- Rendering performance: expensive client rendering, large lists, unnecessary re-renders, blocking scripts, hydration problems.
- Network performance: waterfall shape, duplicate requests, slow APIs, caching, pagination, prefetching, request cancellation.
- Bundle and asset weight: large dependencies, unoptimized images, font loading, unused code, route splitting.
- Core Web Vitals signals: LCP, INP, CLS where measurable.
- Failure states: timeout, empty, partial data, error recovery, offline or retry behavior.
- Accessibility basics that affect performance perception: focus, keyboard flow, reduced motion, visible feedback.

## Workflow

1. Identify the critical user paths and pages.
2. Inspect build scripts, routing, data fetching, component patterns, and styling approach.
3. Run available checks when practical: build, lint, tests, Lighthouse, browser screenshots, or local profiling.
4. Test at minimum:
   - Desktop width.
   - Mobile width.
   - Slow or loading state when possible.
5. Classify findings:
   - Observed: reproduced in app, screenshot, trace, command output, or code.
   - Likely: inferred from code structure or dependency pattern.
   - Needs measurement: plausible but unverified.
6. Recommend fixes by product impact and implementation effort.
7. Call out where measurement is required before prioritizing engineering work.

## Output format

### Verdict

State whether the frontend is likely fast and resilient, acceptable with gaps, or risky for users.

### Critical Findings

Use a table:

| Priority | Issue | Evidence level | Product impact | Validation | Recommendation |
| --- | --- | --- | --- | --- | --- |

### Responsiveness Review

Summarize viewport and layout issues.

### Loading and Failure-State Review

Summarize skeleton/loading, empty, error, timeout, retry, and partial-data coverage.

### Performance Risks

List bundle, rendering, network, and asset risks.

### Product Impact and Priority

State which issues matter for activation, conversion, retention, trust, support load, enterprise readiness, or mobile adoption.

### Recommended Checks

List the exact checks the user or team should run next if evidence is incomplete.

## Quality bar

- Do not claim performance problems from code alone when measurement is needed.
- Do not bury product-impacting loading or responsiveness issues under tooling detail.
- Prefer concrete validation steps over vague optimization advice.
- Keep the result useful for a PM planning quality work with Engineering and Design.
- Name the metric, trace, screenshot, or user behavior that would prove the issue.
