```mermaid
graph LR
    subgraph ConnectCare_Epic_Wisdom ["Connect Care"]
        direction LR
        CC_PatInfo[Patient Demographics]
        CC_Insurance[Insurance Info]
        CC_Sched[Scheduling]
        CC_Clinical[Clinical Documentation]
        CC_Proc[Procedures / Billing Codes]
        CC_Estimates{Estimates Module}
    end

    subgraph Option1_Components ["Option 1 Components"]
        direction LR
        ThirdPartyEMR["3rd Party Dental EMR (e.g., Power Practice, Gold Dental)"]
        DataTransfer["Data Transfer (File/HL7?)"]
        Insurance["Insurance Carriers / CDAnet (ITRANS)"]
    end

    ConnectCare_Epic_Wisdom -- DataTransfer --> ThirdPartyEMR
    ThirdPartyEMR -- CDAnet/ITRANS --> Insurance
    Insurance -- CDAnet/ITRANS --> ThirdPartyEMR
    CC_Estimates -- Potentially informs --> ThirdPartyEMR
