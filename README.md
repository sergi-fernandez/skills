# Product Skills I Use With Codex

These are my personal product-management skills and recommendations for working with Codex and other AI agents.

I use them as reusable workflows for senior PM work: understanding a codebase, researching a market, critiquing a frontend, prioritizing features, pressure-testing a roadmap, building a business case, or turning messy evidence into a decision.

They are intentionally decision-grade. Each skill should ask for the few inputs that materially change the answer, challenge weak assumptions, identify tradeoffs, and end with specific actions or decision gates.

## What To Copy

The reusable skills live here:

```text
.agents/skills/<skill-name>/SKILL.md
```

Each skill is a folder with a `SKILL.md` file. The `agents/openai.yaml` files add Codex UI metadata and are useful to keep with the skills.

The `chatgpt/` folder contains optional instructions for people who want to adapt the same workflows to ChatGPT Projects or a Custom GPT.

## Install Permanently In Codex

Use this if you want the skills available in Codex across your projects.

```bash
mkdir -p "$HOME/.agents/skills"
cp -R .agents/skills/* "$HOME/.agents/skills/"
```

After that, invoke a skill directly in Codex with `$skill-name`:

```text
$research-competitive-landscape-and-positioning I am building a SaaS product that supports finance close processes. Identify the segment, competitors, positioning, pricing, and what I may be missing.
```

## Add Skills To A Specific Repo

Use this if you want the skills to travel with one repository and be available to everyone working in that repo.

```bash
mkdir -p /path/to/your-repo/.agents/skills
cp -R .agents/skills/* /path/to/your-repo/.agents/skills/
```

You can also copy only the skills you want:

```bash
cp -R .agents/skills/research-competitive-landscape-and-positioning /path/to/your-repo/.agents/skills/
```

## Use A Skill Ad Hoc

If you do not want to install anything, copy the relevant `SKILL.md` into your prompt or attach it as a file and ask the agent to follow it.

Example:

```text
Use the attached SKILL.md as your workflow. I am building a finance close SaaS product. Research the competitive landscape and tell me the segment, competitors, pricing, gaps, and strategic wedge.
```

This works in most AI tools, but it is less convenient than installing the skill because the agent will not automatically discover it.

## Adapt For Claude

Claude Code also uses `SKILL.md` folders. To install these as personal Claude skills:

```bash
mkdir -p "$HOME/.claude/skills"
cp -R .agents/skills/* "$HOME/.claude/skills/"
```

To add them to a single Claude Code project:

```bash
mkdir -p /path/to/your-repo/.claude/skills
cp -R .agents/skills/* /path/to/your-repo/.claude/skills/
```

In Claude Code, invoke them with `/skill-name`, for example:

```text
/research-competitive-landscape-and-positioning I am building a SaaS product that supports finance close processes.
```

For Claude.ai, zip the individual skill folder and upload it as a custom skill. Keep the folder structure intact so `SKILL.md` remains at the root of that skill folder.

The Codex-specific `agents/openai.yaml` metadata is harmless to keep, but Claude does not need it.

## Adapt For ChatGPT

ChatGPT does not discover local `SKILL.md` folders. Use:

- `chatgpt/pm-skills-custom-gpt-instructions.md` for a Custom GPT.
- `chatgpt/pm-project-instructions.md` for a ChatGPT Project.
- `chatgpt/conversation-starters.md` for example prompts.

You can also upload selected `SKILL.md` files as Knowledge, but put the core behavior in Instructions. Knowledge files are reference material; instructions are what shape the GPT's behavior.

## Skill Catalog

| Skill | Command | Use it for |
| --- | --- | --- |
| Research a Competitive Landscape and Product Positioning | `research-competitive-landscape-and-positioning` | Find competitors, alternatives, market segment, positioning, pricing, gaps, and differentiation using online research. |
| Map a Codebase for Product Understanding | `codebase-map-for-product` | Understand repo structure, product surfaces, user flows, data flows, and change hotspots. |
| Assess Codebase Quality for Product Planning | `codebase-quality-readout` | Get a PM-readable quality readout covering maintainability, tests, release safety, architecture, dependencies, and product flexibility. |
| Review Frontend Product Experience and Design | `review-frontend-product-experience-and-design` | Critique UI quality, workflows, responsiveness, visual consistency, accessibility basics, and missing product states. |
| Audit Frontend Performance, Responsiveness, and Loading States | `audit-frontend-performance-responsiveness-and-loading-states` | Check perceived speed, layout stability, loading states, skeletons, slow network behavior, bundle risk, and technical UX quality. |
| Identify Product Risks in a Feature, Plan, or Code Area | `product-risk-radar` | Rank product, rollout, data, dependency, operational, compliance, and technical risks. |
| Find Execution Bottlenecks That Could Slow Product Delivery | `execution-bottleneck-scan` | Identify runtime, scaling, dependency, process, and team bottlenecks with validation steps. |
| Review Strategic Positioning for a Product or Feature | `strategy-positioning-review` | Pressure-test ICP, alternatives, differentiation, proof, urgency, category, and GTM fit. |
| Prioritize Feature and Roadmap Options | `feature-prioritization-sparring` | Choose between product bets using the right framework, scoring, sensitivity, and rationale. |
| Build or Challenge a Product Business Case | `build-or-challenge-product-business-case` | Draft or critique business cases, identify financial levers, missing data, scenarios, sensitivities, and business-plan narrative. |
| Critique a Roadmap, Launch Plan, or Product Plan | `roadmap-plan-critique` | Pressure-test outcomes, sequencing, dependencies, capacity, owners, rollout, and decision gates. |
| Write a Product Decision and Requirements Brief | `write-product-decision-and-requirements-brief` | Create a clear decision memo, requirements brief, feature brief, or PRD-style alignment artifact. |
| Synthesize Customer and Product Evidence Into Decisions | `discovery-evidence-synthesis` | Turn interviews, tickets, analytics, feedback, sales notes, and research into themes, confidence levels, and decisions. |

## Example Prompts

```text
$research-competitive-landscape-and-positioning I am building a workflow SaaS for finance teams that helps with month-end close. Find the exact segment, competitors, pricing, positioning, and where we may be differentiated.
```

```text
$review-frontend-product-experience-and-design Review this frontend repo as a PM. Tell me whether the UI feels complete, responsive, and trustworthy enough for beta users.
```

```text
$audit-frontend-performance-responsiveness-and-loading-states Audit the frontend for mobile responsiveness, skeleton loading, slow network behavior, and product-impacting performance issues.
```

```text
$build-or-challenge-product-business-case I have 2,000 eligible customers and think 8 percent may buy this add-on. Help me build the business case, identify missing data, and draft the plan.
```

```text
$feature-prioritization-sparring Help me choose between improving onboarding, adding SSO, building exports, and adding a dashboard.
```

## Output Style

The skills are opinionated:

- Lead with the recommendation.
- Separate evidence from inference.
- State assumptions and confidence.
- Ask for high-leverage missing inputs, not background context.
- Identify tradeoffs, thresholds, reversibility, and what would change the decision.
- Translate code findings into product impact.
- Prioritize actions, owners, risks, and decision gates.
- Use web research for competitive and market work when current information matters.
- Avoid generic frameworks unless they materially improve the decision.

## Notes

These skills are decision-support tools. They are not a substitute for formal legal, financial, security, compliance, or accounting review.
