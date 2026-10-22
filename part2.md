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
