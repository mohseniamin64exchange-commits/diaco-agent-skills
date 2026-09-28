# Diaco Backup & Restore Standard

**Status:** DRAFT  
**Version:** 0.1

## Goal

Provide one reusable backup/restore contract across Diaco applications.

## Approved rules already in force

- Backup and restore are a pair; backup is not complete until restore is proven.
- Define exactly what data/files/configuration are included.
- Never silently overwrite the only recoverable copy.
- Validate backup integrity before declaring success where practical.
- Preserve compatibility information/version metadata when format changes matter.
- Record failures clearly.
- Secrets should not be exposed merely because a backup was created.
- Existing production/user data must not be reset to simplify development.

## Not yet standardized

Requires a real approved reference:
- file/folder naming
- archive format
- compression
- encryption/password behavior
- destination selection
- automatic backup cadence
- retention count
- local/network/cloud targets
- progress UI
- success/failure dialog
- metadata manifest
- restore confirmation flow
- rollback behavior after failed restore

## Promotion workflow

When the user identifies an existing backup form/process as the standard:
1. inspect the exact implementation,
2. capture included data and workflow,
3. test restore using representative data,
4. extract reusable rules,
5. promote approved parts to ACTIVE.
