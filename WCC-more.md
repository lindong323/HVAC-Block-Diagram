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
        VD[Vibration Dampers]
        FS[Flow Switches]
        PG[Pressure Gauges]
        RV[Relief Valves]
        ST[Strainers]
        TS[Temperature Sensors]
        PS[Pressure Sensors]
    end

    A[Power Supply] --> B
    B --> C
    C --> D
    D --> E
    D --> VD
    E --> F
    E --> OR
    E --> OS
    F --> G
    F --> O
    F --> PG
    G --> H
    H --> I
    H --> E
    I --> E
    I --> J[Chilled Water Pump]
    I --> FS
    I --> TS
    J --> K[Air Handling Unit]
    K --> I
    J --> M[Heat Exchanger]
    M --> R[Thermal Storage Pump]
    R --> L[Thermal Storage Tank]
    L --> M
    M --> I
    B --> N[BAS Comms]
    N --> B
    OP --> OH
    OH --> OF
    OF --> E
    OR --> OP
    OS --> EJ
    EJ --> OP
    RV --> E
    RV --> F
    ST --> J
    ST --> O
    VFD[VFD for Pumps] --> J
    VFD --> O
    WT[Water Treatment System] --> F
    O --> P[Cooling Tower]
    P --> F
