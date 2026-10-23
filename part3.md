Astana IT University

0B06101 — SOFTWARE ENGINEERING

**DIPLOMA PROJECT**

**Development of an Explainable AI-Based Decision Support System for Nature-Based Solutions and Urban Heat Mitigation in Astana**

Pre-defense 1 documentation:

*Project Proposal · Evidence of relevance · Literature Review · Existing System Comparison*

> **Team members:**
>
> Bekbosyn Dana, SE-2414
>
> Tynysbek Assel, SE-2414
>
> Bakir Gaziza, SE-2423
>
> **Supervisor:**
>
> Omirgaliyev R.
>
> MSc in Electrical and Computer
>
> Engineering, senior-lecturer

# GitHub Repository: https://github.com/yaselaas/diploma

# YouTrack Project: https://yaselas667.youtrack.cloud/projects

# YouTrack Agile Board: https://yaselas667.youtrack.cloud/projects/AUH/agiles/204-1/current

# Executive summary

This project proposes a web-based geospatial decision support system (DSS) to help assess urban surface heat patterns in Astana and prioritize context-sensitive nature-based solutions (NBS). The planned workflow combines satellite-derived land surface temperature (LST), vegetation indicators, land cover and built-environment features with interpretable machine-learning models. Users will inspect a map, select a location, review model estimates and feature-level explanations, and examine rule-based candidate interventions with feasibility caveats. The system will not claim measured cooling benefits from hypothetical interventions without validation. Research literature and an anonymous questionnaire with 18 responses inform the initial requirements; they are explicitly separated below.

# 1. Project proposal

## 1.1 Problem, rationale and users

Urban heat is spatially heterogeneous: paved surfaces, building form, vegetation and local climate affect the thermal environment. Research shows urban greenery can provide cooling, but effectiveness depends on climate, vegetation type, morphology and spatial configuration \[1–8\]. Astana is the geographic case study; the project will establish local heat patterns empirically rather than assume published global cooling magnitudes apply directly to the city.

Target users: municipal planning and greening specialists; urban environmental researchers; university researchers and students. Secondary users may include local civil-society organizations interested in transparent spatial evidence.

## 1.2 Aim, objectives, outputs and scope

Aim: Design and evaluate an explainable AI-based DSS that maps spatial variation in urban surface heat in Astana and supports transparent screening of potential nature-based interventions.

- O1. Acquire, clean and spatially align remote-sensing and contextual geodata for a defined Astana study area and time period.

- O2. Develop reproducible baseline and machine-learning models for an explicitly defined target (initially satellite-derived LST).

- O3. Explain selected model predictions using SHAP and provide limitations and data provenance.

- O4. Develop an interactive web map, location analysis view and NBS screening recommendations.

- O5. Validate predictive performance using spatial/temporal holdouts and evaluate user-facing clarity through stakeholder feedback.

In scope: city-level spatial exploration; selected satellite acquisition dates; LST prediction/estimation; interpretable feature contributions; transparent, feasibility-aware candidate NBS; research prototype. Out of scope: real-time weather forecasting; clinical heat-health risk diagnosis; automatic construction approvals; quantified intervention-induced temperature reductions without an independent causal/simulation model; operational deployment by city authorities.

Expected deliverables: curated data pipeline; documented trained model and baseline; API; interactive web interface; explanation and recommendation components; reproducible evaluation; technical report and Git history.

# 2. Evidence of relevance: literature and survey findings

## 2.1 Literature-grounded evidence (already documented)

| Evidence | Research support | Implication for requirements |
|----|----|----|
| Urban heat is a planning and adaptation concern | IPCC \[12\] discusses urban heat risks and vegetation-based adaptation. | Map heat-related indicators and disclose interpretation limits. |
| Urban greenery can provide cooling | Global syntheses report cooling effects, with substantial heterogeneity \[1,2,3,4,5\]. | Include NBS options but avoid universal cooling promises. |
| Cooling depends on local context | Climate, tree traits and urban form influence outcomes \[2,3,5,6\]. | Record vegetation, land cover, urban morphology and feasibility constraints. |
| Benefits differ spatially | Global analysis finds unequal cooling capacity across cities \[4\]. | Enable location-specific spatial comparison, not a single citywide score. |
| Transparency is methodologically possible | SHAP attributes model predictions to input features \[10\]. | Provide feature explanations and state that attribution is not causation. |

Important: these publications support the GENERAL relevance of the problem and methodological direction; they do not establish that Astana stakeholders have requested this exact system, or quantify local cooling benefits.

## 2.2 Questionnaire and preliminary findings (18 responses)

An anonymous Google Forms questionnaire about summer heat in Astana, urban greening and the proposed AI-assisted tool received 18 responses. The questions were provided in English, Russian and Kazakh. The survey captures respondents’ experiences and preferences; it is not a representative sample of all Astana residents or a substitute for interviews with municipal planning specialists. The original summary charts are supplied in the separate survey-results document. The questionnaire items above are retained as a planning instrument; the actual completed survey used the questions summarized below.

| No. | Survey / interview question | Purpose |
|----|----|----|
| Q1 | What is your professional role in urban planning, ecology, GIS or greening? | User segment |
| Q2 | How frequently do you work with urban temperature or green-space data? | Current workflow |
| Q3 | What are the main difficulties in identifying overheated areas? | Problem validation |
| Q4 | Which datasets or maps do you currently use? | Data needs |
| Q5 | How valuable would a map of surface heat patterns be (1–5)? | Feature priority |
| Q6 | Would explanations of AI estimates increase your confidence (1–5)? Why? | XAI relevance |
| Q7 | Which NBS options are realistic in Astana, and what constraints matter? | Feasibility |
| Q8 | What information must accompany an intervention suggestion? | Output design |
| Q9 | Which functions are essential vs optional? | Prioritization |
| Q10 | Would you review a clickable prototype? What should change? | Validation follow-up |

**Survey results and interpretation**

| Survey topic | Observed result (n = 18) | Implication for the DSS |
|----|----|----|
| Summer heat and comfort | 16 of 18 respondents (88.9%) rated the effect of summer street heat on their comfort at 3–5 on a five-point scale; 10 of 18 (55.6%) selected 4 or 5. | The heat issue is noticeable among these respondents. A map could support awareness, although the survey does not measure actual LST. |
| Places of discomfort | Wide streets with no shade: 12/18 (66.7%); bus stops: 7/18 (38.9%); near large glass buildings: 5/18 (27.8%); large concrete squares: 4/18 (22.2%). Multiple choices were allowed. | Show localized heat patterns and, where possible, shade, greenery and urban-form indicators. |
| Importance of AI explanations | For explaining why AI selected a tree-planting location, 11/18 (61.1%) rated importance 4–5; 7/18 (38.9%) rated it 5. | Provide short explanations of recommendations and model limitations. |
| Early prototype feedback | 10/18 (55.6%) answered Yes to spending five minutes reviewing an early draft; 8/18 (44.4%) answered No. | A small group may be available for usability testing; no sessions are claimed to have taken place. |
| Preferred green improvements | The largest response group selected wider shade from street trees (7/18, 38.9%); other responses included parks, green roofs and combined options. | Include multiple NBS types rather than presenting tree planting as the only possible intervention. |

The survey supports the need for understandable heat maps and explanation features, while published research supports the scientific basis: the IPCC \[12\] identifies urban heat as an adaptation concern; cooling reviews \[1–6\] report that green infrastructure can reduce heat but its effects vary with climate and local form; SHAP \[10\] offers a method for explaining model predictions. Survey answers are perceptions, not measured cooling effects or proof of predictive performance. This distinction is important when translating the findings into requirements.

Evidence available: screenshots of Google Forms summary charts for 18 responses (separate file: “результаты опроса.docx”). No participant names, emails or Telegram handles are reproduced. The questionnaire provides early user feedback, but 3–5 substantive discussions with relevant specialists or a documented client agreement should still be obtained if required by the pre-defense rubric.

## 2.3 Evidence-to-requirement traceability

| Candidate requirement | Current justification | Additional validation needed |
|----|----|----|
| Interactive heat map | Remote-sensing and cooling literature \[4,9\] | Q3–Q5 |
| Explainable predictions | Interpretability framework \[10\] | Q6, Q8 |
| NBS option screening | NBS reviews \[1–3,5\] | Q7–Q8 |
| Transparent provenance and limitations | Cross-climate variability \[2,3,5\] | Q4, Q8 |

# 3. Critical literature review

Search themes: urban heat island; urban greening; nature-based solutions; tree canopy; remote sensing; spatial heterogeneity; SHAP; tree-based prediction. The following 12 distinct sources are meaningfully used. Eleven are peer-reviewed journal or conference publications \[1–11\]; \[12\] is an authoritative scientific assessment report. Foundational methodological works from 2017 are retained despite their age. Research conclusions must be verified against full texts before final thesis submission.

| Ref. | Approach / key contribution | Limitation and use in this project |
|----|----|----|
| \[1\] | 2025 meta-analysis of 373 studies: NBS cooling varies by scale and climate. | Global averages cannot be assigned to Astana; motivates context-sensitive screening. |
| \[2\] | 2024 synthesis of tree cooling across climates and urban forms. | Not a local experiment; motivates morphology and tree-context features. |
| \[3\] | 2025 review of 84 studies on green-space cooling. | Heterogeneous measurement methods; informs feasibility caveats. |
| \[4\] | 2024 global remote-sensing analysis of uneven urban cooling. | Broad geographic scale; motivates local spatial map. |
| \[5\] | 2024 systematic review of tree canopy cooling. | Evidence synthesis; supports vegetation indicators. |
| \[6\] | 2024 global field-data analysis of urban green-space cooling. | Air-temperature evidence differs from satellite LST; avoid mixing targets. |
| \[7\] | 2024 study of green-space coverage versus spatial arrangement. | Context-specific setting; motivates spatial-pattern indicators. |
| \[8\] | 2024 IoT-sensor study of green infrastructure and street-level heat. | Local sensor availability may be limited; suggests future ground validation. |
| \[9\] | 2017 Earth Engine platform paper on scalable geospatial processing. | Processing platform, not an end-user explainable DSS. |
| \[10\] | 2017 SHAP theoretical framework for feature attribution. | Attribution is not causal explanation; require careful wording. |
| \[11\] | 2016 XGBoost scalable tree-boosting methodology. | Predictive algorithm only; spatial leakage must be controlled. |
| \[12\] | 2022 IPCC assessment of urban heat adaptation and green infrastructure. | High-level assessment; cannot replace local stakeholder evidence. |

Synthesis and gap: literature demonstrates the potential of green infrastructure and the importance of local context, while geospatial platforms and explainability methods provide technical building blocks. The proposed contribution is their integration into a city-specific, user-facing workflow that documents uncertainty and distinguishes predictive explanation from causal intervention evaluation. This is a proposed design gap, not proof that no similar integrated product exists.

# 4. Existing-system comparison

Comparison is feature-scoped rather than a claim that all products are direct substitutes. Ratings: Yes = core or documented capability; Partial = possible via customization or external components; No = not a native primary function; TBD = requires direct product verification.

| System | Geospatial analysis | Thermal inputs | NBS assessment | XAI built-in | Custom DSS UX |
|----|----|----|----|----|----|
| Google Earth Engine | Yes | Yes, datasets/workflows | Partial | No | Partial |
| i-Tree tools | Partial | Limited / varies | Yes, tree ecosystem services | No | Partial |
| InVEST | Yes | Partial / model-dependent | Yes, ecosystem-service modeling | No | Partial |
| QGIS | Yes | Yes, via layers/plugins | Partial | No | Partial |
| Proposed Astana DSS | Planned | Planned LST | Planned screening | Planned SHAP | Planned |

Eight evaluation criteria to apply during final verification: map visualization; temperature-data support; vegetation metrics; NBS assessment; native explainability; ability to focus on Astana; user-oriented scenario workflow; data export and reproducibility. Current table is a preliminary functional comparison and must be backed by product documentation or hands-on tests before committee claims.

# 5. Technology comparison and rationale

| Decision | Alternatives | Decision criteria | Provisional choice |
|----|----|----|----|
| Backend | FastAPI / Django / Flask | Python ML integration, API clarity, complexity | FastAPI |
| Prediction model | Random Forest / XGBoost / LightGBM | Accuracy, training cost, explanation compatibility | Compare RF and XGBoost; choose empirically |
| Web mapping | Leaflet / OpenLayers / Mapbox GL JS | GeoJSON layers, ease, licensing, complexity | Leaflet |
| Geospatial store (optional fourth) | PostGIS / GeoPackage / SQLite | Spatial query needs, deployment overhead | PostGIS if multiuser spatial queries justify it |

Other planned components: React + TypeScript frontend; raster preprocessing with Python geospatial libraries; SHAP for feature contributions; optional Google Earth Engine for data processing subject to access/licensing. Final selection depends on pilot dataset size and deployment constraints.

# 6. Requirements specification

| ID | Requirement | Priority | Acceptance criterion |
|----|----|----|----|
| FR-01 | Display a map of the study area with basemap and heat layer | Must | Map loads and heat layer can be toggled. |
| FR-02 | Select a location and display available environmental features | Must | Click returns spatially matched values and date/provenance. |
| FR-03 | Estimate selected LST target using the trained model | Must | API returns numeric result or informative missing-data error. |
| FR-04 | Explain an estimate with SHAP feature contributions | Must | Feature contributions and target meaning are visible. |
| FR-05 | Display screened NBS candidates with assumptions | Must | At least two context-dependent options or a reason for none. |
| FR-06 | Compare selected areas | Should | Side-by-side indicators use consistent units and dates. |
| FR-07 | Export selected analysis summary | Could | Download includes date, location, data and caveats. |
| NFR-01 | Reproducibility | Must | Training and evaluation can be rerun with documented configuration. |
| NFR-02 | Privacy/security | Must | No secrets in repository; basic input validation; no unnecessary personal data. |
| NFR-03 | Performance | Should | 95% of sampled map selection requests \< 3 s in defined test environment. |
| NFR-04 | Accessibility | Should | Keyboard-accessible primary actions and readable legends. |
| NFR-05 | Scientific transparency | Must | UI distinguishes satellite surface temperature from air temperature and prediction from causal effect. |

# 7. Architecture and diagrams

## 7.1. System Context Diagram
The System Context Diagram illustrates how the proposed Urban Heat Decision Support System (DSS) for Astana interacts with its users and external data sources.

The main component is the Urban Heat DSS web application, which connects users, administrators, domain experts, and data providers.

The main users of the system are urban planners, environmental specialists, and researchers. They can select areas of Astana, request temperature analysis, explore AI-generated explanations, and receive recommendations for nature-based solutions.

The system uses two main types of external data sources. Satellite data providers, such as Landsat and Sentinel, provide information about land surface temperature, vegetation, and land cover. Geospatial data sources, such as OpenStreetMap, provide information about buildings, roads, land use, and administrative boundaries.

The administrator is responsible for managing datasets, updating the system, starting AI model training, and monitoring model performance. Domain experts evaluate the analysis results, check the relevance of recommendations, and provide feedback to improve the system.

The arrows in the diagram represent the exchange of information between the system and external actors.

Overall, this diagram demonstrates the system's external environment and explains how different participants and data sources contribute to supporting better urban planning decisions in Astana.

![System Context Diagram](../diagrams/context.png)

## 7.2. Use Case Diagram
The Use Case Diagram describes the main functions of the Urban Heat DSS and shows how different users will interact with the application.

The system includes two main actors: the User and the Administrator.

The User represents urban planners, researchers, and environmental specialists who use the application to analyze urban heat conditions.

The main user functions include:
* **View Interactive Map:** Users can explore the map of Astana and view different geographical layers.
* **Select Area of Interest:** Users can select a specific area for further analysis.
* **View Surface Temperature and Environmental Indicators:** The system displays temperature information, vegetation indicators, and other available environmental data.
* **Get AI Explanation (SHAP):** Users can understand which factors influenced the AI model's predictions.
* **Explore Nature-Based Recommendations:** The system suggests possible solutions, such as planting trees, increasing green spaces, and creating green corridors.
* **Compare Multiple Areas:** Users can compare different locations to identify areas with higher heat levels.
* **Export Results:** Users can save analysis results for further research or reporting.

The Administrator is responsible for updating data sources, triggering AI model training and evaluation, monitoring model performance, and managing system settings.

The diagram shows the relationship between users and system functions. It also illustrates the main operations that will be implemented in the web application.

Overall, the Use Case Diagram helps define the functional requirements and demonstrates how the proposed system will support urban heat analysis and decision-making.

![Use Case Diagram](../diagrams/usecase.png)

*(Note: Additive exPlanations) to explain the model's predictions and identify important input features.*
* **Recommendation Service:** Suggests suitable nature-based solutions based on the characteristics of selected urban areas and predefined planning criteria.
* **API Layer:** Connects the frontend with the database and analytical services.

## 7.3 Frontend and System Workflow
The frontend is planned to be developed using React and Leaflet. It will provide an interactive map and several user interface components, including:
* Map Interface
* Area Analysis Panel
* AI Explanation Panel
* Nature-Based Solutions Recommendations Panel
* Comparison and Export Functions

Users will interact with these components to explore heat distribution, analyze selected locations, and review possible urban greening strategies.

**System Workflow**
The overall workflow begins with collecting satellite and geographical data. The data is then cleaned, processed, and stored in the database. The machine learning model uses the prepared features to generate predictions, while the SHAP module provides explanations of these predictions.

The recommendation service uses analysis results and planning criteria to suggest possible nature-based solutions. Finally, the FastAPI backend delivers the results to the React web application, where users can view maps, explanations, and recommendations.

Overall, the Component Diagram demonstrates how data processing, machine learning, explainable AI, and web technologies will be integrated into one decision support system for urban heat analysis in Astana.

![Component Diagram](../diagrams/component.png)

# 8. UX / prototype specification
*(team-produced artifact pending)*

![Component Diagram](../diagrams/component.png)

# 9. Verification and evaluation plan

| Dimension | Metric / test | Baseline and conditions |
| :--- | :--- | :--- |
| **Predictive performance** | MAE, RMSE, R² for LST | Mean/median predictor and Random Forest; spatial holdout plus temporal holdout where feasible. |
| **Data quality** | Missingness, cloud coverage, spatial alignment | Report valid pixels, CRS, temporal matching and exclusions. |
| **Explanation fidelity** | SHAP additivity checks; stability under small perturbations | Review selected cases; explain association vs causality. |
| **Recommendation suitability** | Expert rubric: relevance, feasibility, transparency | Compare rule outputs with expert assessment; no claimed cooling °C. |
| **Usability** | Task success, time, short post-task rating | 5 representative users if available; record sample limitations. |
| **Software** | API tests, map interaction tests, export checks | Document environment and pass/fail thresholds. |

**Leakage prevention:** split data by spatial blocks and, where possible, acquisition dates rather than randomly splitting adjacent pixels. Evaluate across seasons only if data support this. Distinguish validation on satellite LST from validation against in-situ air temperature.

### **References (12 distinct sources)** 

1. Wei, H., et al. (2025). Urban cooling and energy-saving effects of nature-based solutions across types and scales. Nature Cities, 2, 1194–1204. https://www.nature.com/articles/s44284-025-00349-0 

2. Li, H., et al. (2024). Cooling efficacy of trees across cities is determined by background climate, urban morphology, and tree trait. Communications Earth & Environment, 5, 754. <u>https://www.nature.com/articles/s43247-024-01908-4</u> 

3. The cooling effect of urban green spaces as nature-based solutions for mitigating urban heat: insights from a decade-long systematic review. (2025). Climate Risk Management, 49, 100731. <u>https://doi.org/10.1016/j.crm.2025.100731</u> 

4. Li, Y., et al. (2024). Green spaces provide substantial but unequal urban cooling globally. Nature Communications, 15, 7108. https://www.nature.com/articles/s41467-024-51355-0 

5. Yin, Y., et al. (2024). Cooling Benefits of Urban Tree Canopy: A Systematic Review. Sustainability, 16(12), 4955. https://doi.org/10.3390/su16124955 

6. Greater local cooling effects of trees across globally distributed urban green spaces. (2024). Science of the Total Environment, 911, 168494. https://doi.org/10.1016/j.scitotenv.2023.168494 

7. Cooling Effect of Green Spaces on Urban Heat Island in a Chinese Megacity: Increasing Coverage versus Optimizing Spatial Distribution. (2024). Environmental Science & Technology, 58(13), 5811–5820. https://doi.org/10.1021/acs.est.3c11048 

8. Jang, S., Bae, J., & Kim, Y. (2024). Street-level urban heat island mitigation: Assessing the cooling effect of green infrastructure using urban IoT sensor big data. Sustainable Cities and Society, 100, 105007. https://doi.org/10.1016/j.scs.2023.105007 

9. Gorelick, N., et al. (2017). Google Earth Engine: Planetary-scale geospatial analysis for everyone. Remote Sensing of Environment, 202, 18–27. https://doi.org/10.1016/j.rse.2017.06.031 [10] Lundberg, S. M., & Lee, S.-I. (2017). A Unified Approach to Interpreting Model Predictions. Advances in Neural Information Processing Systems 30. <u>https://proceedings.neurips.cc/paper_files/paper/2017/hash/8a20a8621978632d76c43dfd28b67767Abstract.html</u> 

[11] Chen, T., & Guestrin, C. (2016). XGBoost: A Scalable Tree Boosting System. KDD 2016, 785–794. https://doi.org/10.1145/2939672.2939785 

[12] IPCC. (2022). Climate Change 2022: Impacts, Adaptation and Vulnerability. Working Group II, Chapter 6: Cities, settlements and key infrastructure. <u>https://www.ipcc.ch/report/ar6/wg2/chapter/chapter-6/</u> 

### **Appendix A. Survey response summary template** 

**<u>Item Entry to complete after data collection</u>** 

|Survey dates|Not visible in supplied screenshots; confirm<br>before submission|
|---|---|
|Number of respondents|18 (Google Forms summary screenshots)|
|Roles / recruitment|Not documented in supplied screenshots;<br>respondent professions cannot be verified|
|Most common reported problem|Heat discomfort in unshaded wide streets (12 of<br>18 selected this location)|
|Top three requested features|Heat map, explanation of recommendations and<br>NBS options are supported by responses;<br>formal feature ranking not verified|
|Key NBS constraints|EVIDENCE|
|Differences from literature expectations|INTERPRETATION|
|Requirements updated after survey|IDS|



