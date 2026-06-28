---
id: LEG-003
type: decision
brand: noomanara
segment: all
source: "memory + brand1_validation_launch_bible.html"
status: validated
confidence: high
author: matt
created: 2026-06-28
tags: [vesting, drift, source-audit, sha]
---

# The launch bible's vesting terms differ from the agreed terms

## Insight
The launch bible's stated vesting terms contain a discrepancy from the agreed terms. Source documents must be audited for internal consistency before being treated as authoritative.

## Why it holds
A document treated as the canonical bible carried terms that do not match what was agreed. This is the same drift pattern as the stale formula (PRD-001): a source doc presenting outdated or incorrect terms as current.

## So what
Audit the launch bible and any equity-bearing doc against the agreed SHA terms before either is shared or signed. Correct the bible. This is exactly why the repo references canonical sources rather than trusting any single document.

## To validate
Validated as a finding. The action is the correction and the consistency check.
