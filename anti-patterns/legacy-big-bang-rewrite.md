# Anti‑Pattern: Big‑Bang Rewrite

## Problem
Attempting to replace the entire lending platform in a single release.

## Why It Happens
- Pressure to “modernize everything at once”
- Underestimation of legacy complexity
- Lack of domain decomposition

## Impact
- Multi‑year delays
- High program failure risk
- No incremental business value

## Recommended Pattern
Use the **Loan Origination Strangler Pattern** and migrate capabilities incrementally.
