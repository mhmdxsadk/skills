# Changelog

Versions apply to the skills collection as a whole. Each published version has a matching Git tag, such as `v0.1.0`.

## 0.2.0 — 2026-10-12

### Changed

- **Invocation change:** the skill now requires explicit invocation in Codex and Claude Code. Select `$product-development` in Codex or use `/product-development` in Claude Code; ordinary matching requests no longer activate it automatically.
- Route work by unresolved decisions and reuse sufficient existing material instead of requiring a full stage sequence. Keep partial engagements within their requested deliverable.
- Define delegated decision authority, work readiness, bounded research, and conditions for reopening accepted concerns.
- Plan implementation as vertical slices with usable end-to-end outcomes and verification. Tie separate foundation work to the slice it enables.
- Clarify conditional handoffs and propagate consequential revisions across affected artifacts.
- Consolidate shared guidance and simplify references and templates while retaining optional validation and the planning-only boundary.

### Added

- Behavioral evaluation scenarios covering invocation, planning reliability, vertical slices, and partial engagements.
- Installation and explicit-invocation guidance for Codex and Claude Code, including wrapper limitations.

### Validation and known limitations

- One successful informal user walkthrough was reported; controlled behavioral comparisons and host invocation verification remain pending.
- Local link and invocation-policy syntax checks passed. The bundled Codex scaffold validator rejects the documented Claude invocation field; the remaining scaffold passed on a temporary copy with that field omitted.
- This remains a development draft. No license has been selected.

## 0.1.0

Initial development draft.

### Added

- Product-development skill covering problem definition, optional validation, product approach, optional prototypes, MVP scope, requirements, UX, technical design, implementation planning, and naming.
- Supporting stage guidance and reusable planning templates.
- Collaborative recommendations, optional validation, and a planning-only boundary.

### Known limitations

- Behavioral evaluation and CLI discovery/installation verification remain pending.
- No license has been selected.
