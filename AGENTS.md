# <ProjectName> — agent and contributor map

Reference map for contributors and AI agents.

## Quick orientation

| Area | Path | Role |
|------|------|------|
| REST API | `Controllers/Api/` | Attribute routes; global prefix `<ApiPrefix>` |
| Web UI | `Controllers/Web/`, `Views/`, `wwwroot/` | Razor + static assets |
| Business logic | `Services/`, `Services/Interfaces/` | DI-registered services |
| DTOs / domain models | `Models/` | Grouped by feature domain |
| DB scripts | `Database/Scripts/` | Stored procedure scripts |
| Cross-cutting | `Extension/`, `Helpers/` | Routing conventions, DB, helper utilities |

## Cursor configuration

- **Project rules**: `.cursor/rules/*.mdc`
- **Workflow skill**: `.cursor/skills/<stack-workflow>/SKILL.md`
- **Engineering quality skill**: `.cursor/skills/general-engineering-practices/SKILL.md`

## Entry points

- **Composition / middleware**: `Program.cs`
- **API route prefix convention**: `Extension/RoutePrefixConvention.cs` (if used)

## Placeholder customization

Replace placeholders on adoption:
- `<ProjectName>`: repository/application name
- `<RootNamespace>`: C# root namespace
- `<ApiPrefix>`: API URL prefix (for example `api`)
- `<DbSchema>`: database schema (for example `dbo`)
- `<DbPrefix>`: stored procedure prefix (for example `ACL_`)
