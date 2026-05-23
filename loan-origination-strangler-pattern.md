# Loan Origination Strangler Pattern

## Problem
Legacy loan origination systems are tightly coupled, slow to change, and difficult to scale.

## Solution
Introduce a strangler façade that routes new loan applications to modern microservices while legacy flows continue to operate.

## Key Steps
- Implement API façade for new loan submissions  
- Use event streaming for underwriting, fraud, and decisioning  
- Gradually migrate product rules and workflows  
- Retire legacy modules incrementally  

## Benefits
- Zero‑downtime modernization  
- Reduced risk during migration  
- Faster delivery of new lending products  
