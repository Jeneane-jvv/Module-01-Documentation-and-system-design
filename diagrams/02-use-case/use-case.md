# Use-Case Model

**Editable source:** [`use-case.mmd`](./use-case.mmd)  
**Visual export:** [`use-case.svg`](./use-case.svg)

```mermaid
flowchart LR

    Learner["Learner"]
    Mentor["Mentor / Reviewer"]

    subgraph FC["FirstCommit System"]
        direction TB

        subgraph LG["Learner Goals"]
            direction TB
            UC1(["Create or access profile"])
            UC2(["Choose engineering scenario"])
            UC3(["Inspect technical evidence"])
            UC4(["Record investigation step"])
            UC5(["Evaluate possible causes"])
            UC6(["Submit root-cause reasoning"])
            UC7(["Review reasoning path and feedback"])
            UC8(["View learning progress"])
        end

        subgraph MG["Mentor / Reviewer Goals"]
            direction TB
            UC9(["Create or maintain scenario"])
            UC10(["Review learner attempt"])
            UC11(["Provide feedback"])
        end
    end

    Learner --> UC1
    Learner --> UC2
    Learner --> UC3
    Learner --> UC4
    Learner --> UC5
    Learner --> UC6
    Learner --> UC7
    Learner --> UC8

    Mentor --> UC9
    Mentor --> UC10
    Mentor --> UC11
```

> **Validation rule:** the model is accepted only when the editable source, rendered output, requirements, data model and related diagrams describe the same system.
