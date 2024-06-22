```mermaid

graph TD
    A[Oil Sump] -->|Stores Oil| B[Oil Pump]
    B -->|Discharges Oil| C[Oil Filter]
    C -->|Filtered Oil| D[Heat Exchanger]
    D -->|Cooled Oil| E[Compressor Bearings]
    E -->|Drains Oil| A
    A -->|Heated Oil| F[Oil Heater]
    F --> A
    A -->|Cooled Oil| G[Oil Cooler]
    G --> D
    A -->|Oil Level Indicator| H[Sight Glass]
    B -->|Suction Oil| I[Suction Port]
    I --> B
    B -->|Discharge| J[Discharge Hose]
    J --> D
    A -->|Draws Discharge Gas| K[Eductor]
    K -->|Siphons Oil| L[Evaporator]
    L --> K
    K -->|Returns Oil| A
    A -->|Pressure Measurement| M[Oil Pressure Transducer]
    B -->|Speed Control| N[VSD]
    N --> B
    D -->|Temperature Control| O[AXV Valve]
    O --> D
    F -->|Monitors Temperature| P[Temperature Sensor]
    P --> F
    G -->|Monitors Temperature| Q[Temperature Sensor]
    Q --> G
