```mermaid
---
title: ACCC Alberta Health Consult Process
---
flowchart LR 
    A[Procedure Completed] --> B(DA Enters Codes in Power Practice);
    B --> C(Patient Checkout with Admin);
    C --> D[Admin Shuts Off Private Insurance, if needed];
    D --> E[Checkout AH Consult in Power Practice];
    E --> F[Print Paper Claim Form];
    F --> G[Manually Enter Claim into Clinic Aid];
    G --> H[Clinic Aid Submits to Alberta Health];
    H --> I[Wait for Payment];
    I --> J[Apply Payment in Power Practice];