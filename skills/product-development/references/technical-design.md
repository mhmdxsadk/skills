# Technical design

Purpose: define how the product's parts will deliver the scoped behavior, with enough direction for implementation planning. Choose technology in service of the requirements and the user's constraints.

## Establish what drives the choices

Reuse the requirements, workflows, design brief, existing codebase, and previous decisions. Identify constraints that affect architecture: target platforms, existing technology preferences and experience, budget, maintenance capacity, sensitive data, offline behavior, integrations, and consequential quality requirements. Ask only about unresolved constraints that could change the recommendation.

Do not infer large-scale requirements from an ambition to become a SaaS product. Separate current needs from possible future growth. Keep dependent technical choices provisional when important product behavior remains open; continue decisions that can be made independently.

## Recommend a coherent approach

Propose a stack and architecture with reasons tied to the agreed behavior. Compare a few credible alternatives only where the tradeoff matters. Explain the effects on development effort, user experience, operating cost, maintenance, and ability to change direction in terms the user can understand. Avoid a catalog of frameworks or asking the user to choose every library.

Start from supplied preferences and existing infrastructure. If a preferred technology conflicts with a requirement, explain the concrete mismatch and offer a workable alternative or requirement tradeoff. Apply the shared decision-authority and challenge rules to the selection.

Favor the simplest design that meets the actual needs. Introduce separate services, queues, caches, or other infrastructure when their role is justified by a requirement or failure mode. Describe future expansion points only where today's choice would make a likely change expensive; do not put speculative features into the release.

Verify decision-critical claims about current platform capabilities, compatibility, pricing, limits, or service terms using authoritative sources when research is available. Date material findings and distinguish documented support from tested behavior and assumptions. If verification is unavailable, keep the claim provisional. For cost estimates, state workload assumptions and major cost drivers rather than presenting unsupported precision.

## Define how the parts connect

Use a short explanation or diagram to show the components, their responsibilities, where they run, and the flow of data through a key user workflow. Include the following only to the depth the product requires:

- **Data:** Core entities, relationships, ownership, storage, and relevant retention or deletion behavior. Identify consequential consistency or synchronization needs without prematurely specifying every column.
- **Identity and access:** Whether accounts are needed, who can access which data or actions, and where permissions are enforced. Do not add accounts by default.
- **Integrations and processing:** External dependencies, inputs and outputs, authentication boundaries, and relevant processing states. Define failure, retry, duplicate-handling, or fallback behavior when it affects the agreed experience.
- **Operation:** Hosting or distribution approach, configuration and secrets boundaries, and proportionate recovery and diagnostic needs. Include backup or migration decisions where losing data or changing an existing system makes them consequential.

Connect these decisions to requirements and UX states. If technical constraints change visible behavior, apply the shared decision-authority rule and update affected requirements before presenting the design as consistent. Do not treat selection of a service as proof that an integration works or that its use is permitted.

## Resolve enough to plan delivery

For consequential uncertainty, apply the shared research and readiness rules. Planning a check does not authorize implementing a prototype or provisioning services. A deferred check must leave its affected choices and work visibly conditional.

Adapt the [technical design template](../templates/technical-design.md). The defined work is ready for delivery planning when each core workflow has a plausible technical path, important data and access boundaries are specified, and dependencies have a chosen approach or an explicit unresolved prerequisite. Record the authority for selected choices and the downstream effects of uncertainty.

Proceed with delivery planning for sufficiently defined work, applying the shared readiness rule to the remainder.
