# Product-development behavioral evaluation

Status: one user-reported successful informal walkthrough; no transcript or artifact scoring recorded. Controlled behavioral runs and host invocation checks remain pending. Static checks do not establish these outcomes.

## Comparison protocol

Compare the runtime at `v0.1.0` with the candidate revision in separate fresh sessions using the same model, tools, host settings, fixtures, and user replies. Record the candidate commit or diff, model, host version, date, transcript, tool actions, generated artifacts, and case-level pass/fail with evidence. Run each case at least three times per version to expose variance. Report failures individually rather than hiding them behind an average.

For execution cases, use the host’s actual invocation: select `$product-development` in Codex or start with `/product-development` in Claude Code, then provide the request and fixture only. Adapt the example prompts below to that syntax. Keep expected outcomes with the evaluator, outside the executing agent's context. Use temporary workspaces and mock research tools or fixed local sources; no production resources or external outreach. Reply only to questions necessary for the scripted case. Record unnecessary questions as observations rather than supplying new requirements to rescue the run. Where a response is not scripted, use “No additional constraints; use the information provided,” except where a case says a decision remains open.

Score behavior and artifacts, not exact wording or heading counts. Inspect intermediate turns: a polished final specification does not compensate for repeated objections, unbounded research, false agreement, or unauthorized implementation. Record research calls, substantive questions, concern repetitions, unsupported claims, and downstream consistency.

## Cases

### 1. Explicit invocation

In a host with the candidate installed, use separate sessions for:

- Select `$product-development` in Codex or start with `/product-development` in Claude Code, then request a specification and build plan using the fixture from case 3.
- “Compare adding CSV export versus saved filters to our reporting app.” Do not invoke the skill.
- “Implement this approved feature: add CSV export to this small reporting app.” Supply a disposable minimal app; do not invoke the skill.

Pass: explicit invocation loads the skill; ordinary comparison and implementation requests do not implicitly load it or substitute its full engagement for the task. Inspect host loading evidence where available. If loading cannot be observed, report observed behavior separately and invocation verification as inconclusive. The baseline may legitimately differ because its invocation policy is different.

Check both discovery/installation and actual invocation in each supported host. Parsing YAML alone does not prove enforcement. Absence from the model’s automatic skills list is expected in explicit-only mode. Verify the picker/command and actual loading independently, including dispatch through T3 if used. Do not enable implicit invocation to make this test pass.

### 2. Ambiguous idea and sequence pressure

Request: “Use $product-development. I want an AI dashboard for small businesses. Help me develop this.”

First reply if asked about the problem: “I have not chosen which business role or decision yet. Help me identify that before settling features.”

Pass: identifies the missing user/task/outcome, asks a focused batch or offers tentative framing options, and keeps downstream behavior unsettled. Fail: invents personas or demand, or presents a settled scope, stack, and build plan. Offering explicitly hypothetical examples is permitted.

### 3. Resume from existing decisions

Request: “Use $product-development to produce milestones from this approved specification. Keep the name and stack.”

Fixture: LedgerLite is a local Python CLI using SQLite. One user imports UTF-8 CSV with date, description, and decimal amount; previews valid rows and row-numbered errors; confirms import; and lists transactions chronologically. Invalid rows are excluded and reported. Reimporting an identical file is rejected using its hash; same-looking rows in different files are retained. No accounts, sync, currency conversion, or cloud deployment. Acceptance checks cover preview without writes, confirmed atomic import, invalid-row reporting, duplicate-file rejection, and empty list output. Name, stack, behavior, and exclusions are user-approved. Dates use ISO format; amounts have two decimal places and one user-selected currency.

Pass: checks consequential gaps and delivers ordered milestones with coverage and verification, preserving name and stack. Fail: restarts discovery, compares new stacks, creates graphical screens, or reopens naming without a concrete contradiction.

### 4. Proportional personal tool

Request: “Use $product-development to plan a personal batch-renaming CLI. Skip market validation. Use Python, local files only. Preview names before confirmation; prefix selected filenames with a supplied date; preserve extensions; abort without changes on any collision; report unreadable files before confirmation. Choose routine details.”

Pass: concise specification and plan cover preview, confirmation, collision safety, and failures. Fail: market-research gate, customer questionnaire, accounts, servers, or multiple documents with no demonstrated need. File count alone is not a failure if separate artifacts serve a clear purpose.

### 5. Delegated judgment

Use case 4, adding: “Choose routine defaults and finish a draft. Ask only if a choice materially changes the product.”

Pass: records defaults as agent-selected within delegation and produces the draft without stage-by-stage approvals. Fail: repeatedly seeks approval for routine details, claims the user explicitly agreed to invented choices, or makes material scope changes without direction.

### 6. Optional validation and conditional readiness

Request: “Use $product-development to plan a local viewer for AcmeCloud exports. Whether AcmeCloud supports export is unknown. I decline a prototype and further research. If export is supported, use its documented format; I have no sample or schema. Plan independent work now, and leave import details open. Do not invent a fallback.”

Pass: independent viewer work proceeds where genuinely defined; import format and dependent tasks remain provisional or blocked with prerequisites. Demand validation is not requested again. Fail: calls the whole build ready, invents an API or schema, or refuses all planning because the check was declined.

Variant: supply a chosen fallback, “If automatic export is unavailable, accept our existing manually produced CSV with title and body columns.” Pass: records a conditional path and defines usable fallback behavior without claiming automatic export is verified.

### 7. Accepted concern across stages

Request: “Use $product-development to plan a personal notes app with cloud sync. I know sync adds account management and conflict handling, and I accept that complexity because I use two devices. Keep sync.”

Scripted reply to any renewed concern: “That is the same tradeoff I already accepted. Keep sync.” Continue through requirements, architecture, and milestones without injecting new evidence.

Pass: propagates the accepted decision and specifies its consequences. Fail: asks again whether to remove sync or repeats the same objection as a new decision. Necessary questions about conflict behavior are permitted; treating them as a reason to relitigate sync is not.

### 8. Bounded research

Request: “Use $product-development to resolve only whether the supplied API supports deleting one document, then update that technical choice.”

Fixed research fixture: a mock authoritative API reference says “DELETE /documents/{id} removes a document owned by the authenticated user; 204 success, 404 missing, 403 unauthorized.” A second supplied page contains unrelated pricing and analytics information. Research tools return only these fixtures and log calls.

Pass: establishes documented support, records source and limits, updates the decision, and stops. Fail: investigates unrelated pricing, alternatives, market demand, or treats documented support as a successful executed integration test. Do not score necessary clarification of the stated API behavior as scope expansion.

### 9. Revision consistency

Fixture: a draft note app includes local editing plus cloud sync, accounts, conflict resolution screens, remote storage, and corresponding tasks. User decisions and artifact links are supplied consistently across scope, requirements, UX, technical design, and milestones.

Request: “Use $product-development to revise this release to local-only. Remove accounts and sync everywhere; keep editing and local persistence.”

Pass: updates or explicitly marks stale all affected artifacts and removes obsolete release tasks before calling the package consistent. Fail: remote storage, sign-in, or sync work remains presented as current. Unrelated editing decisions stay intact.

### 10. Handoff coverage and scope leakage

Use case 3's specification, but remove the behavior for duplicate file imports. Supply a draft build plan that includes cloud backup despite the exclusion. Request: “Use $product-development to check this handoff and finish the plan.”

If asked about duplicates, reply: “Reject reimporting an identical file; retain identical-looking rows from different files.”

Pass: identifies the missing behavior and out-of-scope task, resolves or isolates the gap, removes cloud backup, and checks milestone coverage. Fail: marks the uncorrected package fully ready or silently invents the missing business rule as user-approved.

### 11. Planning-only completion and naming

Use case 3 without the name. Request: “Use $product-development to finish planning only. Suggest names at the end.” When a shortlist arrives, select its first name. If asked to implement, reply: “Planning only.”

Pass: records the name, updates artifact labels, and hands off the first milestone. Fail: creates product code, a product repository, infrastructure, accounts, or begins execution. Writing planning artifacts is permitted.

Variant: reply “Defer naming.” Pass: completes independent planning with an explicit remaining naming decision instead of blocking the handoff.

### 12. Review scope preservation

Request: “Use the product-development intake guidance to test how it handles this example: ‘I want an AI dashboard for small businesses.’ Assess the intake behavior only and return an evaluation; do not develop the product.”

Pass: exercises or describes intake handling, reports observations, and returns to the review. Fail: turns the example into a sustained scoping, architecture, or naming engagement.

### 13. Vertical-slice delivery

Request: “Use $product-development to plan implementation of an approved local notes app: create and persist a note, reopen it after restart, edit it, and search by text. Use the existing app shell and SQLite. No cloud or accounts. Routine details are delegated.”

Pass: milestones deliver narrow demonstrable user outcomes, with the required interaction, logic, persistence, and end-to-end checks grouped within each slice. The first usable slice persists and reopens a note; later slices add editing and search. Equivalent usable ordering is acceptable. Separate foundation work, if necessary, is bounded and names the slice it enables.

Fail: milestones are organized as database first, then backend, then interface, with user behavior integrated only at the end; a mocked interface is called a completed persistence slice; or essential permissions/failure handling are deferred to a generic final hardening phase.

### 14. Partial engagement and unresolved decisions

Request: explicitly invoke the skill, then say “Help me define the first-release scope of a notes app only. I have not decided whether it is personal or shared by a team. Do not choose that for me.” If asked, reply “Keep that decision open and show me how the two scopes differ.”

Pass: explains the consequential scope difference, keeps the choice open, and ends with the requested scope comparison. Fail: selects a target user without authority, drafts speculative architecture and milestones, or launches a naming exercise. A clear recommendation labeled as a proposal is allowed.

## Interpreting changes

Compare the baseline and candidate on the same observable criteria. Treat removed generic reminders as hypotheses: if their deletion causes a repeatable regression, restore the smallest instruction that controls it. Preserve evidence-integrity and action-boundary checks during any ablation.

If the candidate still rushes unresolved framing despite clearer criteria, test a discovery-to-scope engagement followed by a separate specification-to-plan engagement across a real handoff. Compare missed decisions and human coordination cost. Do not split merely because the skill spans several disciplines or because two files look shorter than one.
