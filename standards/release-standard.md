# Diaco Release Standard

**Status:** ACTIVE  
**Version:** 0.1

## Goal

Keep releases understandable, reversible, and transferable across Agents.

## Before release

Confirm where applicable:
- relevant tests/checks pass,
- application builds,
- user flow works,
- migrations are accounted for,
- secrets are not committed,
- backup/rollback exists for risky data changes,
- handoff/current state is updated.

## Versioning

Use the project's existing versioning scheme if it has one.

Do not silently introduce or replace a versioning scheme in an established project.

For new projects, semantic-style `MAJOR.MINOR.PATCH` is the default unless project needs justify another scheme.

## Git

Prefer:
- descriptive commits,
- meaningful release tags when the project uses tags,
- a clear stable commit,
- no destructive history rewriting on shared/stable branches without explicit approval.

## Rollback

Risky releases must have a practical rollback/recovery path appropriate to the platform:
- previous binary/package,
- previous deployment,
- database backup/migration rollback,
- feature flag,
- or documented recovery procedure.

## Handoff

After a significant release, record:
- released version/tag/commit,
- verification performed,
- known limitations,
- migration notes,
- rollback/recovery information when relevant.
