---
name: automated-marketing-growth
description: Builds and validates repeatable marketing workflows by combining local-business discovery, product marketing context, prospect qualification, messaging, structured output, and measurable evaluation.
---

# Automated Marketing & Growth

## Goal

Turn Diaco's marketing tools into a measurable workflow, not a content generator.

## Primary components

1. `Mahanaicoach/google-maps-scraper-kit` — business discovery
2. `coreyhaines31/marketingskills` — marketing strategy and execution guidance
3. project/customer/product data — source of truth
4. `structured-data-output` — approved Persian list/spreadsheet presentation
5. CRM/spreadsheet/database — state and deduplication
6. optional scheduler/Jarvis/Agent — orchestration
7. human approval for outbound actions unless explicitly authorized otherwise

## Default workflow

### Phase 1 — Product context
Build or update product-marketing context:
- what we sell
- target customer
- geography
- value proposition
- ideal customer profile
- disqualifiers
- proof/constraints

### Phase 2 — Discovery
Use the approved Google Maps scraper for a small targeted batch when local-business discovery is relevant.

### Phase 3 — Clean + qualify
- deduplicate
- remove obvious mismatches
- verify important fields
- create useful human-facing categories
- score/segment leads using explicit criteria
- keep reasons for inclusion/exclusion

### Phase 4 — Structured delivery
For Persian list/spreadsheet output:
- use `structured-data-output`
- preserve approved field order
- use RTL
- number rows continuously
- center structured data by default
- keep visual theme flexible by project

### Phase 5 — Marketing output
Use the appropriate Marketing Skill:
- prospecting
- competitor profiling
- content
- cold email
- sales enablement
- pricing
- SEO
- ads
- other relevant skill

### Phase 6 — Human checkpoint
Before real outbound contact, bulk messaging, ad spend, or publication:
- show the user the proposed audience/output
- require approval unless a pre-approved automation policy exists

### Phase 7 — Measure
Track:
- number discovered
- duplicate rate
- valid-contact rate
- qualified-lead rate
- manual-review acceptance rate
- downstream response/conversion metrics when available
- cost/time per useful result

## Validation protocol

Start with a **small pilot**, not a full automation.

Recommended first test:
- one city/area
- one business category
- 20–50 records
- no automated outreach

Manually inspect a meaningful sample and compare the pipeline against reality.

## Pass criteria

Automation should not scale until it demonstrates:
- stable data collection
- deterministic cleaning/deduplication
- acceptable classification/qualification quality
- useful structured output
- useful marketing output
- clear logging and recovery behavior

## Safety / quality boundaries

- Do not auto-send outreach during initial tests.
- Do not fabricate personalization.
- Do not treat scraped contact data as consent for marketing.
- Preserve opt-out/compliance requirements when outreach is later enabled.
- Do not scale a broken workflow; fix the pilot first.
