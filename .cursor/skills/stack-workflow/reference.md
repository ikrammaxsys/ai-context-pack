# Stack workflow reference

## Example stored procedure naming patterns

These illustrate naming only.

| Pattern | Example |
|---------|---------|
| Read | `<DbSchema>.<DbPrefix>User_GetAll` |
| Paged | `<DbSchema>.<DbPrefix>User_GetAllPaged` |
| Write | `<DbSchema>.<DbPrefix>User_Create`, `<DbSchema>.<DbPrefix>Role_Update` |
| Composite / bridge | `<DbSchema>.<DbPrefix>User_GetWithRolesAndAccess`, `<DbSchema>.<DbPrefix>UserRole_Create` |

Always pass fully qualified procedure names to `StoredProcedureHelper.CreateCommand`.

## High-level repo tree

```
Controllers/
  Api/          # JSON + Swagger
  Web/          # MVC pages
Services/
  Interfaces/
Models/
Database/
  Scripts/      # <DbPrefix>*.sql
Extension/
Helpers/
Views/
wwwroot/        # Feature folders + js/utils
```

## API discovery

Use Swagger UI in Development as the source of truth.
