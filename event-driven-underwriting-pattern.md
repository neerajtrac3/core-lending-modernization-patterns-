# Event‑Driven Underwriting Pattern

## Problem
Underwriting is often synchronous, slow, and dependent on legacy rules engines.

## Solution
Decouple underwriting into asynchronous event‑driven components.

## Event Flow
LoanApplicationSubmitted → FraudCheckCompleted → CreditScorePulled → UnderwritingDecisionMade

## Characteristics
- Stateless underwriting microservices  
- Domain events for each decision step  
- Replayable event history for audit  

## Benefits
- Real‑time decisioning  
- Improved auditability  
- Modular rule updates  
