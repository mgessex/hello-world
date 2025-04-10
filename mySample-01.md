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

    subgraph Option3_Components ["Option 3 Components"]
        direction LR
        InHouseInterface["In-House Built Interface"]
        Insurance["Insurance Carriers / CDAnet (ITRANS)"]
    end

    ConnectCare_Epic_Wisdom -- Sends --> InHouseInterface
    Insurance -- Receives --> InHouseInterface
    InHouseInterface -- Sends --> Insurance
    InHouseInterface -- Recieves --> ConnectCare_Epic_Wisdom