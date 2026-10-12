# Skills

Skills I've developed for planning and building digital products.

**Version: 0.2.0** — refined development draft. See the [changelog](CHANGELOG.md).

## product-development

Turn a raw product idea or problem into an implementation-ready specification through discovery, critical evaluation, scoping, requirements, UX definition, technical design, and implementation planning.

**Status: development draft.** Guidance and adaptable templates now cover the full planning workflow, including optional validation, implementation planning, and naming. Local links and invocation-policy syntax checks pass; see validation limits below. Controlled behavioral evaluation and host invocation checks remain pending.

The skill works for a founder defining their own product or someone working with a client. It adapts the depth to the problem, evidence, and consequences of getting the decision wrong. Its responsibility ends at a specification and build plan.

## Invocation

This skill is explicit-only in both supported hosts:

| Host | Invoke | Policy |
| --- | --- | --- |
| Codex | Select `$product-development` in the skill picker, then describe the task | `agents/openai.yaml`: `allow_implicit_invocation: false` |
| Claude Code | Start the message with `/product-development`, followed by the task | `SKILL.md`: `disable-model-invocation: true` |

Use the host’s actual skill mention or slash command. Simply asking a model whether it knows the skill is not a discovery test: explicit-only skills may be absent from its automatic context. In wrappers such as T3, verify that the selected provider receives the explicit invocation. If a wrapper cannot dispatch it, explicitly asking the agent to read the installed `SKILL.md` is a manual fallback; keep automatic invocation disabled.

These policies follow [Codex’s skill settings](https://learn.chatgpt.com/docs/build-skills) and [Claude Code’s invocation controls](https://code.claude.com/docs/en/skills#control-who-invokes-a-skill). End-to-end dispatch in each host still needs verification.

The workflow routes by unresolved decisions and reuses completed work. It does not require every stage or template. Choices delegated to the agent remain distinguishable from user decisions, and conditional work remains separate from work ready to build.

## Structure

```text
skills/
├── README.md
├── CHANGELOG.md
├── VERSION
└── skills/
    └── product-development/
        ├── SKILL.md
        ├── agents/
        │   └── openai.yaml
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
npx skills add . --skill product-development -g -a codex -a claude-code
```

Install from GitHub:

```sh
npx skills add mhmdxsadk/skills --list
npx skills add mhmdxsadk/skills --skill product-development -g -a codex -a claude-code
```

These command forms and the skill folder layout follow the [Vercel skills CLI documentation](https://github.com/vercel-labs/skills). CLI discovery and installation have not yet been tested for this draft.

The local command installs the working-tree revision; the GitHub command installs the pushed revision. The CLI handles agent-specific locations.

## Example requests

After explicitly selecting the skill:

- “Help me decide whether this product idea is worth pursuing, then define what we should build.”
- “We already have discovery notes. Help us identify gaps and turn them into a specification.”
- “I need a small internal tool. Keep the planning proportional to the work.”

## Behavioral evaluation

See [evaluation scenarios](docs/behavioral-evaluation.md) for fixed requests, fixtures, pass/fail criteria, and comparison instructions. These scenarios are specified, not recorded as passed. The user reported one successful informal walkthrough; its transcript and artifacts have not been independently scored.

The bundled Codex scaffold validator rejects Claude Code’s documented `disable-model-invocation` extension because its allowlist does not include that field. We checked the extension’s boolean value separately and validated the remaining scaffold on a temporary copy with only that field omitted. The distributed skill retains the field. This checks structure, not host compatibility or behavior.

## Development status

Supporting references contain stage guidance; templates contain adaptable output structures. The workflow covers problem definition, optional validation, product approach, optional prototypes, MVP scope, requirements, UX, technical design, implementation planning, and naming.

Behavioral evaluation and isolated CLI discovery/installation checks are still pending. The skill is available as a development draft, not a validated release.

## License

No license has been selected yet.

## Versioning

The collection version is recorded in `VERSION`, with changes recorded in `CHANGELOG.md` and releases marked by Git tags such as `v0.1.0`. Patch versions (`0.1.1`) cover fixes and clarifications; minor versions (`0.2.0`) cover new capabilities or substantial workflow changes. Breaking changes during the `0.x` draft phase also increment the minor version and are called out in the changelog.
