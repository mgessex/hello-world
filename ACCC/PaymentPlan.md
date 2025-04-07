```mermaid
graph TD
    A[Patient Agrees to Payment Plan] --> B(Patient Pays 50% Upfront);
    B --> C[Admin Applies Initial Payment in PP];
    C --> D[Admin Records Patient on Spreadsheet];
    D --> E[Provide Initial Statement & Instructions];
    E --> F{Loop Until Paid or 6 Months};
    F -- Payment Made --> G[Patient Makes Payment];
    G --> H[Admin Identifies Payment e.g. iProc];
    H --> I[Admin Applies Payment in PowerPractice];
    I --> J[Mail Updated Statement];
    J --> F;
    F -- 6 Months & Unpaid --> K[Go to Collections Process];
    F -- Fully Paid --> L[End Process];