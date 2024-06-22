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
        OC[Oil Cooler]
        OF[Oil Filter]
        OR[Oil Reservoir]
        OS[Oil Separator]
        EJ[Ejector]
        ED[Eductor]
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
    F --> O[Condenser Water Pump]
    O --> P[Cooling Tower]
    P --> F
    
    OP --> OH
    OP --> OC
    OH --> OF
    OC --> OF
    OF --> E
    E --> OR
    OR --> OP
    E --> OS
    OS --> EJ
    EJ --> OP
    EJ --> ED

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

## Notes

- Some equipment/components could be optional depending on different chiller types. For example:
  - **Economizer**: May not be present in all chillers.
  - **Thermal Storage Tank**: Used only in systems with thermal storage needs.
  - **Oil Heater, Oil Cooler, Oil Filter, Oil Separator, Ejector, Eductor**: Dependent on the specific compressor and system design.
  - **Vibration Dampers, Flow Switches, Pressure Gauges, Relief Valves, Strainers, Temperature Sensors, Pressure Sensors**: These components are essential for monitoring and protection but may vary in type and presence depending on the specific chiller design and application.
  - **Water Treatment System**: Critical for maintaining water quality, especially in large systems, but might be integrated or external depending on the setup.
  - **VFD for Pumps**: Optional depending on the system's energy efficiency requirements.
