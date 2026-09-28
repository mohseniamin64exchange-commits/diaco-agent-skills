# Diaco User Management Standard

**Status:** DRAFT  
**Version:** 0.1

## Goal

Standardize reusable user, role, permission, login, and administrative patterns without forcing one authentication technology onto every project.

## Approved rules already in force

- Authentication and authorization are separate concerns.
- Users must only receive permissions they actually need.
- Existing authentication architecture should not be replaced casually.
- Passwords/secrets must never be stored in plaintext or committed to Git.
- Permission checks belong at the actual protected boundary, not only in the UI.
- Project-specific roles may override generic role names.

## Not yet standardized

Requires an approved reference implementation:
- exact user-management screen layout
- default roles
- role hierarchy
- permission naming scheme
- user creation/edit flow
- password-reset/admin-reset flow
- account lock/disable behavior
- audit trail
- login screen design
- session timeout behavior

## Promotion workflow

Use an approved application section as the reference, extract reusable patterns, and promote only the parts that should apply across projects.
