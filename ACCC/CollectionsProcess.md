```mermaid
---
title: ACCC Collections Process
---
flowchart LR
    A[AR Report Identifies Account >60 Days] --> B(Send Statement 1);
    B --> C[Wait Period];
    C --> D(Send Statement 2);
    D --> E[Wait Period];
    E --> F(Send Statement 3);
    F --> G[Wait Period];
    G --> H[Send 15-Day Collection Warning Letter];
    H --> I[Wait 15 Days];
    I --> J[Submit Account to AHS Collections];