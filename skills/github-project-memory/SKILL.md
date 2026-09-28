---
name: github-project-memory
description: Uses GitHub repositories as durable shared memory for AI-assisted work. Use when important tools, project decisions, reusable workflows, upstream sources, or cross-session state must remain available across accounts and devices.
---

# GitHub Project Memory

## Principle

If information is required to continue future work and exists only in chat, it is not yet durably stored.

## What belongs in GitHub

Store:
- project rules
- architecture decisions
- reusable workflows
- upstream references
- current handoff/state
- non-secret configuration examples
- verification commands
- links between related repositories

Do not store:
- passwords
- API keys
- access tokens
- private keys
- recovery codes
- production credentials

## Central hub pattern

Use a lightweight hub repository as an index and coordination layer.

The hub may contain:
- repository registry
- tool/upstream registry
- global rules
- reusable handoff templates
- pointers to authoritative project repositories

Do not copy whole application repositories into the hub.

## Original vs customized repositories

Record separately:
- upstream owner/repository
- our customized repository
- reason for customization
- upstream commit/tag when relevant
- license/attribution requirements

## Verification

- [ ] Durable information is in the appropriate repository.
- [ ] Secrets are absent.
- [ ] Upstream and customized versions are distinguishable.
- [ ] The hub links to authoritative project state rather than duplicating it.
