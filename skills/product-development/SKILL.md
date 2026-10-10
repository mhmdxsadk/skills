---
name: product-development
description: Guide a digital product idea or problem toward an implementation-ready specification through discovery, critical evaluation, scoping, requirements, UX definition, technical design, and implementation planning. Use when planning a new product, feature, prototype, or internal tool before implementation.
---

# Product Development

**Development draft:** all workflow stages have guidance and adaptable output templates. The complete workflow still needs behavioral evaluation and installation checks before release.

Help the user decide what is worth building and define it well enough to hand to a builder. End at the specification and implementation plan. Treat implementation, deployment, and external outreach as separate actions requiring their own task scope.

## Working approach

- Reuse existing context and artifacts. Start at the earliest unresolved consequential decision rather than forcing a restart.
- Keep the current assignment in view. When using an example to review or test a workflow, resolve the question being tested and return to the review; do not silently turn the example into a full product-planning engagement.
- Distinguish supplied claims, direct evidence, hypotheses, and decisions. Never label an idea validated merely because its documentation is complete.
- Summarize the relevant understanding and propose a coherent next step before asking for input. Ask small batches of questions that change the next decision; invite edits to a concrete proposal instead of seeking approval for every minor detail. Keep unanswered proposals tentative.
- Match depth to uncertainty and the cost of error. A personal tool may need one concise document; a consequential product may need deeper discovery and separate artifacts.
- Challenge the user's ideas when there is a meaningful reason, explain the concern, and work through alternatives with them toward a sound decision. Do not argue for its own sake or invent objections. Treat firm requirements as constraints and distinguish them from preferences. Recommend stopping or changing direction when evidence warrants it; the user owns that choice.
- If the user understands a concern and chooses to proceed or defer it, record the decision and material remaining risk, then move on. Revisit it when new evidence or a dependent decision makes it relevant, rather than repeating the same warning.
- Treat validation as optional. Reuse evidence the user already has, offer further validation when they want it or when it could change a consequential decision, and respect a choice to proceed without it. Keep material uncertainty visible without making validation a gate for planning.
- Bound research to a material question and the next decision. When tools and task scope permit, investigate until there is enough evidence for that decision or a clear limitation; report what was and was not established, then return to planning. Cite sources and separate observations from inference. When research is unavailable, record the gap and a possible next check.
- Use available file tools for useful persistent artifacts, otherwise work in chat. Do not require a specific model, connector, cloud provider, or proprietary format.

## Intake and problem definition

Read [references/intake-and-problem-definition.md](references/intake-and-problem-definition.md) when entering or revisiting these stages. Adapt [templates/problem-brief.md](templates/problem-brief.md) for the resulting brief; omit irrelevant sections rather than filling them with guesses.

Produce a grounded problem brief and a recommendation for the next investment. Pause for missing information only when it is necessary to make that decision; continue independent work where possible.

## Optional discovery and validation

Read [references/discovery-and-validation.md](references/discovery-and-validation.md) when reviewing evidence or deciding whether further validation would help. Reuse existing findings, propose focused checks only when useful, and respect a choice to skip. Adapt [templates/evidence-and-validation.md](templates/evidence-and-validation.md) when an evidence record is warranted.

## Product definition and scope

Read [references/product-definition-and-scope.md](references/product-definition-and-scope.md) when choosing a product approach, deciding whether to plan a prototype, or defining/revising MVP scope. Compare plausible approaches, recommend a scope, and invite the user's changes. Adapt [templates/product-and-scope-brief.md](templates/product-and-scope-brief.md) to capture the result or extend existing planning material.

## Requirements and UX

Read [references/requirements-and-ux.md](references/requirements-and-ux.md) when turning scoped capabilities into observable behavior, acceptance criteria, workflows, and a design brief. Propose a coherent draft and refine it with the user. Adapt [templates/requirements.md](templates/requirements.md) and [templates/design-brief.md](templates/design-brief.md), combining them for small projects. Keep proposed choices distinct from agreed requirements and make the design brief usable by a designer or design tool without the conversation history.

## Technical design

Read [references/technical-design.md](references/technical-design.md) when choosing the stack and defining how the product's parts connect. Recommend an approach grounded in the requirements and existing constraints, compare material alternatives, and refine it with the user. Adapt [templates/technical-design.md](templates/technical-design.md) to capture decisions and uncertainties before implementation planning.

## Implementation planning and naming

Read [references/implementation-planning.md](references/implementation-planning.md) when translating the specification into ordered, reviewable milestones. Adapt [templates/build-plan.md](templates/build-plan.md) to capture deliverables, dependencies, and completion checks. Read [references/naming.md](references/naming.md) for the final pre-build name choice; reuse a name the user already likes.

## Workflow sequence and completion

After problem definition, move through optional discovery/validation, product definition, an optional prototype, MVP scope, requirements, UX, technical design, implementation planning, and finally naming as needed. Revisit earlier decisions when new findings invalidate them. Make naming the last planning step before implementation so the user can choose a name they like for their project directory or repository. Treat it as changeable; do not begin implementation during this step.

At meaningful boundaries, recommend PROCEED, VALIDATE, REVISE, PARK, or KILL with evidence, residual uncertainty and the next action. Do not treat missing evidence as disproof. If the user proceeds with uncertainty, preserve it explicitly. When relevant, distinguish readiness to build from confidence in the underlying evidence; do not require validation before continuing.

The final planning handoff connects user outcomes to scoped requirements, acceptance criteria, UX behavior, technical choices, and delivery work. Identify the current artifacts, agreed name or remaining naming decision, first actionable milestone, and material unresolved dependencies. Do not call major unresolved behavior implementation-ready, and do not confuse readiness to build with validated demand.
