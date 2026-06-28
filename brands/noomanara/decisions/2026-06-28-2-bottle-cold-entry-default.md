---
id: DEC-001
type: decision
brand: noomanara
segment: all
source: "noomanara_session_context_dump.md"
status: locked
confidence: high
author: matt
created: 2026-06-28
tags: [offer-architecture, entry-sku, coherence]
---

# The 2-bottle 60-day pack is the cold-entry default

## Insight
Cold traffic is steered to the 2-bottle £60 60-day pack. It is the smallest SKU that gives a fair 60-day trial, matches the onset and the guarantee window, and asks for lower commitment than the box.

## Why it holds
Offer mechanics must be internally coherent. The guarantee window, the trial length, the product onset, and the entry SKU all point at the same unit: the 2-bottle 60-day pack. A single bottle is 30 days of product, which runs out at the efficacy trough and cannot carry a 60-day trial or guarantee. The box is too much commitment for a cold buyer.

## So what
PDP and email position the 2-bottle pack as the recommended trial, the single bottle as a price trade-down, and the box as best value and upgrade. Three SKUs: single £35, double £60, hero £85, all shipped as one parcel.

## To validate
Locked, but the cold default is the dominant validation target. Smoke-test the three defaults head-to-head, net of AOV (FIN-002).
