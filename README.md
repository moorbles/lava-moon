# brand-os

Master store of durable insights from working sessions, structured as a reusable operating system for launching DTC brands. Brand 1 (Noomanara) is the test vehicle. The corpus is built to travel to Brand 2 untouched.

One insight per file, plain markdown, versioned in git. Organised by domain, filtered by frontmatter.

## Why this exists

Insights surface constantly in chats and get lost. Capture was manual and bottlenecked on one person remembering to copy things across. This repo fixes capture, not storage. The mechanism is an end-of-session extraction ritual run by either founder from their own Claude account. See `CONTRIBUTING.md`.

## Structure

```
brands/
  noomanara/
    crm/           retention, churn, lifecycle, onboarding, subscription, email
    audience/      segments, language mining, who they are pre-purchase
    creative/      hooks, angles, naming, comparison assets
    product/       formulation, dosing, format, quality non-negotiables
    supply/        sourcing, MOQ, COAs, manufacturer assessment
    regulatory/    Novel Food, claims law, Meta policy, ASA
    finance/       unit-economics learnings, model assumptions
    legal/         SHA, equity, vesting, partnership
    decisions/     locked cross-domain calls and their reasoning
os-patterns/       cross-brand distillation (the actual OS asset)
templates/         the insight file template
```

Domains are the reusable skeleton. Every DTC brand has these. Brand 2 slots in as `brands/<brand>/` with the same domains.

## Frontmatter schema

```yaml
---
id:         # DOMAIN-style handle, e.g. CRM-001, FIN-003
type:       # positioning | customer | creative-hook | decision | objection
brand:      # noomanara
segment:    # exhausted-professional | perimenopause-processor | performance-male | anxious-functional | all
source:     # provenance
status:     # hypothesis | validated | locked
confidence: # high | medium | low
author:     # matt | isabel
created:    # YYYY-MM-DD
tags: []
---
```

Domain decides the folder. Type, segment, status, and confidence are frontmatter, so you can still pull "every validated customer insight" across domains with a search.

## The canonical-source boundary

This repo captures durable insight that otherwise gets lost. It does not duplicate things that already have a strong home. Four sources stay canonical and are referenced, not copied:

- Gates and decision status: Notion.
- Financial numbers: `Noomanara_Budget_Model_v42.xlsx`.
- Media plan: Notion, operational.
- Customer research and hook banks: `Noomanara_customer_research.html`.

So `finance/` captures the learning and points to the model. `audience/` captures distilled truths and points to the research doc. The repo references canonical sources, never restates them. That boundary is what stops two systems disagreeing later.

## Status discipline

`hypothesis` becomes `validated` only when live data or direct evidence supports it. `validated` becomes `locked` when it is a committed call the brand operates on. The status field is the audit trail of what is actually known versus assumed.

## Drift flags

Where a source document contradicts a locked decision, the relevant insight carries a Drift flag. Current open ones:
- Formula: several docs still show the old five-ingredient stack with magnesium glycinate. Locked formula is four ingredients (PRD-001).
- Claims spine: built on magnesium, which is now cut (REG-002).
- Vesting: launch bible differs from agreed terms (LEG-003).

## Multi-brand path

Brand 2 starts as `brands/<brand>/` with the same domains. Brand-specific insights stay filterable. Anything that proves true across both brands graduates to `os-patterns/`. The OS is what survives any single brand being cut.
