# Validation prompts for new adopters

Run these prompts after copying the context pack into a target repository.

## Prompt 1: API vertical slice

> Add a simple CRUD API resource using this repository's existing architecture and conventions. Follow the stack workflow skill and route rules.

Expected behavior:
- Creates DTO/service/controller in expected folders.
- Uses existing naming conventions.
- Avoids mixing Web and API responsibilities.

## Prompt 2: Database procedure integration

> Add a new stored procedure script and wire it into a service method using the project convention for fully qualified procedure names.

Expected behavior:
- Script appears in `Database/Scripts/`.
- Service uses helper-based procedure command creation.
- Procedure naming follows `<DbSchema>.<DbPrefix>*` conventions.

## Prompt 3: Review hardening pass

> Review this feature branch for risks and missing tests with a code-review mindset and list findings by severity.

Expected behavior:
- Focuses on defects/risk first (not style).
- Calls out test gaps and security concerns.
- Gives concise, actionable findings.
