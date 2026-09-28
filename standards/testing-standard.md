# Diaco Testing & Verification Standard

**Status:** ACTIVE  
**Version:** 0.2

## Principle

Produced code is not evidence that the task works.

## Minimum verification

Use the checks that actually exist for the project:
- build/compile
- tests
- type checking
- lint/static analysis
- runtime/manual user flow
- data migration verification
- print/backup/restore verification when affected

## Web applications

When browser behavior changed and Playwright CLI is available, use it for agent-driven verification such as:
- critical user flows
- screenshots
- traces
- selector/interaction checks
- reproduction of browser-specific failures

One-off browser verification does not replace the project's durable automated tests.

If a meaningful bug is found, add a regression test when practical.

## Security-sensitive changes

For auth, permissions, public APIs, RLS, secrets, file handling, payment, or exposed admin functionality:
- apply `security-review-standard.md`,
- use Strix when authorized and useful,
- validate automated findings before treating them as confirmed.

## Existing projects

Do not invent a giant test framework as a side effect of a small task.

For risky untested legacy behavior, prefer targeted characterization/regression coverage before changing it when practical.

## Failure rule

If a check cannot be run or fails:
- do not claim it passed,
- record the exact limitation/failure,
- state what remains unverified.

## Regression rule

A bug fix should gain a regression guard when practical so the same failure is detectable later.

## Evidence

Important verification results belong in the project handoff when another session/Agent may depend on them.
