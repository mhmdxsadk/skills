# Requirements and UX

Purpose: turn the chosen scope into collaboratively defined product behavior, user workflows, and a portable design brief. Give a builder and designer enough direction to work without inventing major behavior, while leaving proposed choices open to user input.

## Start from the agreed scope

Reuse existing requirements, designs, platform choices, and the product-and-scope brief. Summarize the intended users, core outcome, included capabilities, and relevant unresolved decisions. If a scope choice is still provisional, keep its dependent requirements provisional too. Do not reopen settled choices merely to fill a template.

For a small product, a few paragraphs and a flow may suffice. For a larger one, use separate requirement and design sections or documents. Add identifiers only when they make references across requirements, flows, and later tasks easier to maintain.

## Propose requirements, then refine together

Give the user an initial proposal for each agreed capability. Describe the user or role, triggering situation, expected behavior and result, relevant business rules, and important constraints. Cover permissions, data handling, and quality needs where they change the behavior or consequences of failure. Do not invent numeric performance targets, retention periods, or business policies; propose a reasoned option or leave a consequential choice open.

Acceptance criteria should describe observable conditions that demonstrate the behavior works. Include the successful path and material failure or boundary cases, without listing every imaginable exception. Avoid prescribing frameworks or internal implementation merely to make a requirement sound precise.

For example, an upload requirement might propose that a successfully saved document appears in the library and a failed upload offers recovery without claiming success. Supported formats and size limits remain proposed or unresolved until established. A criterion such as “upload works correctly” is too vague to verify.

Present related requirements as a coherent draft, explain consequential choices, and invite corrections or additions. Ask focused questions about differences that materially affect behavior. Routine wording does not need individual approval. Keep proposed, agreed, and unresolved details distinguishable; silence is not acceptance of an assumption.

When a requested change expands scope, explain its effect and update the scope decision before treating it as an agreed requirement. Apply the shared rule for constructive pushback and respect the user's informed choice.

## Map user workflows, then feature workflows

Start with the important user goals across the product. For each workflow, describe its starting context, the user's actions and system responses, and the outcome that counts as completion. Show navigation or transitions between capabilities where relevant.

Zoom in on individual features when their steps, branches, or states need more definition. For example, “collect documents → find a relevant one → use its information” is a user workflow; selecting a file, waiting for processing, and recovering from a failed upload form a feature workflow.

Include material loading, empty, partial, error, and success states where applicable. Explain what users know, what they can do next, and whether their input or progress is preserved. Define permissions and accessibility needs that affect completing the task. Do not force a state checklist onto a feature that does not need it.

Use plain steps, a diagram, or a small state table according to what makes the behavior easiest to review. Cross-reference requirements rather than duplicating whole descriptions. If a flow reveals missing or contradictory behavior, revise the affected requirement with the user; do not silently introduce features through UX work.

## Produce a design brief

For products with screens, produce a brief a designer or design tool can use without this conversation. Include enough product context, intended users, platform constraints, and links or excerpts from the agreed requirements and workflows to make it understandable.

For each needed screen or view, describe:

- Its purpose and the user goal it supports.
- How users arrive, navigate onward, and return where relevant.
- The content and information hierarchy, with primary and supporting actions.
- The important states and recovery behavior defined in the workflows.
- Relevant accessibility and interaction constraints.

Include supplied visual references, style preferences, and existing branding. Label any suggested visual direction as a proposal. Do not invent a brand identity or require a final product name at this stage; naming comes later. Simple wireframes may clarify difficult layouts, but polished mockups are not required for every screen. Keep the format portable and do not require a particular design application.

For a product without a graphical interface, describe its interaction surfaces as relevant rather than inventing screens. If later design exploration changes behavior or scope, update the linked requirements and workflows before presenting them as consistent.

## Finish this stage

Adapt the [requirements template](../templates/requirements.md) and [design brief template](../templates/design-brief.md), or extend existing artifacts. They may be sections in one document rather than separate deliverables.

Review whether each included capability has understandable behavior and meaningful completion checks, whether important user goals can be completed through the flows, and whether the design brief reflects those decisions. Record remaining questions and which downstream choices depend on them.

When the material is agreed and clear enough, proceed to technical design. Continue independent technical planning if some choices remain open, but do not describe unresolved major behavior as implementation-ready. Do not begin implementation as part of this stage.
