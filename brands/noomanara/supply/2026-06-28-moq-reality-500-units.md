---
id: SUP-001
type: decision
brand: noomanara
segment: all
source: "call_-_12-06-26 + Potential_suppliers"
status: locked
confidence: high
author: matt
created: 2026-06-28
tags: [moq, inventory, budget-floor, custom-formula]
---

# MOQ floor is 500 units, not 150

## Insight
Custom formulations from UK manufacturers carry MOQs of roughly 500 units, not the original 150-unit planning assumption. At about £6.50 per unit that is around £3,250 for a first batch, which consumes most of the inventory budget.

## Why it holds
Supplier responses, Supplement Factory in particular, confirmed the 500-unit floor. The financial model was rebuilt from this floor rather than patched.

## So what
The model is built from the 500-unit floor. This is the constraint that pushes toward the stock-formula route for validation (SUP-002) and was a driver of the budget rebuild (FIN-001). It also raises the open question of whether ad spend must rise to clear a larger initial stock position.

## To validate
Locked as a planning floor. Confirm exact MOQ and unit cost per chosen supplier with a costed quote at 500-unit MOQ.
