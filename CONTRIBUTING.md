# Contributing

## Scope

This repository stores reusable AI context artifacts:
- `.cursor/rules/`
- `.cursor/skills/`
- `AGENTS.md`

## Change policy

- Keep one concern per pull request when possible.
- Include rationale for behavior changes.
- Avoid broad wording changes that alter agent behavior unintentionally.

## Review requirements

- At least one reviewer approval is required for context changes.
- Changes that alter conventions must include a `CHANGELOG.md` entry.
- Breaking behavior changes require a major version bump.

## Versioning rules

- `PATCH`: typo clarifications, non-behavior wording fixes.
- `MINOR`: additive guidance or new optional rule/skill.
- `MAJOR`: incompatible behavioral change to existing guidance.
