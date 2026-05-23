# Lending Domain Event Pattern

## Purpose
Standardize event structure across loan origination, underwriting, servicing, and collections.

## Event Structure
- eventName  
- loanId  
- customerId  
- timestamp  
- eventAttributes  
- sourceSystem  

## Examples
- LoanApplicationSubmitted  
- UnderwritingDecisionMade  
- PaymentPosted  
- LoanClosed  

## Benefits
- Consistent event modeling  
- Easier integration across domains  
- Strong audit and lineage  
