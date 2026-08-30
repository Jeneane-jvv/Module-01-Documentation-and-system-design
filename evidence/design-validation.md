# Design Validation

**Review date:** 16 August 2026  
**Method:** VS Code source + live Mermaid preview review

## Status

| Area | Source reviewed | Live visual reviewed | Screenshot captured | Final SVG updated |
|---|---|---|---|---|
| FRAME | Yes | Yes | Yes | Yes |
| System context | Yes | Yes | Yes | Yes |
| Use case | Yes | Yes | Yes | Yes |
| DFD Level 0 | Yes | Yes | Yes | Yes |
| DFD Level 1 | Yes | Yes | Yes | Yes |
| ERD | Yes | Yes | Yes | Yes |
| Wireframe | Yes | Yes | Yes | Yes |
| Full system-design documentation | Updated | Yes | Yes | N/A |

## Validation outcomes

### FRAME
- [x] Stages follow Idea → Find → Research → Ask & Analyse → Map → Explore → Design Ready.
- [x] Wording is clear and professional.
- [x] Transition to Module 02 is visible.

### System context
- [x] External actors are outside the system.
- [x] Information crossing the boundary is labelled.
- [x] Internal process detail is not mixed into the context view.

### Use case
- [x] Learner and mentor/reviewer goals are separated.
- [x] Use cases represent actor goals rather than process sequence.
- [x] Workflow arrows were removed from the use-case model.

### DFD Level 0
- [x] Four high-level processes are shown.
- [x] D1–D4 data stores are identified.
- [x] Major external flows are labelled.
- [x] Level 0 is kept readable instead of carrying Level 1 detail.

### DFD Level 1
- [x] Explicitly decomposes **3.0 Investigate Scenario**.
- [x] Shows 3.1 through 3.5 in a readable sequence.
- [x] Does not introduce login or unrelated mentor-administration logic.
- [x] Input/output duplication is used only to improve visual readability.

### ERD
- [x] `erDiagram` is present in editable Mermaid source.
- [x] Primary and foreign keys are identified.
- [x] Relationships and cardinalities are defined.
- [x] Data stores can be mapped to ERD concepts.
- [x] Final reasoning is stored as `submitted_reasoning`; possible causes and assessments remain structured separately.

### Wireframe
- [x] Main learner flow is visible: Dashboard → Workspace → Review.
- [x] Wireframe information exists in the data model.
- [x] Screen design was simplified for readability.

## Cross-diagram consistency

- [x] `Learner` and `Mentor / Reviewer` have consistent meaning.
- [x] Major use cases trace to candidate requirements.
- [x] Level 0 process 3.0 is decomposed by Level 1.
- [x] DFD data stores map to ERD concepts.
- [x] Wireframe information can be supported by the ERD.
- [x] Editable sources open and render in VS Code.
- [x] Screenshots 01–08 capture source + live visual evidence.
- [x] Screenshot 09 captures the updated `System-Design-Documentation.md` source + Markdown preview.

## Final review rule

> A design element is accepted only when I can explain **why it exists, which need or requirement justifies it, where its data comes from, and how it connects to the other models**.


## Final evidence status

All nine planned VS Code evidence screenshots have been captured and reviewed for Project 01.

## Authorship / provenance validation

- [x] No lecturer/provider guide is included in the repository.
- [x] No original assessment brief or marking rubric is included.
- [x] No third-party application code is included.
- [x] No other student's work is included.
- [x] Assessment-specific scenario names have been removed from the public learning-evidence summary.
- [x] AI-assisted mentoring is disclosed in the provenance statement.
- [x] Jeneane reviewed the editable source and rendered artefacts in VS Code.
