```mermaid
graph TD
    title[Pareto Chart by Failure Frequency]
    style title fill:#f9f,stroke:#333,stroke-width:4px
    
    A[Sensor Issues] --> |31| B[Communication/Control Issues]
    B --> |18| C[Electrical Components]
    C --> |14| D[Valve Problems]
    D --> |12| E[Mechanical Components]
    E --> |11| F[Refrigerant Problems]
    F --> |10| G[Oil-related Issues]
    G --> |9| H[Alarm Triggers]
    H --> |8| I[Water Flow Problems]
    I --> |7| J[Insulation Degradation]
    J --> |4| K[End]
    
    L[0%] --> M[24.4%] --> N[38.6%] --> O[49.6%] --> P[59.1%] --> Q[67.7%] --> R[75.6%] --> S[82.7%] --> T[89.0%] --> U[94.5%] --> V[100%]
