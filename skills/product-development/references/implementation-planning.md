# Implementation planning

Purpose: turn the agreed specification into an ordered plan a builder can follow, with small milestones the user can try and review. This stage plans implementation; it does not start it.

## Check the planning inputs

Reuse the scope, requirements, acceptance criteria, workflows, and technical decisions, preserving their decision authority and readiness. Identify contradictions or missing decisions that would force a builder to invent major behavior. Resolve consequential gaps within delegated judgment or raise them for user review; block only the work that depends on them. Do not treat missing market validation as an implementation blocker.

## Propose milestones and tasks

Organize delivery as vertical slices: each milestone makes a narrow user capability work end-to-end through the interaction surface, application behavior, and persistence or integrations it actually needs. Name milestones by the outcome the user can demonstrate. Deliver a thin usable slice early, then add further capabilities or deepen existing ones.

For example, a notes app might deliver “Create a note and reopen it after restarting,” then “Edit an existing note,” then “Find a note by its text.” Each slice includes its required interface, logic, storage changes, and verification. Layer-specific tasks may appear inside a slice; database, backend, and frontend are not separate release milestones. A large feature can span several slices if each delivers a usable outcome.

Include only the foundation needed by the next slice. When setup, migration, or an authorized feasibility check genuinely needs separate work, keep it bounded and name the slice it enables. A mocked interface alone does not complete a slice that requires real persistence or integration; label it as prototype or provisional work.

For each milestone, state what the user can try or review, the requirements it covers, and its completion check. Break it into tasks with a concrete deliverable, prerequisites, and verification tied to agreed behavior. Keep granularity useful to the builder; avoid both vague tasks such as “build backend” and exhaustive speculative file-level instructions.

Order work by dependencies and material risk. Put a feasibility check before work that depends on its result when the user has chosen to perform that check. Mark genuinely independent work as parallelizable when helpful, without assuming a team or delegating execution. Do not assign dates, owners, or precise effort estimates without a basis; label rough estimates and their assumptions if requested.

Include failure handling, permissions, and other agreed quality requirements in the relevant milestones. Plan proportionate verification: acceptance checks, targeted automated tests, or manual review according to the behavior and risk. Include migration, deployment, or release preparation tasks only when relevant to the intended deliverable; listing them does not authorize execution. Keep deferred features separate from the release plan.

Present the coherent plan for review. Apply shared decision authority to changes in sequence or scope, and perform the shared revision consistency check when upstream decisions change.

## Prepare the build handoff

Adapt the [build plan template](../templates/build-plan.md). A small product can use one document; a larger one can link its briefs, requirements, UX, technical design, and tasks through an index. Use existing artifacts rather than duplicating conflicting copies. The builder should be able to find the current decisions without the conversation history.

The build plan is complete when every included capability has delivery work, dependencies have a feasible order, completion checks demonstrate each slice end-to-end against requirements, and exclusions have stayed outside the release. Perform the shared consistency check across current artifacts. State which work is ready, provisional, or blocked, the prerequisites for each unresolved part, and the first actionable milestone. If all work is conditional, identify the first decision needed instead of inventing a ready milestone.

For a full planning handoff, move to [naming](naming.md) if the user has neither chosen nor deferred a name. A request limited to delivery planning needs no new naming exercise. Finalize references and the project label after the choice. Deliver the planning artifacts and next action; do not create the product repository, provision infrastructure, or begin implementation under a planning-only request.
