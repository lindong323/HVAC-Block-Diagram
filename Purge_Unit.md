```mermaid

graph TD
    subgraph Chiller
        A[Condenser]
        B[Evaporator]
        C[Compressor]
        D[Expansion Valve]
        E[Refrigerant Line]
    end
    subgraph PurgeUnit[Purge Unit]
        PU[Compressor/Vacuum Pump]
        SEP[Separator]
        RL[Return Line]
        VL[Vent Line]
    end

    A -->|Gas Extraction Line| PU
    PU --> SEP
    SEP -->|Return Line| E
    SEP -->|Vent Line| VL
