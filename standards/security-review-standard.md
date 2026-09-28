# Diaco Security Review Standard

**Status:** ACTIVE  
**Version:** 0.1

## Scope

Applies to applications and environments we own or are explicitly authorized to test.

## When to run

Security review is especially relevant after changes to:
- authentication
- authorization/roles
- public APIs
- file upload/download
- payment flows
- secrets/configuration
- database/RLS
- exposed admin features
- dependency or deployment boundaries

For major web releases, consider an automated Strix review in addition to normal engineering checks.

## Safety

- Prefer local/staging/test environments.
- Default to non-destructive validation.
- Do not perform destructive exploitation against production without explicit authorization and a recovery plan.
- Never expose real credentials in reports, logs, screenshots, or Git.

## Findings

Automated scanner/Agent findings must be validated.

For each meaningful finding record:
- affected component
- impact
- evidence
- remediation
- regression test or verification after the fix

## Release gate

High-impact unresolved vulnerabilities affecting confidentiality, integrity, authentication, authorization, or data safety must be surfaced before release.
