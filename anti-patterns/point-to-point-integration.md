# Anti‑Pattern: Point‑to‑Point Integration

## Problem
Each system integrates directly with every other system.

## Why It Happens
- Legacy architecture
- Lack of API gateway or event backbone

## Impact
- Tight coupling
- High maintenance cost
- Fragile change management

## Recommended Pattern
Use **API Gateway + Event Backbone** for decoupled communication.
