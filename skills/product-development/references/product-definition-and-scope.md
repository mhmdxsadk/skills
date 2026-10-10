# Product definition and scope

Purpose: turn an understood problem into a chosen product approach and a collaboratively agreed first-release scope. These instructions cover product definition, optional prototype planning, and MVP scoping. They do not authorize building a prototype or product.

## Start from existing work

Reuse the problem brief, supplied evidence, constraints, and decisions. If there is already a product concept or scope, work on its consequential gaps instead of restarting. Summarize the relevant understanding before proposing an approach or asking the next consequential questions. Do not keep collecting preferences once there is enough context to offer a useful proposal.

Validation is optional. Use existing evidence, and offer additional validation when it could affect the decision. If the user chooses to proceed without it, preserve important assumptions without blocking planning. A problem experienced by the builder supports their own need; broader demand remains a separate question.

Use a descriptive project label during planning if there is no name yet. Choosing a name comes at the end of planning, before implementation.

## Compare product approaches

Compare a few plausible ways to address the problem. Explain how each would help the intended users, its fit with constraints, its main limitations, and consequential uncertainty. Compare only dimensions that could change the decision; avoid unsupported scores, cost estimates, or claims about demand.

Include a non-software option only when it is viable and easier than developing software. Do not pad the comparison with unsuitable alternatives. Preserve firm requirements; explore alternatives to preferences where useful. For an existing, agreed approach, revisit it only when a meaningful concern or new finding warrants doing so.

Recommend the strongest fit and explain why. Discuss objections and alternatives with the user, then capture their chosen approach separately from your recommendation if they differ. Once the user understands a concern and chooses to proceed, note the remaining risk and help them move forward.

Summarize the resulting product concept: who it serves, what outcome it enables, and how the approach helps. Keep the product's possible future ambition distinct from the first release. A personal tool that may become SaaS does not automatically require the whole future SaaS scope now.

## Decide whether a prototype helps

A prototype comes before an MVP when it can resolve a useful question about the approach, interaction, or feasibility. Otherwise recommend proceeding directly to MVP planning. Do not substitute a prototype for a usable MVP without explaining the different purpose.

If a prototype would help, propose:

- The question it should answer and the decision its result would inform.
- The smallest useful representation or experiment, and what it deliberately leaves out.
- How the user could assess the result, including any agreed success signals.
- Which MVP decisions depend on that result.

Keep this as a prototype plan. Building or running it requires a separate implementation or evaluation task. If a feasibility check is within the user's request, define the question, smallest useful check, and stopping point before starting. Report its result and limits, then return to the planning decision. A successful sample establishes only what was tested; it does not establish general reliability or permission to use an integration in production.

If results are needed before deciding MVP scope, mark that scope as provisional rather than inventing findings. Continue planning independent parts where possible, and revisit affected choices when actual results are available. If the user declines the prototype or defers an identified concern, record the consequential uncertainty and proceed within their chosen scope. Do not reopen the same concern without new information or a decision that depends on it.

## Propose an MVP scope

Propose the smallest coherent release that lets the intended first users achieve the agreed outcome. For an existing product, adapt this to the next useful feature or release rather than forcing an MVP exercise.

Identify the core user task and the capabilities needed to complete it. Explain why each belongs in the first release. Include supporting behavior needed for usable, reliable completion; minimal scope should not leave the core task broken. Record relevant constraints and major failure conditions for the requirements stage to detail.

Separate included capabilities from deliberate exclusions and deferred ideas. Explain the important tradeoffs and what would count as a useful release, using agreed outcomes rather than invented targets. Deferring a feature is not a commitment to build it later.

Present a coherent scope proposal with reasons, then explicitly invite the user's suggestions or changes. Bundle related choices so the user can judge the whole first release. Propose tentative defaults for minor details and defer them when they do not affect scope, rather than running a sequence of yes/no approvals. Refine the proposal together before calling it agreed. Continue independent work while decisions are pending, but label dependent details as provisional.

## Handle suggested additions

Assess changes against the core outcome, intended first users, constraints, and dependencies. An addition may reveal a missing essential capability; do not reject it merely because it was absent from the initial proposal.

If a feature is unnecessary for the first release or adds avoidable complexity, explain the specific tradeoff and suggest deferring or simplifying it. Avoid arguing for its own sake. If the user understands and persists, include their choice, record the tradeoff, and update affected scope and planning assumptions. Do not continue describing an expanded release as the smallest possible scope when it includes deliberate extras.

## Capture the result and move on

Adapt the [product-and-scope brief](../templates/product-and-scope-brief.md). Extend existing planning material when that avoids duplication; a small project may need only a few paragraphs.

The result should make the chosen approach, intended first users and outcome, prototype decision, included/excluded capabilities, and unresolved consequential questions clear. Distinguish recommendations from user decisions and note any provisional scope. When the scope is agreed and clear enough, move to collaboratively defining requirements and acceptance criteria. A defined scope is not evidence of validated demand.
