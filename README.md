```mermaid
graph LR
    A[Incoming message] --> B[MiniLM-L6-v2 №1<br>Toxicity gate]
    
    B -- Not toxic --> C[✅ Passes through]
    B -- Toxic --> D[MiniLM-L6-v2 №2<br>Target classifier]
    
    D -- Personnel --> E[Pool A — 40 placeholders]
    D -- Self --> F[Pool B — 40 placeholders]
    D -- System --> G[Pool C — 40 placeholders]
    
    E --> H[🔄 Message replaced<br>2–12ms total]
    F --> H
    G --> H
