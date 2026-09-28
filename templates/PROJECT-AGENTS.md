# Project Agent Rules

This file defines how AI agents must work in this repository.

## Required reading order

Before substantial work, read in this order:

1. Central coordination rules in `00-AI-HUB/AGENT-START-HERE.md`
2. Shared Diaco operating rules in `diaco-agent-skills/AGENTS.md`
3. Any Diaco skill relevant to the current task
4. This project's own rules and specifications
5. This project's `HANDOFF.md`
6. The actual files, tests, configuration, and Git state relevant to the task

## Rule precedence

When instructions conflict, use this precedence:

1. Current project-specific rules and explicit project specifications
2. Current repository state and verified Git state
3. Current project handoff
4. Shared Diaco rules and skills
5. Central hub guidance
6. Conversation history

Project-specific rules may intentionally override shared Diaco defaults.

## Existing projects

Before changing an established project:

- inspect the current codebase
- read relevant files and tests
- understand existing patterns
- preserve unrelated working behavior
- keep changes scoped and reversible
- verify the affected behavior before declaring completion

## Cross-session continuity

This repository must not depend on one chat session.

Maintain `HANDOFF.md` whenever:
- work is unfinished
- another Agent may continue later
- an important decision was made
- a risky change was introduced
- verification results matter for continuation

## Required handoff contents

`HANDOFF.md` should include, when relevant:

- current branch
- last known stable commit
- current state
- completed work
- verification performed
- unresolved issues
- next action
- important files
- external services
- do-not-change constraints

## Security

Never commit real secrets, credentials, tokens, passwords, private keys, or production service keys.

## Completion

A task is complete only after:
- requested behavior is implemented
- relevant verification is performed
- failures are reported accurately
- durable project state is updated when future continuation is expected
