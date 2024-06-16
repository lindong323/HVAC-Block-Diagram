# Air-Cooled Chiller Boundary Diagram

```mermaid
graph TD
    subgraph aircooledchiller[Air-Cooled Chiller]
        style aircooledchiller stroke-dasharray: 5 5
        B[Control Panel]
        C[VSD/Soft Starter]
        D[Motor]
        E[Compressor]
        F[Condenser]
        G[Expansion Valve]
        H[Economizer]
        I[Evaporator]
        OP[Oil Pump]
        OH[Oil Heater]
        OF[Oil Filter]
        OR[Oil Reservoir]
        OS[Oil Separator]
        EJ[Ejector]
    end

    A[Power Supply] --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H
    H --> E
    H --> I
    I --> E
    I --> J[Chilled Water Pump]
    J --> K[Air Handling Unit]
    K --> I
    J --> M[Heat Exchanger]
    M --> R[Thermal Storage Pump]
    R --> L[Thermal Storage Tank]
    L --> M
    M --> I
    B --> N[BAS Comms]
    N --> B
    F --> O[Condenser Fan]
    O --> F
    
    OP --> OH
    OH --> OF
    OF --> E
    E --> OR
    OR --> OP
    E --> OS
    OS --> EJ
    EJ --> OP

    %% Style for nodes outside the subgraph
    style A fill:#ffcccc,stroke:#333,stroke-width:2px
    style J fill:#ffcccc,stroke:#333,stroke-width:2px
    style K fill:#ffcccc,stroke:#333,stroke-width:2px
    style M fill:#ffcccc,stroke:#333,stroke-width:2px
    style R fill:#ffcccc,stroke:#333,stroke-width:2px
    style L fill:#ffcccc,stroke:#333,stroke-width:2px
    style N fill:#ffcccc,stroke:#333,stroke-width:2px
    style O fill:#ffcccc,stroke:#333,stroke-width:2px
