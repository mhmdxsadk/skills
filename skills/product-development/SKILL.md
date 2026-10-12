---
name: product-development
disable-model-invocation: true
description: Develop a raw digital-product idea, problem, or existing planning material into an implementation-ready specification and implementation plan. Ends before implementation.
---

# Product Development

Help the user decide what is worth building and define it well enough to hand to a builder. For a full engagement, deliver the specification and implementation plan. For a narrower request, finish that deliverable and stop there. Implementation, deployment, and external outreach require their own task scope.

## Select the next decision

Reuse supplied context, artifacts, and decisions. Identify the requested deliverable and the earliest unresolved consequential decision affecting it. Read only the relevant guidance below. Existing material satisfies a stage when it meets that stage's completion criteria; skip inapplicable work. The references are routes, not a checklist to complete in order.

Summarize the relevant understanding and propose a coherent next step. Ask a small batch of questions only when the answers change that decision. Continue useful independent work while marking dependent work provisional. Keep speculative downstream detail to the minimum needed to explain a choice; if a missing decision determines the product itself, resolve it before drafting a full plan. When reviewing or testing a workflow with an example, resolve the behavior under examination and return to the review.

Match depth to uncertainty and the cost of error. A personal tool may need one concise document; a consequential product may need separate artifacts. Extend current artifacts rather than creating competing copies. Use files when useful and available, otherwise chat; keep outputs portable. Templates are optional output structures: replace their prompts with content and omit irrelevant sections. An empty field does not require an answer or another investigation.

## Decisions and uncertainty

- Preserve supplied decisions and distinguish firm constraints from preferences. Within judgment the user has delegated, select reasoned defaults and record them as agent-selected decisions. Material choices outside that delegation remain proposals until the user decides; silence is not acceptance. Bundle those choices for review rather than seeking approval for routine details.
- Record decision status separately from work readiness. For consequential choices, record whether they were supplied, user-agreed, agent-selected within delegation, proposed, or unresolved. Group choices sharing the same authority instead of labeling every sentence. Dependent work can be ready, provisional pending a choice or finding, or blocked with a named prerequisite. Accepted risk does not establish a missing fact.
- Challenge a choice when there is a concrete mismatch, consequence, or contrary evidence. Explain alternatives and the tradeoff. After an informed choice, record material residual risk and apply the decision downstream. Reopen it only when new evidence or a newly discovered consequence changes the earlier tradeoff; encountering a known dependency is not a reason to ask again. The user owns investment and stop decisions.
- Distinguish supplied claims, observations, hypotheses, and decisions. Documentation completeness is not validation. Validation is optional: reuse existing evidence and offer a check when wanted or when its result could change a consequential decision. Respect a choice to defer it while preserving its downstream effects.
- Before research, identify the decision, the question that could change it, and the evidence or limitation that will end the investigation. Within available tools and task scope, stop at that condition, report findings and limits with sources, and return to the decision. Record adjacent uncertainties unless they change that decision. Separate inference from observation; unavailable research leaves the claim provisional.

At an investment or direction decision, recommend PROCEED (take the next step), VALIDATE (offer a focused check), REVISE (change the approach or scope), PARK (defer), or KILL (stop this approach), with reasons and the next action. Missing evidence alone does not justify rejection. Use these labels when a decision warrants them, not after every section.

## Guidance by unresolved decision

- **Problem:** When the affected user, task, outcome, or constraints are unclear, read [intake and problem definition](references/intake-and-problem-definition.md).
- **Evidence:** When interpreting findings or considering a useful check, read [discovery and validation](references/discovery-and-validation.md). Evidence review can occur at any stage.
- **Approach and scope:** When choosing an approach, planning a learning prototype, or defining a release boundary, read [product definition and scope](references/product-definition-and-scope.md).
- **Behavior and interaction:** When scoped capabilities lack observable behavior, acceptance checks, workflows, or a portable design brief, read [requirements and UX](references/requirements-and-ux.md).
- **Technical path:** When deciding how components, data, access, and integrations deliver the behavior, read [technical design](references/technical-design.md).
- **Delivery:** When the defined work needs vertical-slice milestones and end-to-end verification, read [implementation planning](references/implementation-planning.md).
- **Name:** At the final planning handoff, read [naming](references/naming.md) if no name has been chosen. Reuse existing choices; naming may be deferred.

Each reference links its output templates and defines completion for its work. Meeting a criterion permits progression within the request; it does not require opening every later reference.

## Revisions and handoff

When a consequential decision changes, inspect affected scope, requirements, workflows, technical choices, and delivery work. Update each affected artifact or mark it stale before presenting the package as consistent. Revisit only the affected decisions. Use links or identifiers where they make dependencies easier to maintain.

The final handoff connects outcomes to scoped requirements, acceptance criteria, UX behavior, technical choices, and delivery work. Check capability coverage, dependency order, exclusions, and consistency of current artifacts. Identify the chosen name or deferred naming decision, the first actionable milestone, and unresolved prerequisites.

Report readiness separately from evidence confidence. Unproven demand can remain an accepted assumption for an otherwise defined build. An unverified integration may support a conditional plan with a chosen fallback; an unknown integration contract without a fallback leaves dependent work provisional or blocked. Declining a check changes whether to investigate, not whether its missing fact is known. Use a conditional handoff when the user defers a dependency or a finding cannot be obtained within scope, after completing independent planning. Resolve answerable gaps within the current request before handing off. Unresolved major behavior is not implementation-ready.
