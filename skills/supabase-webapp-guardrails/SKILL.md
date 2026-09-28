---
name: supabase-webapp-guardrails
description: Provides safety rules for Diaco web applications using Supabase. Use when modifying authentication, database tables, RLS policies, Edge Functions, scheduled jobs, environment variables, or frontend integrations with Supabase.
---

# Supabase Web App Guardrails

## Before changing anything

Identify:
- Supabase project/environment
- schema and affected tables
- current authentication flow
- existing RLS policies
- Edge Functions involved
- scheduled jobs/webhooks involved
- environment variables required

Never guess production identifiers from old chat history when the project can be inspected.

## Database and RLS

- Treat schema changes as high-impact.
- Preserve existing data unless migration explicitly requires transformation.
- Review RLS whenever table access changes.
- Test access for intended roles/users, not just service-role access.
- Avoid solving authorization problems by disabling RLS.

## Secrets

Never commit:
- service-role key
- private API keys
- database passwords
- webhook secrets

Keep placeholders in `.env.example`.

## Edge Functions and jobs

For scheduled or background behavior:
- make execution idempotent where possible
- log actionable failures without exposing secrets
- distinguish deployment success from end-to-end behavior
- verify trigger configuration as well as function code

## Auth

Do not replace a working auth model casually.
Verify:
- sign-in/out
- session persistence
- protected routes
- role/ownership enforcement
- recovery/verification flows when affected

## Verification

- [ ] Correct project/environment was identified.
- [ ] No secrets were committed.
- [ ] RLS/security impact was checked.
- [ ] Migration implications were considered.
- [ ] Relevant frontend + backend flow was verified.
