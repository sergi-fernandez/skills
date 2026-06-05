---
name: review-frontend-product-experience-and-design
description: Use when a product manager wants to critique a frontend repo, web app, prototype, or product UI for product experience, interaction design, responsive behavior, information architecture, visual consistency, accessibility basics, empty states, error states, loading states, and workflow clarity. Produces PM-readable design findings with evidence and priority.
---

# Review Frontend Product Experience and Design

## Goal

Review a frontend product experience from the perspective of product quality, usability, clarity, and design execution. The output should help a PM understand whether the UI is credible, responsive, complete, and ready for users.

## Inputs to request when missing

Ask for context that changes the product critique:

- Target user, buyer, workflow, and product stage.
- Primary route, task, or funnel to review.
- Design standard: internal tool, customer-facing SaaS, enterprise workflow, consumer app, marketplace, or admin console.
- Target devices, accessibility expectations, and supported browsers.
- Known issues, launch deadline, or metric the UI must improve.

If missing, review the visible primary workflow and state assumptions.

## Senior PM standard

Critique the UI as a product system, not as visual taste.

Look for:

- Task clarity: whether users can understand what to do, why it matters, and what happens next.
- Cognitive load: whether layout, copy, controls, and data density match the workflow.
- Workflow completeness: whether the product handles real-life states, not only the happy path.
- Trust and accountability: source of data, status, permissions, destructive actions, auditability, and recovery.
- Design-system maturity: consistency, component reuse, interaction patterns, and scalable information architecture.
- Conversion or adoption friction: where UX choices could hurt activation, retention, or enterprise confidence.

## Inputs

Use whatever is available:

- A frontend repository.
- A running local app.
- Screenshots, video, Figma notes, or product requirements.
- A URL the user is authorized to inspect.

When a repo is available, inspect code and run the app if practical. When a live surface is available, use browser testing and screenshots where possible.

## Review lenses

Evaluate:

- First impression: what product, workflow, and primary action are immediately clear.
- Layout and responsiveness: desktop, tablet, mobile, overflow, wrapping, density, navigation.
- Interaction design: forms, filters, menus, modals, tables, editing, destructive actions, confirmations.
- State coverage: loading, skeletons, empty states, error states, disabled states, optimistic updates, offline or slow network behavior.
- Visual consistency: spacing, typography, color, icon use, hierarchy, reusable components.
- Accessibility basics: keyboard path, focus states, labels, contrast, semantic controls, reduced motion where relevant.
- Product completeness: onboarding, help, permissions, upsell, lifecycle states, edge cases.
- Trust: clarity of data, source, last updated time, privacy-sensitive flows, auditability where relevant.

## Workflow

1. Identify the product workflow and primary user goal.
2. Inspect relevant routes, pages, components, styles, and design-system usage.
3. Run or view the UI when possible. Check at least desktop and mobile widths.
4. Note evidence for each finding: file, route, screenshot observation, component, or behavior.
5. Prioritize issues by product impact:
   - P0: blocks task completion or creates serious trust risk.
   - P1: likely hurts conversion, comprehension, accessibility, or adoption.
   - P2: polish or consistency issue worth fixing before broader rollout.
   - P3: nice-to-have refinement.
6. Recommend concrete product and design fixes.
7. Distinguish design debt, product ambiguity, and implementation defects.

## Output format

### Verdict

State whether the frontend feels ready, usable with fixes, risky, or too incomplete to judge.

### Top Findings

Use a table:

| Priority | Finding | Evidence | Product impact | Recommendation |
| --- | --- | --- | --- | --- |

### Workflow Review

Summarize how the main user journey performs from start to finish.

### Responsive and State Coverage

Call out mobile, tablet, loading, empty, error, and disabled-state gaps.

### Design Quality Notes

Highlight visual hierarchy, consistency, density, information architecture, and trust issues.

### Product Judgment

State whether the issue is mainly product definition, UX design, visual system, content, accessibility, or implementation.

### Next Fixes

List the highest-leverage fixes in order.

## Quality bar

- Do not give generic design advice without tying it to a screen, route, or workflow.
- Do not require aesthetic perfection for internal tools; judge fit for product context.
- Include responsive and state coverage even if the UI looks good at one viewport.
- Separate user-blocking issues from polish.
- Tie recommendations to the target user and product stage.
