---
name: safe-existing-project-change
description: Makes controlled changes to established codebases while protecting working behavior. Use when fixing bugs, adding features, refactoring, or editing a project that already has users, history, or undocumented constraints.
---

# Safe Existing Project Change

## Workflow

### 1. Inspect
- read project rules
- inspect current Git state
- read files to be modified
- inspect related tests and analogous code

### 2. Establish baseline
Identify what currently works and how it is verified.

For risky areas with weak tests, add characterization coverage where practical before refactoring.

### 3. Define scope
State:
- what must change
- what must not change
- files/modules expected to be touched

### 4. Change incrementally
Prefer one logical change at a time.

Keep the project buildable/recoverable between meaningful steps.

### 5. Verify
Run relevant checks and affected user flow.

### 6. Persist
Commit according to project policy and update the handoff when continuation is expected.

## Never

- delete unexplained code because it "looks unused"
- replace architecture as a side effect
- suppress failing tests to obtain green output
- modify unrelated formatting across the codebase
- claim verification that was not performed

## Verification

- [ ] Baseline was understood.
- [ ] Scope stayed controlled.
- [ ] Working behavior outside the task was protected.
- [ ] Relevant checks passed or failures are documented.
- [ ] Rollback/recovery remains possible.
