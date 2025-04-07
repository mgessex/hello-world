```mermaid
graph TD
    A[Procedure Completed] --> B(RDA Enters Codes in Power Practice);
    B --> C(Patient Checkout with Admin);
    C --> D{Submit Electronically via CDA Net};
    D -- Success --> E{EOB Received Immediately?};
    D -- Failed --> F[Go to Manual Billing Process];
    E -- Yes --> G[Review EOB and Calc Patient Portion];
    G --> H[Collect Patient Payment];
    H --> I[Receive Insurance Payment Later];
    I --> J[Apply Payments in Power Practice];
    E -- No --> K[Wait for Insurance Payment/Details];
    K --> L[Apply Insurance Payment in Power Practice];
    L --> M[Calculate Patient Portion];
    M --> N[Send Statement to Patient];
    N --> O[Patient Pays Balance];
    O --> J;