```mermaid
---
title: ACCC Estimate Process
---
flowchart LR
    A[Dentist Identifies Treatment] --> B(DA Plans Treatment in PP);
    B --> C(Admin 'Checks Out' Plan in PP);
    C --> D(Submit Pre-Auth Electronically);
    D --> E{EOB Received Immediately?};
    E -- Yes --> F[Review EOB];
    F --> G[Adjust Amounts in PP Ledger];
    G --> H[Print Estimate];
    H --> I[Present Estimate to Patient];
    I --> J{Patient Agrees?};
    J -- Yes --> K[Book Appointment];
    J -- No --> L[End Process];
    E -- No --> M[Print Estimate - Insurance Unconfirmed];
    M --> I;