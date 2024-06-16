# Water-Cooled Chiller Boundary Diagram

```mermaid
graph TD
    A[Power Supply] --> B[Control Panel]
    B --> C[VSD/Soft Starter]
    C --> D[Motor]
    D --> E[Compressor]
    E --> F[Condenser]
    F --> G[Expansion Valve]
    G --> H[Economizer]
    H --> I[Evaporator]
    H --> E
    I --> J[Chilled Water Pump]
    J --> K[Air Handling Unit]
    K --> I
    J --> M[Heat Exchanger]
    M --> R[Thermal Storage Pump]
    R --> L[Thermal Storage Tank]
    L --> M
    B --> N[BAS Comms]
    N --> B
    F --> O[Condenser Water Pump]
    O --> P[Cooling Tower]
    P --> F
