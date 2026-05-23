# Event‑Driven Lending Flow

```mermaid
flowchart LR

    A[Loan Application Submitted] --> B[Fraud Check Triggered]
    B --> C[Credit Bureau Pull]
    C --> D[Underwriting Rules Engine]
    D --> E[Underwriting Decision Published]

    E -->|Approved| F[Loan Boarding Service]
    E -->|Declined| G[Customer Notification]

    F --> H[(Kafka - LoanLifecycleEvents)]
    H --> I[Servicing System]
    H --> J[Analytics & Risk Platform]
