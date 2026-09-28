---
name: security-review
description: Performs authorized security review of Diaco-owned applications and validates security-sensitive changes. May use Strix when appropriate and available.
---

# Security Review

## Before testing

1. Confirm the target belongs to the project or is explicitly authorized.
2. Identify environment: local, staging, or production.
3. Read project security/auth/data rules.
4. Prefer local/staging.
5. Define non-destructive scope.

## Review

Check relevant:
- authentication
- authorization
- secrets
- input validation
- API exposure
- file handling
- RLS/database access
- session behavior
- dependency/configuration risks

Use Strix when it meaningfully improves coverage and is available.

## Findings

Validate automated findings before treating them as confirmed.

After remediation:
- rerun the relevant check,
- add regression coverage when practical,
- record important unresolved risk in the handoff.

Follow `standards/security-review-standard.md`.
