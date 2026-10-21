# Requirements Specification
Each mandatory requirement must have an objectively testable acceptance criterion.

| ID | Type | Requirement | Priority | Acceptance criterion |
|---|---|---|---|---|
| FR-01 | Functional | Display an interactive map of Astana | Must | Map renders selected study area and legend |
| FR-02 | Functional | Select an area and inspect data | Must | Selected area returns available indicators, dates and sources |
| FR-03 | Functional | Generate model prediction | Must | API returns result with target variable and model version |
| FR-04 | Functional | Explain predictions with SHAP | Must | Feature contributions are shown for a selected prediction |
| FR-05 | Functional | Display context-aware NBS options | Must | Options include rationale and constraints |
| FR-06 | Functional | Compare selected areas | Should | At least two areas can be compared |
| FR-07 | Functional | Export analysis | Could | User can export supported results |
| NFR-01 | Nonfunctional | Reproducible experiments | Must | Dataset split, seed and metrics recorded |
| NFR-02 | Nonfunctional | Protect secrets and validate inputs | Must | No secrets in repo; invalid requests rejected |
| NFR-03 | Nonfunctional | Usable and accessible interface | Should | Keyboard navigation and readable legends tested |
| NFR-04 | Nonfunctional | Scientific clarity | Must | LST and air temperature are never conflated |

Confirm and refine priorities after stakeholder discussions.
