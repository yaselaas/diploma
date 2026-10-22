Astana IT University 0B06101 — SOFTWARE ENGINEERING 

## **DIPLOMA PROJECT** 

# **Development of an Explainable AI-Based Decision Support System for Nature-Based Solutions and Urban Heat Mitigation in Astana** 

Pre-defense 1 documentation: 

_Project Proposal · Evidence of relevance · Literature Review · Existing System_ 

_Comparison_ 

**Team members:** Bekbosyn Dana, SE-2414 Tynysbek Assel, SE-2414 Bakir Gaziza, SE-2423 

**Supervisor:** Omirgaliyev R. MSc in Electrical and Computer Engineering, senior-lecturer 

GitHub Repository: <u>https://github.com/yaselaas/diploma</u> 

YouTrack Project: <u>https://yaselas667.youtrack.cloud/projects</u> 

YouTrack Agile Board: <u>https://yaselas667.youtrack.cloud/projects/AUH/agiles/204-1/current</u> 

### **Executive summary** 

This project proposes a web-based geospatial **decision support system (DSS)** to help assess urban surface heat patterns in Astana and prioritize context-sensitive **nature-based solutions (NBS)** . The planned workflow combines satellite-derived **land surface temperature (LST)** , vegetation indicators, land cover and built-environment features with interpretable machine-learning models. Users will inspect a map, select a location, review model estimates and feature-level explanations, and examine rule-based candidate interventions with feasibility caveats. The system will not claim measured cooling benefits from hypothetical interventions without validation. Research literature and an anonymous questionnaire with 18 responses inform the initial requirements; they are explicitly separated below. 

## **1. Project proposal** 

### **1.1 Problem, rationale and users** 

Urban heat is spatially heterogeneous: paved surfaces, building form, vegetation and local climate affect the thermal environment. Research shows urban greenery can provide cooling, but effectiveness depends on climate, vegetation type, morphology and spatial configuration [1–8]. Astana is the geographic case study; the project will establish local heat patterns empirically rather than assume published global cooling magnitudes apply directly to the city. 

**Target users:** municipal planning and greening specialists; urban environmental researchers; university researchers and students. Secondary users may include local civil-society organizations interested in transparent spatial evidence. 

### **1.2 Aim, objectives, outputs and scope** 

**Aim:** Design and evaluate an explainable AI-based DSS that maps spatial variation in urban surface heat in Astana and supports transparent screening of potential nature-based interventions. 

- **Objective 1** . Acquire, clean and spatially align remote-sensing and contextual geodata for a defined Astana study area and time period. 

- **Objective 2** . Develop reproducible baseline and machine-learning models for an explicitly defined target (initially satellite-derived LST). 

- **Objective 3** . Explain selected model predictions using SHAP and provide limitations and data provenance. 

- **Objective 4** . Develop an interactive web map, location analysis view and NBS screening recommendations. 

- **Objective 5** . Validate predictive performance using spatial/temporal holdouts and evaluate userfacing clarity through stakeholder feedback. 

**In scope:** city-level spatial exploration; selected satellite acquisition dates; LST prediction/estimation; interpretable feature contributions; transparent, feasibility-aware candidate NBS; research prototype. 

**Out of scope:** real-time weather forecasting; clinical heat-health risk diagnosis; automatic construction approvals; quantified intervention-induced temperature reductions without an independent causal/simulation model; operational deployment by city authorities. 

**Expected deliverables:** curated data pipeline; documented trained model and baseline; API; interactive web interface; explanation and recommendation components; reproducible evaluation; technical report and Git history. 

## **2. Evidence of relevance:** 

### **2.1 Literature-grounded evidence (already documented)** 

|Evidence|Researchsupport|Implication for requirements|
|---|---|---|
|Urban heat is a planning and<br>adaptation concern|IPCC [12] discusses urban<br>heat risks and vegetation-<br>based adaptation.|Map heat-related indicators<br>and disclose interpretation<br>limits.|
|Urban greenery can provide<br>cooling|Global syntheses report<br>cooling effects, with<br>substantial heterogeneity<br>[1,2,3,4,5].|Include NBS options but avoid<br>universal cooling promises.|
|Cooling depends on local<br>context|Climate, tree traits and urban<br>form influence outcomes<br>[2,3,5,6].|Record vegetation, land cover,<br>urban morphology and<br>feasibility constraints.|
|Benefits differ spatially|Global analysis finds unequal<br>cooling capacity across cities<br>[4].|Enable location-specific<br>spatial comparison, not a<br>single citywide score.|
|Transparency is<br>methodologically possible|SHAP attributes model<br>predictions to input<br>features [10].|Provide feature<br>explanations and state that<br>attribution is not<br>causation.|



**Important:** these publications support the GENERAL relevance of the problem and methodological direction; they do not establish that Astana stakeholders have requested this exact system, or quantify local cooling benefits. 

### **2.2 Questionnaire and preliminary findings (18 responses)** 

An anonymous **Google Forms questionnaire** about summer heat in Astana, urban greening and the proposed AI-assisted tool received 18 responses. The questions were provided in English, Russian 

and Kazakh. The survey captures respondents’ experiences and preferences; it is not a representative sample of all Astana residents or a substitute for interviews with municipal planning specialists. The original summary charts are supplied in the separate survey-results document. The questionnaire items above are retained as a planning instrument; the actual completed survey used the questions summarized below. 

|**No.**|**Survey / interview question**|**Purpose**|
|---|---|---|
|Q1|What is your professional role<br>in urban planning, ecology,<br>GIS or greening?|User segment|
|Q2|How frequently do you work<br>with urban temperature or<br>green-space data?|Current workflow|
|Q3|What are the main difficulties<br>in identifying overheated<br>areas?|Problem validation|
|Q4|Which datasets or maps do you<br>currently use?|Data needs|
|Q5|How valuable would a map of<br>surface heat patterns be (1–5)?|Feature priority|
|Q6|Would explanations of AI<br>estimates increase your<br>confidence (1–5)? Why?|XAI relevance|
|Q7|Which NBS options are<br>realistic in Astana, and what<br>constraints matter?|Feasibility|
|Q8|What information must<br>accompany an intervention<br>suggestion?|Output design|
|Q9|Which functions are essential<br>vs optional?|Prioritization|
|Q10|Would you review a clickable<br>prototype? What should<br>change?|Validation follow-up|



## **Survey results and interpretation** 

|**Survey topic**|**Observed result (n = 18)**|**Implication for the DSS**|
|---|---|---|
|Summer heat and comfort|16 of 18 respondents (88.9%)<br>rated the effect of summer<br>street heat on their comfort at<br>3–5 on a five-point scale; 10 of<br>18 (55.6%) selected 4 or 5.|The heat issue is noticeable<br>among these respondents. A<br>map could support awareness,<br>although the survey does not<br>measure actual LST.|
|Places of discomfort|Wide streets with no shade:<br>12/18 (66.7%); bus stops: 7/18<br>(38.9%); near large glass<br>buildings: 5/18(27.8%); large|Show localized heat patterns<br>and, where possible, shade,<br>greenery and urban-form<br>indicators.|



||concrete squares: 4/18<br>(22.2%). Multiple choices<br>were allowed.||
|---|---|---|
|Importance of AI explanations|For explaining why AI<br>selected a tree-planting<br>location, 11/18 (61.1%) rated<br>importance 4–5; 7/18 (38.9%)<br>rated it 5.|Provide short explanations of<br>recommendations and model<br>limitations.|
|Early prototype feedback|10/18 (55.6%) answered Yes<br>to spending five minutes<br>reviewing an early draft; 8/18<br>(44.4%) answered No.|A small group may be<br>available for usability testing;<br>no sessions are claimed to<br>have taken place.|
|Preferred green improvements|The largest response group<br>selected wider shade from<br>street trees (7/18, 38.9%);<br>other responses included parks,<br>green roofs and combined<br>options.|Include multiple NBS types<br>rather than presenting tree<br>planting as the only possible<br>intervention.|



The survey supports the need for understandable heat maps and explanation features, while published research supports the scientific basis: the IPCC [12] identifies urban heat as an adaptation concern; cooling reviews [1–6] report that green infrastructure can reduce heat but its effects vary with climate and local form; SHAP [10] offers a method for explaining model predictions. Survey answers are perceptions, not measured cooling effects or proof of predictive performance. This distinction is important when translating the findings into requirements. 

Evidence available: screenshots of Google Forms summary charts for 18 responses (separate file: “результаты опроса.docx”). No participant names, emails or Telegram handles are reproduced. The questionnaire provides early user feedback, but 3–5 substantive discussions with relevant specialists or a documented client agreement should still be obtained if required by the pre-defense rubric. 

## **2.3 Evidence-to-requirement traceability** 

|Candidate requirement|Current justification|Additional validation needed|
|---|---|---|
|Interactive heat map|Remote-sensing and cooling<br>literature [4,9]|Q3–Q5|
|Explainable predictions|Interpretability framework [10]|Q6, Q8|
|NBS option screening|NBS reviews [1–3,5]|Q7–Q8|
|Transparent provenance and<br>limitations|Cross-climate variability<br>[2,3,5]|Q4, Q8|



## **3. Critical literature review** 

Search themes: urban heat island; urban greening; nature-based solutions; tree canopy; remote sensing; spatial heterogeneity; SHAP; tree-based prediction. The following 12 distinct sources are 

meaningfully used. Eleven are peer-reviewed journal or conference publications [1–11]; [12] is an authoritative scientific assessment report. Foundational methodological works from 2017 are retained despite their age. Research conclusions must be verified against full texts before final thesis submission. 

|**Reference number**|**Approach / key contribution**|**Limitation and use in this**<br>**project**|
|---|---|---|
|1|2025 meta-analysis of 373<br>studies: NBS cooling varies by<br>scale and climate.|Global averages cannot be<br>assigned to Astana; motivates<br>context-sensitive screening.|
|2|2024 synthesis of tree cooling<br>across climates and urban<br>forms.|Not a local experiment;<br>motivates morphology and<br>tree-context features.|
|3|2025 review of 84 studies on<br>green-space cooling.|Heterogeneous measurement<br>methods; informs feasibility<br>caveats.|
|4|2024 global remote-sensing<br>analysis of uneven urban<br>cooling.|Broad geographic scale;<br>motivates local spatial map.|
|5|2024 systematic review of tree<br>canopy cooling.|Evidence synthesis; supports<br>vegetation indicators.|
|6|2024 global field-data analysis<br>of urban green-space cooling.|Air-temperature evidence<br>differs from satellite LST;<br>avoid mixing targets.|
|7|2024 study of green-space<br>coverage versus spatial<br>arrangement.|Context-specific setting;<br>motivates spatial-pattern<br>indicators.|
|8|2024 IoT-sensor study of<br>green infrastructure and street-<br>level heat.|Local sensor availability may<br>be limited; suggests future<br>ground validation.|
|9|2017 Earth Engine<br>platform paper on scalable<br>geospatialprocessing.|Processing platform, not<br>an end-user explainable<br>DSS.|
|10|2017 SHAP theoretical<br>framework for feature<br>attribution.|Attribution is not causal<br>explanation; require<br>careful wording.|
|11|2016 XGBoost scalable tree-<br>boosting methodology.|Predictive algorithm only;<br>spatial leakage must be<br>controlled.|
|12|2022 IPCC assessment of<br>urban heat adaptation and<br>green infrastructure.|High-level assessment; cannot<br>replace local stakeholder<br>evidence.|



**Synthesis and gap:** literature demonstrates the potential of green infrastructure and the importance of local context, while geospatial platforms and explainability methods provide technical building blocks. The proposed contribution is their integration into a city-specific, user-facing workflow that 

documents uncertainty and distinguishes predictive explanation from causal intervention evaluation. This is a proposed design gap, not proof that no similar integrated product exists. 

## **4. Existing-system comparison** 

Comparison is feature-scoped rather than a claim that all products are direct substitutes. Ratings: 

- Yes = core or documented capability; 

- Partial = possible via customization or external components; 

- No = not a native primary function; 

- TBD = requires direct product verification. 

|System|Geospatial<br>analysis|Thermal inputs|NBS<br>assessment|XAI<br>built-in|Custom<br>DSS UX|
|---|---|---|---|---|---|
|Google<br>Earth<br>Engine|Yes|Yes,<br>datasets/workflows|Partial|No|Partial|
|i-Tree<br>tools|Partial|Limited / varies|Yes, tree<br>ecosystem<br>services|No|Partial|
|InVEST|Yes|Partial / model-<br>dependent|Yes,<br>ecosystem-<br>service<br>modeling|No|Partial|
|QGIS|Yes|Yes, via<br>layers/plugins|Partial|No|Partial|
|Proposed<br>Astana<br>DSS|Planned|Planned LST|Planned<br>screening|Planned<br>SHAP|Planned|



### **Eight evaluation criteria to apply during final verification:** 

- map visualization; 

- temperature-data support; 

- vegetation metrics; 

- NBS assessment; 

- native explainability; 

- ability to focus on Astana; 

- user-oriented scenario workflow; 

- data export and reproducibility. 

_Current table is a preliminary functional comparison_ 

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



