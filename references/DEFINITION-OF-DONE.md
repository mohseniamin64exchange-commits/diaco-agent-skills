# Diaco Definition of Done

A change is done only when both its task-specific acceptance criteria and this standing quality bar are satisfied.

## Correctness
- [ ] Requested behavior is implemented.
- [ ] Existing relevant behavior is preserved unless intentionally changed.
- [ ] Edge/error cases relevant to the task are handled.

## Verification
- [ ] Relevant tests pass, when tests exist.
- [ ] Build/type/lint checks pass when applicable.
- [ ] Runtime or user-flow behavior is checked when applicable.
- [ ] Any unverified area is explicitly reported.

## Scope
- [ ] No unrelated refactors were introduced.
- [ ] No unexplained dependency or architecture change was introduced.
- [ ] No secrets or credentials were committed.

## Continuity
- [ ] Important decisions are persisted in the repository.
- [ ] A handoff is updated when another session/Agent may need to continue.
- [ ] The next Agent can identify the current state without needing the previous chat.
