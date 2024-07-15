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
        FD[Filter-drier]
        SG[Sight Glass]
        G[Expansion Valve]
        H[Economizer]
        I[Evaporator]
        O[Condenser Fan with VSD]
        OP[Oil Pump]
        OF[Oil Filter]
        OR[Oil Sump]
        OS[Oil Separator]
        OC[Oil Cooler]
        EJ[Ejector]
        ED[Eductor]
    end

    A[Power Supply] -->|Supplies power| B
    B -->|Controls speed| C
    C -->|Powers| D
    D -->|Drives| E
    E -->|Compresses refrigerant| F
    F -->|Condenses refrigerant| FD
    FD -->|Filters refrigerant| SG
    SG -->|Monitors refrigerant| G
    G -->|Regulates flow| H
    H -->|Enhances efficiency| E
    H -->|Enhances efficiency| I
    I -->|Evaporates refrigerant| E
    I -->|Provides chilled water| J[Chilled Water Pump]
    J -->|Circulates chilled water| K[Air Handling Unit]
    K -->|Returns warm water| I
    J -->|Transfers heat| M[Heat Exchanger]
    M -->|Pumps heat transfer fluid| R[Thermal Storage Pump]
    R -->|Stores cold fluid| L[Thermal Storage Tank]
    L -->|Returns fluid| M
    M -->|Transfers chilled water| I
    B -->|Communicates with| N[BAS Comms]
    N -->|Receives commands| B
    F -->|Facilitates heat removal| O
    O -->|Cools refrigerant| F
    
    OP -->|Pumps oil| OF
    OF -->|Filters oil| OC
    OC -->|Cools oil| E
    E -->|Stores oil| OR
    OR -->|Supplies oil| OP
    E -->|Separates oil| OS
    OS -->|Ejects oil| EJ
    EJ -->|Returns oil| OP
    I -->|Reclaims oil| ED
    ED -->|Returns oil| OR

    %% Style for nodes outside the subgraph
    style A fill:#ffcccc,stroke:#333,stroke-width:2px
    style J fill:#ffcccc,stroke:#333,stroke-width:2px
    style K fill:#ffcccc,stroke:#333,stroke-width:2px
    style M fill:#ffcccc,stroke:#333,stroke-width:2px
    style R fill:#ffcccc,stroke:#333,stroke-width:2px
    style L fill:#ffcccc,stroke:#333,stroke-width:2px
    style N fill:#ffcccc,stroke:#333,stroke-width:2px

