# Google Maps Scraper Kit — Diaco Reference

## Source

Repository: `Mahanaicoach/google-maps-scraper-kit`  
URL: https://github.com/Mahanaicoach/google-maps-scraper-kit  
Default branch: `master`  
License: MIT  
Upstream engine: `gosom/google-maps-scraper` (MIT)

## Diaco role

**Priority Local Business Data / Lead Generation Tool**

Use this tool when a Diaco/Jarvis workflow needs structured public business-listing data from Google Maps, such as:
- business name
- category
- address
- phone
- website
- rating
- review count
- coordinates
- optional email/social links when available

## Typical Diaco/Jarvis uses

- finding suppliers in a city or region
- building a local-business prospect list
- market research
- competitor discovery
- enriching CRM/contact lists
- finding stores, workshops, distributors, service providers, or other local businesses
- exporting results for later filtering, ranking, outreach, or analysis

## Operating policy

The user expects **light / non-heavy use**.

Default operating posture:
- small, targeted queries
- one job at a time
- conservative depth
- avoid repeated high-volume scheduled runs unless explicitly needed
- verify important business data before relying on it operationally

## Data handling

Treat extracted contact data as business/contact data that may be regulated depending on jurisdiction and use case.

Do not:
- assume scraped data is always current
- automatically send bulk outreach without a separate user-approved workflow
- treat results as authoritative without verification
- expose collected contact data publicly without a reason

## Relationship to Jarvis

Jarvis may use this as a business-discovery/data-gathering capability, for example:

> Find industrial equipment suppliers in Tehran and return name, phone, website, address, rating, and review count.

The scraper performs the collection; Jarvis/Diaco can then clean, filter, deduplicate, rank, summarize, and export the results.

## Installation/deployment

The kit supports local Docker-based operation and includes Agent/Claude-oriented commands and skills.

Do not install it into every project by default. Prefer a shared local/server deployment when multiple Diaco/Jarvis projects need the capability.

## Source precedence

This reference records the exact user-selected repository:
`Mahanaicoach/google-maps-scraper-kit`

Do not silently substitute another fork without checking why.
