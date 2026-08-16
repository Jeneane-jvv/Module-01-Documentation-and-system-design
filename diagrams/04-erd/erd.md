# Entity Relationship Diagram

**Editable source:** [`erd.mmd`](./erd.mmd)  
**Visual export:** [`erd.svg`](./erd.svg)

```mermaid
erDiagram
    USER {
        int user_id PK
        string display_name
        string email
        string role
        string account_status
    }

    SCENARIO {
        int scenario_id PK
        string title
        string difficulty
        string learning_goal
        string status
    }

    EVIDENCE_ITEM {
        int evidence_id PK
        int scenario_id FK
        string system_layer
        string evidence_type
        string content_reference
        int sequence_no
    }

    ATTEMPT {
    int attempt_id PK
    int user_id FK
    int scenario_id FK
    datetime started_at
    datetime completed_at
    string status
    string submitted_reasoning
}

    INVESTIGATION_STEP {
        int step_id PK
        int attempt_id FK
        int evidence_id FK
        int sequence_no
        string action_taken
        string observation
        string reason_for_next_step
    }

    CAUSE_OPTION {
        int cause_id PK
        int scenario_id FK
        string description
        boolean is_root_cause
    }

    CAUSE_ASSESSMENT {
        int assessment_id PK
        int attempt_id FK
        int cause_id FK
        string assessment_status
        string reasoning
    }

    FEEDBACK {
        int feedback_id PK
        int attempt_id FK
        int reviewer_id FK
        string feedback_text
        datetime created_at
    }

    USER ||--o{ ATTEMPT : makes
    SCENARIO ||--o{ ATTEMPT : attempted_in
    SCENARIO ||--o{ EVIDENCE_ITEM : contains
    ATTEMPT ||--o{ INVESTIGATION_STEP : records
    EVIDENCE_ITEM ||--o{ INVESTIGATION_STEP : referenced_by
    SCENARIO ||--o{ CAUSE_OPTION : defines
    ATTEMPT ||--o{ CAUSE_ASSESSMENT : evaluates
    CAUSE_OPTION ||--o{ CAUSE_ASSESSMENT : assessed_as
    ATTEMPT ||--o{ FEEDBACK : receives
    USER ||--o{ FEEDBACK : writes
```

> **Validation rule:** the model is accepted only when the editable source, rendered output, requirements, data model and related diagrams describe the same system.
