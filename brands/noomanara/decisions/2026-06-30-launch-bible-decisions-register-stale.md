---
id: DEC-003
type: decision
brand: noomanara
segment: all
source: "brand1_validation_launch_bible.html vs DEC-001, SUP-002, Noomanara_Budget_Model_v42.xlsx"
status: validated
confidence: high
author: matt
created: 2026-06-30
tags: [drift-flag, launch-bible, offer-architecture, moq, source-audit]
---

# The launch bible's decisions register (D2, D5, D6, D9) predates the current offer architecture and MOQ

## Insight
The bible's "Decisions register" section was written before the v4 → v4.2 offer-architecture rebuild and the MOQ confirmation. Four entries are stale:

- **D6 (Pricing & offer architecture):** states only "£35 single unit; contribution must stay ≥£25 (71%)" with no mention of the 2-bottle or hero SKUs. This predates DEC-001 (locked: three SKUs — single £35, double £60, hero £85 — with the 2-bottle pack as the cold-entry default).
- **D2 (Sourcing route):** assumes "Lower MOQ (100–200 units), 4–6 wk lead, ~£4–5/unit." Superseded — see SUP-002, now 500 units at £5/bottle COGS.
- **D5 (Final manufacturer + production order):** says "Place 150 units." Superseded by the same 500-unit figure.
- **D9 (Inventory reorder):** the reorder logic ("reorder only when sell-through justifies it") was written against the smaller batch size and should be re-checked against a 500-unit first order and its longer sell-through runway.

## Why it holds
The decisions register reads as a live, current section of the bible, but it was authored before the offer-architecture and MOQ work that produced v4.2. Treating it as current risks re-litigating settled questions with the wrong numbers, or briefing a supplier or the budget plan off the old figures.

## So what
Correct D2, D5, D6, and D9 in the bible directly:
- D6 → restate as the locked three-SKU architecture (DEC-001): single £35 / double £60 / hero £85, 2-bottle cold-entry default, all one parcel.
- D2 and D5 → restate at 500-unit MOQ, £5/bottle COGS (SUP-002, v4.2 Settings row 26).
- D9 → re-derive reorder logic against the 500-unit batch and the ~232 implied first orders it supports.

This is the fifth live drift flag in the repo, alongside: magnesium claims spine, five-ingredient legacy documents, launch bible vesting terms, and smoke-test terminology (DEC-002).

## To validate
N/A — this is a source-document correction, not an open assumption. The action is editing the bible's decisions register to match DEC-001 and SUP-002.