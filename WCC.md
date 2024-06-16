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
    E -.-> I
    I --> J[Chilled Water Pump]
    J --> K[Air Handling Unit]
    J --> L[Thermal Storage]
    L -.-> M[Heat Exchanger]
    M -.-> I
    A -.-> N[BAS Comms]
    F --> O[Cooling Tower]
    O --> P[Water Pump]
    P -.-> F
