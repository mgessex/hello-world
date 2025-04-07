```mermaid
graph TD
    A[Procedure/Checkout Completed] --> B(Admin Prints Paper Claim Form);
    B --> C(Patient Signs Form);
    C --> D(Clinic Signs Form);
    D --> E[Mail Form to Insurer/Entity];
    E --> F[Wait for Payment];
    F --> G[Apply Payment in Power Practice];
    G --> H{Patient Portion Remaining?};
    H -- Yes --> I[Send Statement to Patient];
    I --> J[Patient Pays Balance];
    J --> K[Apply Patient Payment in Power Practice];
    H -- No --> K;