```mermaid
flowchart 
    subgraph Solution
        subgraph Connect Care
            subgraph Wisdom
                proc[Dental Procedures]
                doc[Dental Documenation]
            end
            subgraph EpicCare Ambulatory
                activity[Clinic Activities]
                encDoc[Encounter Documentation]
            end
        end
    end
    subgraph UX
        web[Web Browser]
        cda[CDAnet iTrans]
    end
    subgraph Users
        clerks[Clerks/Front Desk Staff]
        hygene[Dental Hygenists]
        denAssist[Registered Dental Assistants]
        dentist[Dentists]
    end