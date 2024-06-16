```markdown
# Block Diagram Project

## Overview

This project contains block diagrams for HVAC systems, including Water-Cooled Chiller and Air-Cooled Chiller systems. The diagrams are created using Mermaid syntax to visually represent the components and their connections within these systems.

## Table of Contents

- [Overview](#overview)
- [Block Diagrams](#block-diagrams)
  - [Water-Cooled Chiller Diagram](#water-cooled-chiller-diagram)
  - [Air-Cooled Chiller Diagram](#air-cooled-chiller-diagram)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Block Diagrams

### Water-Cooled Chiller Diagram

```mermaid
graph TD
    subgraph watercooledchiller[Water-Cooled Chiller]
        style watercooledchiller stroke-dasharray: 5 5
        B[Control Panel]
        C[VSD/Soft Starter]
        D[Motor]
        E[Compressor]
        F[Condenser]
        G[Expansion Valve]
        H[Economizer]
        I[Evaporator]
        OP[Oil Pump]
        OH[Oil Heater]
        OF[Oil Filter]
        OR[Oil Reservoir]
        OS[Oil Separator]
        EJ[Ejector]
    end

    A[Power Supply] --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H
    H --> E
    H --> I
    I --> E
    I --> J[Chilled Water Pump]
    J --> K[Air Handling Unit]
    K --> I
    J --> M[Heat Exchanger]
    M --> R[Thermal Storage Pump]
    R --> L[Thermal Storage Tank]
    L --> M
    M --> I
    B --> N[BAS Comms]
    N --> B
    F --> O[Condenser Water Pump]
    O --> P[Cooling Tower]
    P --> F
    
    OP --> OH
    OH --> OF
    OF --> E
    E --> OR
    OR --> OP
    E --> OS
    OS --> EJ
    EJ --> OP

    %% Style for nodes outside the subgraph
    style A fill:#ffcccc,stroke:#333,stroke-width:2px
    style J fill:#ffcccc,stroke:#333,stroke-width:2px
    style K fill:#ffcccc,stroke:#333,stroke-width:2px
    style M fill:#ffcccc,stroke:#333,stroke-width:2px
    style R fill:#ffcccc,stroke:#333,stroke-width:2px
    style L fill:#ffcccc,stroke:#333,stroke-width:2px
    style N fill:#ffcccc,stroke:#333,stroke-width:2px
    style O fill:#ffcccc,stroke:#333,stroke-width:2px
    style P fill:#ffcccc,stroke:#333,stroke-width:2px
```

### Air-Cooled Chiller Diagram

```mermaid
graph TD
    subgraph aircooledchiller[Air-Cooled Chiller]
        style aircooledchiller stroke-dasharray: 5 5
        B[Control Panel]
        C[VSD/Soft Starter]
        D[Motor]
        E[Compressor]
        F[Condenser]
        G[Expansion Valve]
        H[Economizer]
        I[Evaporator]
        O[Condenser Fan]
        OP[Oil Pump]
        OH[Oil Heater]
        OF[Oil Filter]
        OR[Oil Reservoir]
        OS[Oil Separator]
        EJ[Ejector]
    end

    A[Power Supply] --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H
    H --> E
    H --> I
    I --> E
    I --> J[Chilled Water Pump]
    J --> K[Air Handling Unit]
    K --> I
    J --> M[Heat Exchanger]
    M --> R[Thermal Storage Pump]
    R --> L[Thermal Storage Tank]
    L --> M
    M --> I
    B --> N[BAS Comms]
    N --> B
    F --> O
    O --> F
    
    OP --> OH
    OH --> OF
    OF --> E
    E --> OR
    OR --> OP
    E --> OS
    OS --> EJ
    EJ --> OP

    %% Style for nodes outside the subgraph
    style A fill:#ffcccc,stroke:#333,stroke-width:2px
    style J fill:#ffcccc,stroke:#333,stroke-width:2px
    style K fill:#ffcccc,stroke:#333,stroke-width:2px
    style M fill:#ffcccc,stroke:#333,stroke-width:2px
    style R fill:#ffcccc,stroke:#333,stroke-width:2px
    style L fill:#ffcccc,stroke:#333,stroke-width:2px
    style N fill:#ffcccc,stroke:#333,stroke-width:2px
```

## Installation

1. Clone the repository to your local machine:
    ```sh
    git clone https://github.com/yourusername/block-diagram-project.git
    ```

2. Navigate to the project directory:
    ```sh
    cd block-diagram-project
    ```

## Usage

Open the `README.md` file in any Markdown viewer that supports Mermaid to visualize the block diagrams. You can also use online Mermaid editors such as [Mermaid Live Editor](https://mermaid-js.github.io/mermaid-live-editor/) to view and edit the diagrams.

## Contributing

Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch: `git checkout -b my-feature-branch`.
3. Make your changes and commit them: `git commit -m 'Add new feature'`.
4. Push to the branch: `git push origin my-feature-branch`.
5. Create a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
```

Feel free to modify the content according to your project's specific requirements and details.
