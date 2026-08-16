# System Context

**Editable source:** [`system-context.mmd`](./system-context.mmd)  
**Visual export:** [`system-context.svg`](./system-context.svg)

```mermaid
flowchart LR
    Learner["Learner<br/>Student, Intern or Junior Developer"]
    Mentor["Mentor / Reviewer"]
    System(("FirstCommit<br/>Engineering Readiness System"))

    Learner -->|Profile information, scenario selection, investigation responses| System
    System -->|Scenario content, technical evidence, feedback, progress| Learner

    Mentor -->|Scenario content, review feedback| System
    System -->|Learner attempts, reasoning trail, progress| Mentor
```

> **Validation rule:** the model is accepted only when the editable source, rendered output, requirements, data model and related diagrams describe the same system.
