# AI Context Pack

Reusable Cursor context package for:
- project rules (`.cursor/rules/*.mdc`)
- workflow skills (`.cursor/skills/*/SKILL.md`)
- contributor/agent orientation (`AGENTS.md`)

Use this repo as a baseline in new projects so AI behavior is consistent across teams.

## Contents

- `AGENTS.md`
- `.cursor/rules/`
- `.cursor/skills/`
- `CHANGELOG.md`
- `examples/`

## Quick start (copy-in model)

1. Copy these paths into your target repository:
   - `.cursor/rules/`
   - `.cursor/skills/`
   - `AGENTS.md`
2. Replace placeholders documented in `AGENTS.md` and rule/skill files:
   - `<ProjectName>`
   - `<RootNamespace>`
   - `<ApiPrefix>`
   - `<DbSchema>`
   - `<DbPrefix>`
3. Remove rules that do not apply to the target stack.
4. Run validation prompts (see `examples/validation-prompts.md`).

## Placeholder policy

This package intentionally uses placeholders instead of hard-coded project values.
Downstream repos should replace placeholders during setup and keep behavior-focused guidance intact.

## Versioning

- Follows Semantic Versioning: `MAJOR.MINOR.PATCH`.
- See `CHANGELOG.md` for migration notes.

## Recommended governance

- Assign one owner for AI context updates.
- Require PR review for all changes to `.cursor/rules`, `.cursor/skills`, and `AGENTS.md`.
- For behavior-changing updates, include migration notes in `CHANGELOG.md`.
