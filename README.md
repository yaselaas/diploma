**Astana Urban Heat DSS**

**Development of an Explainable AI-Based Decision Support System for Nature-Based Solutions and Urban Heat Mitigation in Astana**

Diploma Project \| Astana IT University \| Software Engineering

**1. Project Overview**

Astana Urban Heat DSS is a proposed web-based decision support system designed to analyze urban surface heat patterns in Astana, Kazakhstan, and support the identification of suitable nature-based solutions (NBS).

The system will combine satellite imagery, geospatial data, machine learning, and explainable artificial intelligence (XAI) to provide transparent, location-specific insights for urban planning.

The project is currently in the **first pre-defense documentation and prototype stage**. The planned AI prediction and recommendation functionality has not yet been fully implemented or validated.

**2. Problem Statement**

Urban areas experience uneven heat distribution due to differences in vegetation, building density, paved surfaces, and land use.

In Astana, understanding these spatial patterns can support more informed decisions about urban greening and heat mitigation.

The proposed system aims to make geospatial heat information easier to explore and interpret, while clearly communicating the limitations of satellite measurements and AI predictions.

**3. Project Objectives**

1.  Collect and preprocess satellite and geospatial data for Astana.

2.  Analyze land surface temperature (LST) and relevant environmental indicators.

3.  Develop and evaluate machine-learning models for LST estimation.

4.  Apply SHAP to explain model predictions.

5.  Develop an interactive web interface for spatial analysis.

6.  Provide context-sensitive nature-based solution recommendations.

7.  Evaluate predictive performance, usability, and scientific transparency.

**4. Planned System Features**

| **Feature**          | **Description**                                                       |
|----------------------|-----------------------------------------------------------------------|
| Interactive Heat Map | Visualize spatial patterns of urban surface heat                      |
| Area Selection       | Explore environmental indicators for selected locations               |
| AI-Based Estimation  | Estimate a defined LST target using trained ML models                 |
| Explainable AI       | Display SHAP feature contributions                                    |
| NBS Recommendations  | Suggest potential greening interventions with feasibility assumptions |
| Area Comparison      | Compare environmental indicators across selected locations            |
| Export Results       | Download analysis summaries with data provenance and limitations      |

**Scientific limitation:** Satellite-derived land surface temperature is not the same as air temperature. SHAP explanations describe model feature contributions, not causal effects. Proposed interventions will not be presented as having verified cooling benefits without appropriate validation.

**5. Technology Stack**

The following technologies are planned or under evaluation.

| **Component**         | **Technology**                                         |
|-----------------------|--------------------------------------------------------|
| Frontend              | React, TypeScript                                      |
| Interactive Mapping   | Leaflet                                                |
| Backend API           | Python, FastAPI                                        |
| Machine Learning      | Random Forest, XGBoost, LightGBM                       |
| Explainable AI        | SHAP                                                   |
| Geospatial Processing | Python geospatial libraries                            |
| Geospatial Storage    | PostgreSQL/PostGIS, subject to deployment requirements |
| Data Sources          | Landsat, Sentinel, OpenStreetMap                       |
| Project Management    | YouTrack                                               |
| Version Control       | Git and GitHub                                         |

The final ML model will be selected through experimental comparison rather than assumed in advance.

**6. System Architecture**

The planned system consists of:

- **Data Layer:** Satellite imagery, land-cover information, and geospatial datasets.

- **Processing Layer:** Data cleaning, feature extraction, and spatial alignment.

- **Machine Learning Layer:** LST estimation and model evaluation.

- **Explainability Layer:** SHAP-based prediction explanations.

- **Recommendation Layer:** Context-sensitive NBS screening.

- **Backend Layer:** API services connecting analytical components with the interface.

- **Frontend Layer:** Interactive maps, analysis panels, explanations, and recommendations.

Architecture documentation includes the System Context Diagram, Use Case Diagram, and Component Diagram.

**7. Project Documentation**

The repository contains the documentation prepared for the first pre-defense.

| **File / Directory** | **Contents**                                                                                         |
|----------------------|------------------------------------------------------------------------------------------------------|
| part1.md             | Sections 1–4: Project proposal, evidence of relevance, literature review, existing-system comparison |
| part2.md             | Sections 1–6, including technology comparison and requirements specification                         |
| part3.md             | Additional documentation, architecture diagrams, and UI/UX prototype materials                       |
| part4.md             | Project management, risks, supervisor feedback documentation, and consolidated report materials      |
| diagrams/            | Architecture diagrams                                                                                |
| prototype/           | UI/UX prototype materials                                                                            |
| CONTRIBUTING.md      | Team collaboration guidelines                                                                        |

The latest consolidated documentation should be used for the first pre-defense submission, while earlier parts are retained to preserve the development history.

**8. User Research**

An anonymous Google Forms questionnaire was conducted with **18 respondents** to explore perceptions of summer heat, urban greening, and interest in understandable AI-assisted analysis.

Preliminary findings include:

- 12 of 18 respondents identified wide streets without shade as locations of heat discomfort.

- 11 of 18 respondents rated explanations of AI-assisted recommendations as important (4–5 on a five-point scale).

- 10 of 18 respondents indicated willingness to review an early prototype.

These findings provide initial user-oriented evidence but do not constitute a representative survey of Astana residents or professional stakeholder validation.

**9. Evaluation Plan**

The project plans to evaluate:

- **Prediction accuracy:** MAE, RMSE, and R².

- **Generalization:** Spatial holdout and temporal validation where feasible.

- **Data quality:** Missing data, cloud coverage, and spatial consistency.

- **Explainability:** SHAP consistency and interpretation.

- **Recommendations:** Relevance, feasibility, and transparency.

- **Usability:** Task completion, interaction clarity, and user feedback.

- **Software quality:** API tests and interface checks.

**10. Development Roadmap**

| **Period**             | **Planned Activities**                                                       |
|------------------------|------------------------------------------------------------------------------|
| October 2026           | First pre-defense: proposal, research, requirements, architecture, prototype |
| November–December 2026 | Data acquisition, preprocessing, baseline models                             |
| January–February 2027  | ML comparison, spatial validation, explainable AI                            |
| March 2027             | Backend and frontend integration                                             |
| April 2027             | User testing, refinement, final thesis preparation                           |

**11. Project Team**

**Astana IT University — Software Engineering**

| **Team Member** | **Main Responsibilities**                               |
|-----------------|---------------------------------------------------------|
| Dana Bekbosyn   | Backend architecture, API, database, system integration |
| Assel Tynysbek  | Data processing, machine learning, explainable AI       |
| Gaziza Bakir    | Frontend, UI/UX, user research and interface design     |

All team members contribute to research, documentation, testing, and project management.

**Academic Supervisor:** Omirgaliyev R., MSc in Electrical and Computer Engineering, Senior Lecturer.

**12. Project Management and Collaboration**

Development activities and documentation tasks are managed using YouTrack.

- [<u>YouTrack Project</u>](https://yaselas667.youtrack.cloud/projects/AUH)

- [<u>YouTrack Agile Board</u>](https://yaselas667.youtrack.cloud/projects/AUH/agiles/204-1/current)

- [<u>GitHub Repository</u>](https://github.com/yaselaas/diploma)

- [<u>Pull Requests</u>](https://github.com/yaselaas/diploma/pulls)

The team uses issue-linked commits, task-specific branches, and Pull Requests to document individual contributions and review changes.

**13. Running the Project**

The repository currently focuses on project documentation, architecture, and prototype materials.

A complete executable application is not yet available.

Installation instructions, environment variables, API startup commands, and frontend development commands will be added when the implementation is ready.

**14. First Pre-Defense Submission**

The first pre-defense submission includes:

- Project proposal and problem justification

- Evidence of relevance and preliminary user survey

- Critical literature review

- Existing-system and technology comparisons

- Functional and non-functional requirements

- System architecture diagrams

- UI/UX prototype materials

- Verification and evaluation plan

- Project milestones and risk management

- GitHub contribution history and YouTrack task tracking

The final submission version will be identified using the Git tag **prob-period-1** once all required materials have been reviewed and merged.

**15. Current Limitations**

The project remains in its design and early development phase.

Predictive performance, operational feasibility, intervention effectiveness, and end-user usability have not yet been established through completed system evaluations.

The project will document uncertainty, data limitations, and validation results throughout implementation.
