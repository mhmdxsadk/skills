# Implementation planning

Purpose: turn the agreed specification into an ordered plan a builder can follow, with small milestones the user can try and review. This stage plans implementation; it does not start it.

## Check the planning inputs

Reuse the agreed scope, requirements, acceptance criteria, workflows, and technical decisions. Identify contradictions or missing decisions that would force a builder to invent major behavior. Resolve consequential gaps with the user or explicitly block only the work that depends on them. Do not treat missing market validation as an implementation blocker.

## Propose milestones and tasks

Group work into small milestones that deliver observable progress toward the core user outcome. Prefer a thin usable workflow early, then deepen it, rather than completing every database, backend, and interface task before anything can be tried. Include foundational work when necessary and explain what it enables.

For each milestone, state what the user can try or review, the requirements it covers, and its completion check. Break it into tasks with a concrete deliverable, prerequisites, and verification tied to agreed behavior. Keep granularity useful to the builder; avoid both vague tasks such as “build backend” and exhaustive speculative file-level instructions.

Order work by dependencies and material risk. Put a feasibility check before work that depends on its result when the user has chosen to perform that check. Mark genuinely independent work as parallelizable when helpful, without assuming a team or delegating execution. Do not assign dates, owners, or precise effort estimates without a basis; label rough estimates and their assumptions if requested.

Include failure handling, permissions, and other agreed quality requirements in the relevant milestones. Plan proportionate verification: acceptance checks, targeted automated tests, or manual review according to the behavior and risk. Include migration, deployment, or release preparation tasks only when relevant to the intended deliverable; listing them does not authorize execution. Keep deferred features separate from the release plan.

Present the coherent plan for review and invite changes to sequence or scope. Explain the consequences of requested additions and update upstream decisions as needed. Preserve agreed choices and label proposals clearly rather than asking for approval on every routine task.

## Prepare the build handoff

Adapt the [build plan template](../templates/build-plan.md). A small product can use one document; a larger one can link its briefs, requirements, UX, technical design, and tasks through an index. Use existing artifacts rather than duplicating conflicting copies. The builder should be able to find the current decisions without the conversation history.

Check that every included capability is covered by delivery work, dependencies have a feasible order, and completion checks match the requirements. Verify that excluded features have not silently entered the plan. State which work is ready, which is provisional or blocked, and the first actionable milestone.

Then move to [naming](naming.md) if the user has not already chosen a name they like. Finalize references and the project label after the choice. Deliver the planning artifacts and next action; do not create the product repository, provision infrastructure, or begin implementation under a planning-only request.
