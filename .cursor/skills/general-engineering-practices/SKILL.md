---
name: general-engineering-practices
description: Applies a consistent quality bar to code and documentation changes, covering build/test discipline, security, error handling, and PR quality.
---

# General engineering practices

Stack-agnostic checklist for finishing work and preparing review.

## Before finishing a change

- [ ] Build succeeds; run lint/format commands if the repo defines them.
- [ ] Run tests if present; add or update tests for non-trivial behavior.
- [ ] Smoke-test critical user paths for user-visible changes.
- [ ] Ensure no secrets, tokens, or production credentials are committed.
- [ ] New dependencies are justified (maintenance, size, and license).

## Pull request and review

- [ ] Keep scope clear and focused on one concern when practical.
- [ ] Explain what changed and why.
- [ ] Consider edge cases, failure modes, and rollback strategy for risky changes.
- [ ] Keep diffs reviewable; avoid unrelated formatting churn.

## Security and data handling

- [ ] Validate untrusted input at boundaries (HTTP, files, external APIs).
- [ ] Apply least privilege for service/database permissions.
- [ ] Avoid logging passwords, tokens, or unnecessary PII.

## Observability and errors

- [ ] Error messages are actionable for operators.
- [ ] Avoid swallowed exceptions and empty catch blocks.

## Documentation

- [ ] Update README/runbooks when setup or behavior changes.
- [ ] For APIs, treat generated docs (for example Swagger) as the source of truth where available.
