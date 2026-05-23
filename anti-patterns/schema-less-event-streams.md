# Anti‑Pattern: Schema‑Less Event Streams

## Problem
Events are published without a governed schema.

## Why It Happens
- Rapid delivery pressure
- No schema registry

## Impact
- Breaking changes
- Downstream failures
- Poor auditability

## Recommended Pattern
Adopt the **Lending Domain Event Pattern** with versioned schemas.
