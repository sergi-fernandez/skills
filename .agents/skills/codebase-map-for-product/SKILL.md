---
name: codebase-map-for-product
description: Use when a product manager needs a PM-readable map of a repository, feature area, or unfamiliar codebase, including key modules, request or data flows, product surfaces, ownership clues, and likely places where product changes land. Do not use for line-by-line code review.
---

# Map a Codebase for Product Understanding

## Goal

Create a product-manager-readable map of a codebase or feature area. The output should help a PM understand what exists, where product behavior lives, where changes are likely to land, and which areas carry product risk.

## Inputs to request when missing

Ask for context that changes the map:

- Product area, feature, route, user flow, service, or business question.
- Planned decision: scope feature, assess risk, onboard to repo, estimate change area, or challenge architecture.
- Target user segment, workflow, permission model, pricing/package implication, or data object if relevant.
- Whether the user wants a full repo map or a focused slice.

If no scope is provided, start with a repo-level map and identify the highest-value follow-up slices.

## Senior PM standard

The map should reveal product leverage and constraints, not just file structure.

Look for:

- Product-policy axes: roles, permissions, eligibility, pricing, packaging, experiments, localization, compliance, lifecycle states.
- Coupling: places where a small product change touches many modules, services, data models, or teams.
- Extension points: where the system appears designed for new workflows, integrations, plans, or user segments.
- Hard-to-change areas: legacy boundaries, shared domain models, migrations, tightly coupled UI/API contracts, hidden side effects.
- Evidence gaps: areas where code does not reveal operational, data, support, or rollout realities.

## Workflow

1. Establish scope. If the user named a repo, feature, route, screen, service, or file, use that as the boundary. If scope is broad, inspect the repository at a high level first.
2. Inspect orientation files before source files: `README`, `AGENTS.md`, docs, package manifests, route maps, API specs, deployment config, tests, and obvious app entry points.
3. Build a product vocabulary. Translate module names, services, screens, routes, jobs, and data models into product concepts.
4. Trace one or more representative flows from user action or API entry point to persistence, background work, integrations, and user-visible output.
5. Identify change hotspots: files or modules where new product behavior, permissions, pricing, onboarding, analytics, notifications, or workflow changes are likely to happen.
6. Call out uncertainty. Separate evidence from inference and list what could not be verified from the available files.

## Output format

Use this structure unless the user asks for another format:

### Product Readout

- What this codebase or area appears to do.
- The main users, jobs, or product surfaces it supports.
- The 3-5 concepts a PM needs to understand first.

### System Map

Provide a concise map of:

- User-facing surfaces.
- Backend services, jobs, or APIs.
- Important data models or storage.
- External dependencies and integrations.
- Tests, docs, and operational clues.

### Flow Trace

Describe the most important flow in plain language. Include file references when available.

### Change Hotspots

List the likely files, modules, or teams involved in common PM requests:

- Add or change user-facing behavior.
- Change pricing, packaging, permissions, or eligibility.
- Add analytics, reporting, notification, or lifecycle behavior.
- Adjust rollout, experiments, or configuration.

### Product Leverage and Constraints

State which product changes appear easy, which appear expensive, and which need deeper engineering validation.

### Product Risks and Questions

List the practical risks, missing context, and questions to ask Engineering or Design.

## Quality bar

- Use file references for concrete claims.
- Avoid pretending uncertain architecture is certain.
- Do not recommend rewrites unless the user asks.
- Do not bury the PM answer under implementation detail.
- Prefer a small, accurate map over an exhaustive file inventory.
- Focus on product change implications, not repository tourism.
