---
id: DEC-002
type: decision
brand: noomanara
segment: all
source: "session 2026-06-30"
status: locked
confidence: high
author: matt
created: 2026-06-30
tags: [terminology, drift-flag, validation, smoke-test, sku-test]
---

# "Smoke test" means the fake-door test, not the live SKU test

## Insight
Two different tests had collapsed into one label. They are now split:

- **Smoke test** = a pre-inventory, no-real-sale purchase-intent check: waitlist, "coming soon" page, or fake-door product page. Run before committing inventory. Origin: context dump, blind-spot question 2.
- **SKU test** (aka **cold-default test**) = the live, paid-traffic, real-sale test in Phase 4 that runs single vs 2-bottle vs box head-to-head, net of AOV, to settle the cold-entry mix. This requires stock in hand and is not a smoke test by definition.

## Why it holds
A smoke test by definition takes no real sale. The Phase 4 SKU comparison takes real orders against real stock, so calling it a "smoke test" misdescribes what it is and when it can run. The two tests also sit at different gates: the smoke test belongs before the Week 5 production order / inventory commitment, the cold-default test belongs in Phase 4 (Weeks 13–16) after stock arrives.

## So what
- Repo and documents should use "smoke test" only for the fake-door / waitlist mechanism, pre-inventory.
- Repo and documents should use "SKU test" or "cold-default test" for the live single vs double vs hero comparison in Phase 4.
- FIN-002 and DEC-001 currently use "smoke test" to mean the cold-default test — these need updating to the corrected terminology.
- The launch bible's Week 12 readiness gate is a launch-readiness gate, not a smoke test, and should not be referred to as one.
- This is the fourth live drift flag in the repo, alongside: magnesium claims spine, five-ingredient legacy documents, and launch bible vesting terms.

## To validate
N/A — this is a terminology correction, not an open assumption. Open item: decide whether a standalone fake-door smoke test will actually be run pre-inventory, since the current plan (Weeks 0–12) has no explicit waitlist/coming-soon step before the Week 5 production order.
