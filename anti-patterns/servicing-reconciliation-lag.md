# Anti‑Pattern: Servicing Reconciliation Lag

## Problem
Servicing updates are reconciled days later due to batch processes.

## Why It Happens
- Legacy servicing cores
- No real‑time data capture

## Impact
- Incorrect delinquency status
- Poor collections performance
- Customer experience issues

## Recommended Pattern
Use the **Loan Servicing CDC Pattern** to publish real‑time servicing events.
