# Sequence Diagram

Example using a sequence diagram in a markdown file.

#### Sequence
::: mermaid
sequenceDiagram
participant Client1 as Application
participant Manager1 as Manager
participant Engine1 as Engine
participant Accessor1 as Accessor 1
participant Accessor2 as Accessor 2
participant Accessor3 as Accessor 3
participant Utility1 as Queue Utility

    Client1->>Manager1: Action
    
    Manager1->>+Engine1: Process

    Engine1->>+Accessor1: Get Items
    Accessor1->>-Engine1: Return Items

    Engine1->>+Accessor2: Get Details
    Accessor2->>-Engine1: Return Details

    Engine1->>+Accessor3: Get Status
    Accessor3->>-Engine1: Return Status

    Engine1->>+Accessor2: Store Details
    Accessor2->>-Engine1: Return

    Engine1->>-Manager1: Return Details

    Manager1-->Utility1: Queue message

    Manager1->>Client1: Return
:::