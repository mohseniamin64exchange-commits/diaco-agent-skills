---
name: project-context-handoff
description: Preserves project state across chats, accounts, devices, and AI agents. Use when starting or ending a substantial session, switching Agents, or when conversation history cannot be trusted as persistent project memory.
---

# Project Context and Handoff

## Goal

Another capable Agent should be able to continue the project from repository artifacts without needing the previous conversation.

## Start-of-session workflow

1. Read project rules and README.
2. Read the latest handoff.
3. Inspect `git status`, active branch, and recent relevant commits when available.
4. Read the files involved in the current task.
5. Reconcile any conflict between handoff text and actual repository state.

Repository state wins over stale handoff text.

## End-of-session workflow

Update or create a handoff containing:
- repository and branch
- last known stable commit when useful
- current working state
- completed work
- verification performed and results
- unresolved issues
- next recommended action
- critical do-not-change constraints
- important files/services

Do not paste the chat transcript.

## Red flags

- "The next chat will remember."
- State exists only in conversation.
- Handoff says work is complete but repository verification disagrees.
- No next action is recorded for unfinished work.

## Verification

- [ ] Another Agent can identify where to start.
- [ ] Current state matches the repository.
- [ ] Verification results are explicit.
- [ ] Unresolved work and constraints are explicit.
