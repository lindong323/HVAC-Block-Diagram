```mermaid

graph TD
    A[Oil Sump] -->|Suction Oil| B[Oil Pump]
    B -->|Discharge Oil| C[Oil Filter]
    C -->|Filtered Oil| D[Heat Exchanger]
    D -->|Cooled Oil| E[Compressor Bearings]
    E -->|Drains Oil| A
    A -->|Heated Oil| F[Oil Heater]
    F -->|Return Heated Oil| A
    A -->|Oil to Cooler| G[Oil Cooler]
    G -->|Cooled Oil| D
    A -->|Oil Level Indicator| H[Sight Glass]
    B -->|Suction Port| I[Suction Port]
    I --> B
    B -->|Discharge| J[Discharge Hose]
    J --> D
    A -->|Draws Discharge Gas| K[Eductor]
    K -->|Siphons Oil| L[Evaporator]
    L --> K
    K -->|Returns Oil| A
    A -->|Pressure Measurement| M[Oil Pressure Transducer]
    M -->|Reads Pressure| N[VSD]
    N --> B
    D -->|Temperature Control| O[AXV Valve]
    O -->|Controls Flow| D
    F -->|Monitors Temperature| P[Temperature Sensor]
    P -->|Sends Data| F
    G -->|Monitors Temperature| Q[Temperature Sensor]
    Q -->|Sends Data| G
