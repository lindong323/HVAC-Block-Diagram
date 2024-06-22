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

    A[Power Supply] -->|Supplies Power| B
    B -->|Controls| C
    C -->|Drives| D
    D -->|Powers| E
    E -->|Compresses Refrigerant| F
    F -->|Condenses Refrigerant| G
    G -->|Regulates Flow| H
    H -->|Enhances Efficiency| E
    H -->|Enhances Efficiency| I
    I -->|Evaporates Refrigerant| E
    I -->|Provides Chilled Water| J[Chilled Water Pump]
    J -->|Circulates Chilled Water| K[Air Handling Unit]
    K -->|Returns Warm Water| I
    J -->|Transfers Heat| M[Heat Exchanger]
    M -->|Pumps Heat Transfer Fluid| R[Thermal Storage Pump]
    R -->|Stores Heat| L[Thermal Storage Tank]
    L -->|Returns Fluid| M
    M -->|Transfers Chilled Water| I
    B -->|Communicates| N[BAS Comms]
    N -->|Receives Commands| B
    F -->|Circulates Condenser Water| O[Condenser Water Pump]
    O -->|Transfers Heat| P[Cooling Tower]
    P -->|Cools Water| F
    
    OP -->|Pumps Oil| OH
    OH -->|Heats Oil| OF
    OF -->|Filters Oil| E
    E -->|Stores Oil| OR
    OR -->|Supplies Oil| OP
    E -->|Separates Oil| OS
    OS -->|Ejects Oil| EJ
    EJ -->|Returns Oil| OP

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
