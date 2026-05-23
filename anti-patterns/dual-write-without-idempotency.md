# Anti‑Pattern: Dual‑Write Without Idempotency

## Problem
Modern services and legacy cores write to the same data without idempotency controls.

## Why It Happens
- Coexistence phase complexity
- Lack of correlation IDs

## Impact
- Data corruption
- Inconsistent loan states
- Reconciliation failures

## Recommended Pattern
Use **CDC‑based coexistence** with idempotent event processing.
