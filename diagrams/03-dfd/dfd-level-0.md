# Data Flow Diagram — Level 0

**Editable source:** [`dfd-level-0.mmd`](./dfd-level-0.mmd)  
**Visual export:** [`dfd-level-0.svg`](./dfd-level-0.svg)

```mermaid
flowchart LR

    subgraph ACTORS["External Actors"]
        direction TB
        Learner["Learner"]
        Mentor["Mentor / Reviewer"]
    end

    subgraph SYSTEM["FirstCommit System"]
        direction TB
        P1(("1.0 User Access"))
        P2(("2.0 Manage Scenarios"))
        P3(("3.0 Investigate Scenario"))
        P4(("4.0 Review & Track Progress"))
    end

    subgraph STORES["Data Stores"]
        direction TB
        D1[("D1 Users")]
        D2[("D2 Scenarios")]
        D3[("D3 Attempts")]
        D4[("D4 Feedback")]
    end

    Learner -->|Credentials| P1
    P1 -->|Access result| Learner
    P1 <--> D1

    Learner -->|Scenario request| P2
    Mentor -->|Scenario updates| P2
    P2 <--> D2
    P2 -->|Scenario| Learner
    P2 -->|Status| Mentor

    Learner -->|Actions & observations| P3
    D2 -->|Technical evidence| P3
    P3 <--> D3
    P3 -->|Next-step context| Learner

    Learner -->|Reasoning / progress request| P4
    Mentor -->|Review| P4
    D3 -->|Attempt history| P4
    P4 <--> D4
    P4 -->|Feedback / progress| Learner
    P4 -->|Attempt summary| Mentor
```

> **Validation rule:** the model is accepted only when the editable source, rendered output, requirements, data model and related diagrams describe the same system.
