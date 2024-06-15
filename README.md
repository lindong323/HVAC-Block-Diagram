# Water-Cooled Chiller Block Diagram

```mermaid
graph TD
    A[Compressor] --> B[Condenser]
    B --> C[Expansion Valve]
    C --> D[Evaporator]
    D --> E[Cooling Tower]
    E --> F[Pumps]
    F --> A
    D --> G[Chilled Water]
    G --> H[Air Handling Unit]
    H --> I[Building Space]
    I --> G
