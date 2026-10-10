# Intake and problem definition

Purpose: turn the user's starting material into a defensible account of the problem and a useful next decision. Do not prematurely convert a requested solution into a feature list.

## 0. Intake

Extract what the user has already supplied:

- The request and current stage: exploring an idea, deciding whether to invest, defining a prototype, or refining an existing specification.
- Context along separate dimensions: who is driving the work (self-directed, client, internal team, or another sponsor); who the product is for (the requester, internal users, or an intended user group/market); and the kind of product (personal or internal tool, commercial product such as SaaS, or another form). These may overlap rather than fit one category.
- Existing evidence and artifacts, including conflicting versions or decisions already made.
- Constraints that may change feasibility or scope: time, resources, required platforms/integrations, sensitive data, contractual obligations, or dependencies.
- Who experiences the problem, who pays or sponsors the work, and who decides scope. These may be the same person.

Treat context as a working judgment, not a questionnaire. Recommend concise or deeper planning with a reason; the user can override it. A self-directed commercial product may begin with the builder's own problem, but do not assume that others share it or that demand is established. Do not demand commercial market research for a personal tool, or assume an internal tool has no adoption or operational risks.

If existing material is sufficient, summarize the relevant decisions and advance. If it conflicts, identify the decision affected and ask the appropriate owner to resolve it.

## 1. Define the problem

Seek enough specificity to explain:

- **Who and when:** the primary affected person or group and the situation that triggers the problem.
- **Current task:** what they are trying to accomplish and how they do it today.
- **Pain and consequence:** where the current approach fails, how often it happens if known, and what it costs or prevents.
- **Desired outcome:** what improvement would matter, independent of the proposed feature or technology.
- **Alternatives:** existing tools, workarounds, manual services, or leaving the situation unchanged.
- **Evidence and uncertainty:** what supports this account, what is assumed, and what could materially change the next decision.

Do not invent personas, pain frequency, budgets, interviews, market demand, or numeric targets. A user's first-hand experience is usable evidence about their situation; it is not proof of broad demand. A client's request establishes a preference, not necessarily the underlying need.

Separate problem from proposed solution without discarding explicit commitments. If a technology is contractually required, record it as a constraint. If it is only a preference, preserve it as a preference and examine whether it serves the outcome.

## Ask and challenge selectively

Ask only what cannot be safely inferred and affects the next recommendation. Prefer one short batch, then adapt to the answer instead of administering a fixed survey. Record inferred context as tentative.

For example, “I want an AI dashboard for small businesses” leaves the user, task and pain unclear. Ask which person makes which decision, how they do it today, and what goes wrong. Do not start selecting models or dashboard widgets.

For a personal tool to rename a known set of files, clarify naming rules, collision behavior and the desired outcome as needed. Do not require customer segmentation or willingness-to-pay studies.

Challenge a solution-first premise when there is a meaningful reason to question it. Explain the concern and work through alternatives with the user toward a sound decision; do not argue for its own sake or invent objections. Preserve firm requirements as constraints, distinguish preferences from requirements, and do not argue indefinitely after an informed choice.

## Produce the brief

Use the [problem-brief template](../templates/problem-brief.md) as an adaptable structure. A short task may fit in a few paragraphs. Give claims stable identifiers only when later evidence or requirements need to reference them.

Track critical assumptions with their basis, consequence if false, and the next evidence needed. Avoid numeric confidence scores without a meaningful basis. State unresolved success targets as unresolved; identify who can set them or how they will be established.

## Exit decision

The brief is sufficient for the next stage when it identifies a primary affected user, a specific situation/task, a meaningful desired outcome, relevant constraints, and the uncertainties affecting the next investment. This is not a claim that the opportunity is validated. Validation is optional: use evidence already available, offer further validation if the user wants it or it could change a consequential decision, and allow the user to continue without it while stating material uncertainty.

- PROCEED to discovery or definition when the problem is clear enough and residual uncertainty is tolerable for that next step.
- VALIDATE when an assumption could change whether or what to build; propose a focused test with an observable result.
- REVISE when the framing conflates different users/problems or the solution conflicts with the desired outcome.
- PARK or KILL only with a reason beyond incomplete information; record conditions for reconsideration where useful.

Return the brief, recommendation, reasons, and unresolved questions. Obtain user direction when proceeding would materially change the intended problem or scope. Otherwise continue within the existing request.
