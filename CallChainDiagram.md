# Call Chain Diagram

Example using a call chain diagram in a markdown file.

#### Call Chain
::: mermaid
graph TB;

Client1[Application];
Manager1[Manager];
Engine1[Engine];
Accessor1[Accessor 1];
Accessor2[Accessor 2];
Accessor3[Accessor 3];
Data1[(DB)];
Data2[Blob Storage];
Data3[[Queue]];

style Client1 fill:green,color:white
style Manager1 fill:yellow,color:black
style Engine1 fill:orange,color:black
style Accessor1 fill:gray,color:black
style Accessor2 fill:gray,color:black
style Accessor3 fill:gray,color:black
style Data1 fill:blue,color:white
style Data2 fill:blue,color:white
style Data3 fill:blue,color:white

Client1 --> Manager1
Manager1 --> Engine1
Engine1 --> Accessor1
Accessor1 --> Data1
Engine1 --> Accessor2
Accessor2 --> Data2
Engine1 --> Accessor3
Accessor3 --> Data3
:::