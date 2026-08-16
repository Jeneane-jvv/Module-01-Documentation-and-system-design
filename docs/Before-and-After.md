# Before and After — What I Am Improving

This file does not hide mistakes from my earlier work. It records what those mistakes taught me.

| Earlier learning / issue | What I understand now | New practice |
|---|---|---|
| A problem statement could move quickly into the proposed solution | Problem and solution are different stages | Keep the initial problem statement solution-neutral |
| Some success targets appeared before strong evidence for the exact number | A measurable target still needs a source or justification | Mark unvalidated targets as assumptions/design targets |
| Strong spreadsheet findings could lead quickly to a proposed action | Correlation does not automatically prove the cause | Separate **finding → possible explanation → research question → decision** |
| Different diagrams were sometimes created as separate deliverables | Models must describe the same system | Use requirement traceability across use case, DFD, ERD and UI |
| An earlier ERD source began with a malformed Mermaid fence | A diagram is not finished only because the visual looks right | Validate the editable source and rendered result |
| Some earlier diagram Markdown files missed closing Mermaid fences | Source hygiene matters | Use consistent raw `.mmd` source plus a clean Markdown wrapper |
| An earlier independent-design ERD source did not include the `erDiagram` declaration | Correct model syntax is part of reproducibility | Keep the ERD source explicit and self-contained |
| An earlier wireframe included information not represented in the ERD | UI data must trace to the data model | Run a cross-diagram consistency check |
| A Level 1 DFD could introduce logic that blurred the boundary with another Level 0 process | DFD decomposition should remain balanced with its parent | Define which Level 0 process is being decomposed before drawing Level 1 |
| Finishing the exercise was once the end goal | A professional design must support the next developer/stage | End the project with a clean data/design handoff |

## What I am keeping

Not everything needed changing.

My earlier guided design work showed useful habits that I want to preserve:

- documenting stakeholder communication;
- identifying project roles;
- analysing a real dataset instead of relying only on opinion;
- linking high borrowing/late-return patterns to system needs;
- distinguishing functional and non-functional requirements;
- designing multiple views of the same proposed system.

## New standard

A design is ready only when I can answer:

> **Why does this element exist, what evidence or requirement justifies it, and where does it appear in the rest of the system?**
