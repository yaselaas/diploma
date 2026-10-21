# Architecture and Diagrams
The required diagrams are available as **editable Mermaid source files** in `diagrams/`:
1. `system-context.mmd`
2. `use-case.mmd`
3. `component.mmd`

Export each to SVG/PNG for your report, and keep the editable source. These are preliminary diagrams and should be updated with the final scope and requirements.

## Data flow
Satellite / geographic sources → ETL and feature extraction → spatial storage → prediction → SHAP explanations and NBS recommendation logic → FastAPI → React/Leaflet.

Note: SHAP explains model outputs, not causation. Recommendations are decision-support options, not proven cooling outcomes.
