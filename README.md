# Water-Cooled Chiller Functional System Block Diagram

```mermaid
graph TD
    subgraph Functional_Systems
        style Functional_Systems stroke-dasharray: 5 5
        A[Electrical System]
        B[Compressor System]
        C[Lubrication System]
        D[Evaporator System]
        E[Condenser System]
        F[Refrigerant Circuit]
        G[Economizer]
        H[Purge System]
        I[Control System]
    end
    
    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H
    H --> I
