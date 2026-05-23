# Core‑to‑Modern Coexistence Architecture

```mermaid
flowchart LR

    %% Legacy Core
    subgraph LegacyCore[Legacy Core Banking]
        L1[(COBOL System)]
        L2[(Legacy DB)]
        L3[Batch Jobs]
    end

    %% CDC Layer
    subgraph CDC[CDC & Data Capture Layer]
        C1[Log-Based CDC Engine]
        C2[Change Events Stream]
    end

    %% Modern Platform
    subgraph ModernPlatform[Modern Event-Driven Platform]
        M1[(Kafka Topics)]
        M2[Event Enrichment Service]
        M3[Domain Microservices]
        M4[API Gateway]
    end

    %% Downstream Consumers
    subgraph Consumers[Downstream Consumers]
        D1[Servicing Microservices]
        D2[Underwriting Engine]
        D3[Fraud & Risk Models]
        D4[Customer 360 Platform]
        D5[Analytics & Reporting]
    end

    %% Strangler Façade
    subgraph Strangler[Strangler Façade]
        S1[Routing Layer]
        S2[Modern APIs]
    end

    %% Flows
    L2 --> C1 --> C2 --> M1
    M1 --> M2 --> M3
    M3 --> D1
    M3 --> D2
    M3 --> D3
    M3 --> D4
    M3 --> D5

    %% Dual Write / Read
    S1 --> L1
    S1 --> S2
    S2 --> M3

    %% Notes
    classDef legacy fill:#f4cccc,stroke:#b30000,stroke-width:1px;
    classDef modern fill:#d9ead3,stroke:#38761d,stroke-width:1px;
    classDef cdc fill:#cfe2f3,stroke:#1155cc,stroke-width:1px;
    classDef consumers fill:#fff2cc,stroke:#bf9000,stroke-width:1px;

    class L1,L2,L3 legacy;
    class C1,C2 cdc;
    class M1,M2,M3,M4 modern;
    class D1,D2,D3,D4,D5 consumers;

```

## Summary

This coexistence architecture enables progressive modernization of legacy core banking systems without disrupting business operations. It uses:

- **CDC (Change Data Capture)** to stream real-time changes from legacy cores  
- **Event-driven architecture** to power underwriting, servicing, fraud, and analytics  
- **Strangler façade** to gradually shift traffic from legacy APIs to modern microservices  
- **Dual-write and dual-read patterns** during migration  
- **Canonical events** to unify data models across lending domains  

This model was used to modernize 77+ legacy lending applications and forms the foundation for the Core Lending Modernization Patterns library.

