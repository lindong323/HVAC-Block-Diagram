# Water-Cooled Chiller Boundary Diagram

```mermaid
graph TD
    A[Power Supply] --> B[Power Delivery / Control Panel]
    B --> C[VSD (VFD) / Soft Starter]
    C --> D[Motor]
    D --> E[Compressor]
    E --> F[Condenser]
    F --> G[Expansion Valve]
    G --> H[Economizer (Optional)]
    H --> I[Evaporator]
    E -.-> I
    I --> J[Chilled Water Pump]
    J --> K[Air Handling Unit]
    J --> L[Thermal Storage Tank (Optional)]
    L -.-> M[Heat Exchanger (Optional)]
    M -.-> I
    A -.-> N[BAS Comms]
    F --> O[Cooling Tower]
    O --> P[Condenser Water Pump]
    P -.-> F
