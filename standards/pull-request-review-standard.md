# Diaco Pull Request Review Standard

**Status:** ACTIVE  
**Version:** 0.1

## Principle

Significant changes should be reviewed as a diff before merge/release, even when the same Agent implemented them.

## Review order

1. Understand requested behavior and acceptance criteria.
2. Inspect the actual changed files/diff.
3. Identify correctness and regression risks.
4. Check security, permissions, secrets, and privacy impact.
5. Check database/schema/migration impact.
6. Check platform-specific behavior.
7. Check tests and missing verification.
8. Check unrelated scope creep.
9. Check documentation, standards, and handoff impact.

## Finding quality

A useful finding should include:
- severity or practical impact,
- affected file/area,
- concrete reason,
- reproducible evidence when practical,
- recommended remediation.

Do not manufacture issues merely to produce a long review.

## Merge gate

Block or flag merge/release when there is a credible unresolved issue involving:
- data loss/corruption,
- authentication/authorization bypass,
- committed secrets,
- broken critical flow,
- destructive migration without recovery,
- severe regression,
- failed required verification.

Minor style preferences are not release blockers unless the project explicitly makes them so.

## Tool independence

Use GitHub PR tools, local diffs, Agent review tools, or other available tooling. Diaco owns the review criteria; no single external PR-review plugin is mandatory.
