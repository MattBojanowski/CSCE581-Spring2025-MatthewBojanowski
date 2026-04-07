# AI Testcase: Adult Income Model

### 1. TC-identifier:
TC-adult-001

### 2. TC-name:
Adult census dataset model and explanation pipeline correctness

### 3. TC-objective:
Validate adult data loading pipeline and classification model AUC metrics for glassbox and blackbox models.

### 4. TC-input:
- `load_adult_data()`
- `build_glassbox_pipeline()` + train
- `build_blackbox_rf_pipeline()` + train

### 5. TC-reference-output:
- Adult data has > 30,000 rows and no nulls after preprocessing.
- Logistic regression (glassbox) AUC >= 0.76.
- Random forest (blackbox) AUC >= 0.85.

### 6. TC-harm-risk-info:
HC1-incorrect-info (income predictions can affect policy decisions if relied on). Use thresholds and checks to avoid silent failure.

### 7. TC-other-info:
- Data set loaded from UCI; tests depend on network availability but drop missing values and encode categories to stable features.
- Use fixed `random_state=42`.

