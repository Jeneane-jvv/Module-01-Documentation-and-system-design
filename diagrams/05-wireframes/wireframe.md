# Low-Fidelity Wireframe

**Editable source:** [`wireframe.mmd`](./wireframe.mmd)  
**Visual export:** [`wireframe.svg`](./wireframe.svg)

```mermaid
flowchart TB

    DASH["LEARNER DASHBOARD<br/><br/>
    FirstCommit<br/>
    ─────────────────────<br/>
    Continue current scenario<br/>
    Available scenarios<br/>
    Recent progress<br/>
    Feedback waiting"]

    WORK["SCENARIO WORKSPACE<br/><br/>
    Scenario title and objective<br/>
    Problem / ticket summary<br/>
    ─────────────────────<br/>
    Technical evidence<br/>
    What did I observe?<br/>
    What should I inspect next and why?<br/>
    Possible causes<br/>
    ─────────────────────<br/>
    Save investigation step<br/>
    Submit reasoning"]

    REVIEW["REVIEW SUMMARY<br/><br/>
    Reasoning trail<br/>
    Evidence inspected<br/>
    Causes assessed / eliminated<br/>
    Submitted reasoning<br/>
    Reviewer feedback<br/>
    ─────────────────────<br/>
    What would I do differently?"]

    DASH -->|Open scenario| WORK
    WORK -->|Submit investigation| REVIEW
    REVIEW -->|Return to dashboard| DASH
```

> **Validation rule:** the model is accepted only when the editable source, rendered output, requirements, data model and related diagrams describe the same system.
