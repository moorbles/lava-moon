---
id: FIN-004
type: decision
brand: noomanara
segment: all
source: "noomanara_session_context_dump.md"
status: validated
confidence: high
author: matt
created: 2026-06-28
tags: [gate, statistics, leading-indicators, repeat-rate]
---

# The 90-day repeat-rate gate is underpowered

## Insight
The 90-day gate rests on repeat purchase rate, but the cohort with a full 60-day window at the gate is tiny, around 8 customers in the base case. A 25 percent versus 30 percent repeat rate cannot be distinguished at that n.

## Why it holds
Small-n makes the retention read noisy. The machine read sits on a larger base and is both more reliable and more strategically central.

## So what
Treat the 90-day repeat number as directional. Shift the gate toward leading indicators: checkout subscribe rate, second-order rate of the earliest cohort, CPA trend, creative win rate. Weight the decision toward the machine verdict, treat retention as directional. This is the scaffold for the no-deviation playbook gate (DEC-quadrant).

## To validate
Validated as a design correction. Build the gate on leading indicators.
