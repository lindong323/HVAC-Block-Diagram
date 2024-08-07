# Water-Cooled Chiller Boundary Diagram

```mermaid
graph TD
    subgraph watercooledchiller[Water-Cooled Chiller]
        style watercooledchiller stroke-dasharray: 5 5
        B[Control Panel]
        C[VSD/Soft Starter]
        D[Motor]
        E[Compressor]
        F[Condenser]
        FD[Filter-Drier]
        SG[Sight Glass]
        G[Expansion Valve]
        H[Economizer]
        I[Evaporator]
        OP[Oil Pump]
        OF[Oil Filter]
        OR[Oil Sump with Oil Heater]
        OS[Oil Separator]
        OC[Oil Cooler]
        EJ[Ejector]
        PU[Purge Unit]
    end

    A[Power Supply] -->|Supplies power| B
    B -->|Controls speed| C
    C -->|Powers| D
    D -->|Drives| E
    E -->|Increases pressure| F
    F -->|Condenses refrigerant| FD
    FD -->|Filters refrigerant| SG
    SG -->|Provides visual inspection| G
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
    F -->|Circulates condenser water| O[Condenser Water Pump]
    O -->|Transfers heat| P[Cooling Tower]
    P -->|Cools water| F
    F -->|Removes non-condensables| PU
    
    OP -->|Pumps oil| OF
    OF -->|Filters oil| OC
    OC -->|Cools oil| E
    E -->|Stores oil| OR
    OR -->|Supplies oil| OP
    E -->|Separates oil| OS
    OS -->|Ejects oil| EJ
    EJ -->|Returns oil| OP

    %% Style for nodes outside the subgraph
    style A fill:#ffcccc,stroke:#333,stroke-width:2px
    style J fill:#ffcccc,stroke:#333,stroke-width:2px
    style K fill:#ffcccc,stroke:#333,stroke-width:2px
    style M fill:#ffcccc,stroke:#333,stroke-width:2px
    style R fill:#ffcccc,stroke:#333,stroke-width:2px
    style L fill:#ffcccc,stroke:#333,stroke-width:2px
    style N fill:#ffcccc,stroke:#333,stroke-width:2px
    style O fill:#ffcccc,stroke:#333,stroke-width:2px
    style P fill:#ffcccc,stroke:#333,stroke-width:2px
