# Verification and Evaluation Plan
## Model evaluation
- Specify prediction target (e.g., land surface temperature), spatial resolution and time period.
- Baseline: training-set mean/median or simple regression; compare Random Forest / XGBoost if feasible.
- Metrics: MAE, RMSE, R² (where appropriate).
- Avoid spatial leakage with geographic holdout; consider temporal holdout.
## Data quality
Track cloud masks, missingness, spatial alignment, provenance and acquisition dates.
## XAI validation
Check SHAP output consistency and stability; clearly distinguish association from causality.
## Recommendation evaluation
Expert review for relevance, feasibility, and limitations; no unsupported temperature-reduction estimates.
## Usability and software tests
Test map selection, response schema, error handling, explanation display, and representative user tasks.
## Conditions and success criteria
[DEFINE HARDWARE, DATA SPLITS, THRESHOLDS, TEST SAMPLE AND ACCEPTANCE RULES BEFORE EVALUATION]
