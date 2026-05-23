# Lending Domain Event Map

```mermaid
flowchart TD

    subgraph Origination
        O1[LoanApplicationSubmitted]
        O2[ApplicationDataValidated]
        O3[ApplicationEnriched]
    end

    subgraph Underwriting
        U1[CreditScorePulled]
        U2[FraudCheckCompleted]
        U3[UnderwritingDecisionMade]
    end

    subgraph Servicing
        S1[PaymentPosted]
        S2[DelinquencyStatusChanged]
        S3[EscrowAdjusted]
    end

    subgraph Collections
        C1[CollectionCaseOpened]
        C2[PromiseToPayRecorded]
        C3[ChargeOffProcessed]
    end

    subgraph Payoff
        P1[PayoffQuoteGenerated]
        P2[LoanClosed]
    end

    O1 --> O2 --> O3 --> U1 --> U2 --> U3 --> S1 --> S2 --> S3 --> C1 --> C2 --> C3 --> P1 --> P2

