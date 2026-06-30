---
id: FIN-004
type: decision
brand: noomanara
segment: all
source: "Noomanara_Budget_Model_v42.xlsx + brand1_validation_launch_bible.html audit"
status: validated
confidence: high
author: matt
created: 2026-06-30
tags: [budget, ring-fence, drift-flag, ad-spend, reconciliation]
---

# Brand 1 ring-fence reconciled to £9,800 (was stated as £7,570 in the bible)

## Insight
The launch bible's headline budget figures predated the v4.2 rebuild and were wrong on two counts:

- **Total ring-fence:** bible said £7,570. The v4.2 model's actual derivation is £11,500 total founder investment minus £2,000 Brand 2 ring-fence (DEC-006) = **£9,500** Brand 1 envelope (£4,928 one-time setup + £1,115 tech pre-fund + £3,457 90-day ad spend, Settings rows 8, 9, 57, 78–92, 103–106).
- **90-day ad spend:** bible said £2,500. The model and the reconciled media plan (v2.1) both confirm **£3,457** (£501 / £899 / £1,279 / £778 across M1–4).
- Plus a **£300 smoke-test spend** (see DEC-002, DEC-004), agreed verbally but never carried into the v4.2 model. Additive to the £9,500 envelope, bringing the live total to **£9,800**.

## Why it holds
The bible's £7,570 figure was built on the pre-v4.2 assumptions: 150-unit MOQ at £6.50/unit (£975, not £2,500) and an unreconciled £2,500 ad-spend placeholder that never matched the media plan's own £3,457 test total. Both were silently inconsistent with the canonical sources (Budget Model v4.2, media plan v2.1) the rest of the repo treats as authoritative.

## So what
The bible's Budget Timing table (§13), decision D4, the front-page "ring-fenced" tag, the daily ad-spend pacing references, and the tech-stack table's Meta Ads line have all been corrected to £9,800 / £3,457 / £300 in the bible directly (2026-06-30 edit).

## Drift flag
The £300 smoke-test spend is not yet a line item in Budget Model v4.2. The model's setup-cost block (Settings rows 78–91) and 90-day ad-spend total (row 57) should be updated to include it, or the £9,800 figure in the bible will quietly drift from the model again the next time v4.2 is touched.

## To validate
Validated against the model's own cells. Open: add the £300 smoke-test line to Budget Model v4.2 so the two sources stay reconciled.