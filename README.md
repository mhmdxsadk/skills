# Skills

Skills I've developed for planning and building digital products.

**Version: 0.1.0** — initial development draft. See the [changelog](CHANGELOG.md).

## product-development

Turn a raw product idea or problem into an implementation-ready specification through discovery, critical evaluation, scoping, requirements, UX definition, technical design, and implementation planning.

**Status: development draft.** Guidance and adaptable templates now cover the full planning workflow, including optional validation, implementation planning, and naming. Scaffold and local link checks pass; behavioral evaluation and CLI discovery/installation checks remain before release.

The skill works for a founder defining their own product or someone working with a client. It adapts the depth to the problem, evidence, and consequences of getting the decision wrong. Its responsibility ends at a specification and build plan.

## Structure

```text
skills/
├── README.md
├── CHANGELOG.md
├── VERSION
└── skills/
    └── product-development/
        ├── SKILL.md
        ├── references/
        │   ├── intake-and-problem-definition.md
        │   ├── discovery-and-validation.md
        │   ├── product-definition-and-scope.md
        │   ├── requirements-and-ux.md
        │   ├── technical-design.md
        │   ├── implementation-planning.md
        │   └── naming.md
        └── templates/
            ├── problem-brief.md
            ├── evidence-and-validation.md
            ├── product-and-scope-brief.md
            ├── requirements.md
            ├── design-brief.md
            ├── technical-design.md
            └── build-plan.md
```

The installable skill is self-contained under `skills/product-development/`. It does not depend on a particular model, vendor API, connector, or agent-specific UI.

## Installation

From this repository's root, inspect the draft with:

```sh
npx skills add . --list
```

Install locally only if you want to try the development draft:

```sh
npx skills add . --skill product-development
```

Install from GitHub:

```sh
npx skills add mhmdxsadk/skills --list
npx skills add mhmdxsadk/skills --skill product-development
```

These command forms and the skill folder layout follow the [Vercel skills CLI documentation](https://github.com/vercel-labs/skills). CLI discovery and installation have not yet been tested for this draft.

## Example requests

- “Help me decide whether this product idea is worth pursuing, then define what we should build.”
- “We already have discovery notes. Help us identify gaps and turn them into a specification.”
- “I need a small internal tool. Keep the planning proportional to the work.”

## Development status

Supporting references contain stage guidance; templates contain adaptable output structures. The workflow covers problem definition, optional validation, product approach, optional prototypes, MVP scope, requirements, UX, technical design, implementation planning, and naming.

Behavioral evaluation and isolated CLI discovery/installation checks are still pending. The skill is available as a development draft, not a validated release.

## License

No license has been selected yet.

## Versioning

The collection version is recorded in `VERSION`, with changes recorded in `CHANGELOG.md` and releases marked by Git tags such as `v0.1.0`. Patch versions (`0.1.1`) cover fixes and clarifications; minor versions (`0.2.0`) cover new capabilities or substantial workflow changes. Breaking changes during the `0.x` draft phase also increment the minor version and are called out in the changelog.
