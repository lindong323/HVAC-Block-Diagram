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
        O[Condenser Fan]
        OP[Oil Pump]
        OH[Oil Heater]
        OF[Oil Filter]
        OR[Oil Reservoir]
        OS[Oil Separator]
        OC[Oil Cooler]
        EJ[Ejector]
    end

    A[Power Supply] -->|Supplies power| B
    B -->|Controls speed| C
    C -->|Powers| D
    D -->|Drives| E
    E -->|Compresses refrigerant| F
    F -->|Condenses refrigerant| G
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
    F -->|Facilitates heat removal| O[Condenser Fan]
    O -->|Cools refrigerant| F
    
    OP -->|Pumps oil| OH
    OH -->|Heats oil| OF
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

%% Notes
    %% Some equipment/components could be optional depending on different chiller types. For example:
    %% Economizer: May not be present in all chillers.
    %% Thermal Storage Tank: Used only in systems with thermal storage needs.
    %% Oil Heater, Oil Filter, Oil Separator, Ejector: Dependent on the specific compressor and system design.
    %% Vibration Dampers, Flow Switches, Pressure Gauges, Relief Valves, Strainers, Temperature Sensors, Pressure Sensors: These components are essential for monitoring and protection but may vary in type and presence depending on the specific chiller design and application.
    %% Water Treatment System: Critical for maintaining water quality, especially in large systems, but might be integrated or external depending on the setup.
    %% VFD for Pumps: Optional depending on the system's energy efficiency requirements.
