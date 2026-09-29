# Diaco Agent Skills

Reusable workflows, shared standards, engineering tools, design-engineering references, business-data tooling, and repeatable marketing workflows for AI-assisted projects.

**Current version:** 0.6.0

## Important capabilities

- project continuity and GitHub-backed memory
- Windows and Supabase platform profiles
- UI design engineering
- local-business and supplier discovery
- repeatable marketing and growth workflows
- testing, security review, and PR review

## Marketing workflow

Diaco now treats the combination of these two sources as an important reusable capability:

- `Mahanaicoach/google-maps-scraper-kit`
- `coreyhaines31/marketingskills`

Typical flow:

```text
Product context
→ Local business discovery
→ Clean / deduplicate
→ Qualify / segment
→ Prepare marketing output
→ Human review
→ Measure
→ Repeat only after pilot success
```

References:
- `references/google-maps-scraper-kit.md`
- `references/marketing-skills.md`

Skills:
- `skills/local-business-data/SKILL.md`
- `skills/automated-marketing-growth/SKILL.md`

## Validation principle

A workflow is not considered successful just because an Agent produced output.

Start with a small pilot and measure:
- business-record accuracy
- duplicate rate
- contact validity
- qualified-record rate
- human acceptance of generated output
- downstream business results when available

## Core principles

1. GitHub is the durable source of truth.
2. Important project state must not live only in chat history.
3. Read before modifying an existing project.
4. Preserve scope and working behavior.
5. Verify changes with evidence.
6. Use specialized tools only when relevant.
7. Keep secrets out of Git.
8. Do not scale a workflow before its pilot is validated.
9. Real business/project/customer data outranks generic model assumptions.
