# Core Lending Modernization Patterns

This repository provides architectural patterns, modernization frameworks, and integration standards used in large‑scale lending transformation programs. The assets support the transition from legacy lending platforms to modular, cloud‑aligned, API‑driven architectures that improve scalability, auditability, and regulatory alignment.

---

## Modernization Architecture Overview

```mermaid
flowchart LR
    subgraph Channels
        DChannels[Digital Channels]
        Branch[Branch / RM]
        Contact[Contact Center]
    end

    subgraph ExperienceAPIs
        ExpLend[Experience API - Lending]
    end

    subgraph ProcessAPIs
        ProcOrig[Process API - Origination]
        ProcServ[Process API - Servicing]
        ProcColl[Process API - Collections]
    end

    subgraph SystemAPIs
        SysCore[System API - Core Lending]
        SysCRM[System API - CRM]
        SysGL[System API - GL]
        SysRisk[System API - Risk]
    end

    subgraph Legacy
        ALS[Legacy Core (ALS200/171)]
        Mainframe[Mainframe Services]
        Batch[Batch Jobs]
    end

    DChannels --> ExpLend
    Branch --> ExpLend
    Contact --> ExpLend

    ExpLend --> ProcOrig
    ExpLend --> ProcServ
    ExpLend --> ProcColl

    ProcOrig --> SysCore
    ProcServ --> SysCore
    ProcColl --> SysCore

    SysCore --> ALS
    SysCore --> Mainframe
    SysCore --> Batch

    SysCRM --> CRM[(CRM)]
    SysGL --> GL[(General Ledger)]
    SysRisk --> Risk[(Risk Engine)]
