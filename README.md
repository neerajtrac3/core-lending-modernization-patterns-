# core-lending-modernization-patterns-
Enterprise modernization patterns, canonical models, and integration standards for lending transformation.
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
