---
name: pull-request-review
description: Reviews a proposed code change or pull request against Diaco correctness, regression, security, data, testing, and scope criteria before merge or release.
---

# Pull Request Review

## Workflow

1. Read the task/spec and project rules.
2. Inspect the actual diff, not only a summary.
3. Read surrounding code needed to judge behavior.
4. Check tests and verification evidence.
5. Report only actionable findings.
6. Separate blockers from non-blocking improvements.
7. If no material issue is found, say so and state remaining verification limits.

## Required checks

- requested behavior
- regressions
- security/secrets
- auth/permissions when relevant
- database/data/migrations
- platform-specific concerns
- error handling
- tests
- unrelated scope
- handoff/docs impact

Follow `standards/pull-request-review-standard.md`.
