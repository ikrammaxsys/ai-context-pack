---
name: stack-workflow
description: Develops features on a layered ASP.NET stack (API vs Web controllers, services, stored procedures, and wwwroot assets) using a vertical-slice workflow.
---

# Stack workflow

Use `.cursor/rules/*.mdc` for naming/layout constraints. This skill defines process only.

## New solution / repo bootstrap (checklist)

- [ ] Align with ASP.NET Core app structure and consistent namespace (`<RootNamespace>`).
- [ ] Split controllers: `Controllers/Api/` (JSON) vs `Controllers/Web/` (MVC).
- [ ] Configure route prefix convention so API controllers use `<ApiPrefix>` (if this architecture uses prefix conventions).
- [ ] Register business services in `Program.cs` (`AddScoped<I..., ...>()` or intentional lifetime).
- [ ] Add/confirm folders: `Services/`, `Services/Interfaces/`, `Models/<Domain>/`, `Database/Scripts/`, `Extension/`, `Helpers/`.
- [ ] For DB via stored procedures: call `<DbSchema>.<DbPrefix>*` and keep matching scripts under `Database/Scripts/`.

## Vertical slice (new feature) checklist

1. Model/request DTOs under `Models/` in the right subfolder.
2. Interface in `Services/Interfaces/` plus implementation in `Services/`.
3. API controller in `Controllers/Api/` with `[Route("...")]` and HTTP verbs.
4. Optional UI: Web controller in `Controllers/Web/`, views in `Views/`, scripts in `wwwroot/<Feature>/` or `wwwroot/js/utils/`.
5. SQL: script in `Database/Scripts/`; service calls the same `<DbSchema>.<DbPrefix>*` name.

## Definition of done

- [ ] Project builds successfully.
- [ ] New API actions appear in Swagger (Development).
- [ ] Procedure names in C# match deployed script names.
- [ ] UI assets follow conventions in the target feature folder.

## More detail

- Naming patterns and layout examples: [reference.md](reference.md)
