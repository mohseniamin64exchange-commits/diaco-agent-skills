# Diaco Testing & Verification Standard

**Status:** ACTIVE  
**Version:** 0.1

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
