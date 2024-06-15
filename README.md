# Water-Cooled Chiller Functional System Block Diagram

```mermaid
graph TD
    A[Electrical System] --> B[Compressor System]
    B --> C[Lubrication System]
    C --> D[Evaporator System]
    D --> E[Condenser System]
    E --> F[Refrigerant Circuit]
    F --> G[Economizer]
    G --> H[Purge System]
    H --> I[Control System]

