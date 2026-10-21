# Astana Urban Heat DSS

**Diploma topic:** Development of an Explainable AI-Based Decision Support System for Nature-Based Solutions and Urban Heat Island Mitigation in Astana.

## Project status
Pre-defense planning and architecture stage. The application, datasets, interviews, and evaluation results are **not yet completed**.

## Problem and goal
Urban areas experience uneven surface heat. This project proposes a web-based decision support system to analyze land surface temperature and related geospatial features, explain machine-learning predictions, and present context-aware nature-based solution options for Astana. Predictions and recommendations must not be presented as proven causal cooling effects.

## Target users
Urban planners, environmental specialists, and researchers.

## Planned stack (subject to comparison and validation)
- Frontend: React, TypeScript, Leaflet
- Backend: Python, FastAPI
- ML: scikit-learn / XGBoost; SHAP for explanations
- Spatial storage: PostgreSQL + PostGIS
- Inputs: appropriate Landsat, Sentinel and OpenStreetMap datasets, subject to availability and licensing

## Team and supervisor
- Team members: [ADD NAMES AND RESPONSIBILITIES]
- Supervisor: [ADD NAME]

## Links
- GitHub repository: [ADD EXISTING REPOSITORY URL]
- YouTrack: [ADD PROJECT URL]
- Figma prototype: [ADD LINK WHEN READY]

## Project scope
See `docs/01-project-proposal.md` and `docs/06-requirements.md`.

## Structure
- `docs/` research, requirements, evaluation, planning, feedback
- `diagrams/` editable diagram sources and exports
- `prototype/` prototype links and screen descriptions
- `frontend/`, `backend/`, `ml/` future application components
- `data/` data dictionary and sample metadata (no sensitive or large raw datasets)
- `tests/` planned and future automated tests
- `config/` configuration examples

## Setup and testing
No runnable implementation has been delivered in this scaffold. Add commands for installation, running, and testing once the relevant components exist. Do not claim the app is operational yet.

## Contributions
Create a YouTrack issue, work on a separate branch, make meaningful commits referencing the issue, open a pull request, obtain teammate review, and merge after acceptance criteria are met. See `CONTRIBUTING.md`.
