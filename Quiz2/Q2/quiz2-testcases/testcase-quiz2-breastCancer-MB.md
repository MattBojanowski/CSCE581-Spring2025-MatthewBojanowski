# AI Testcase: Breast Cancer Model

### 1. TC-identifier:
TC-breast-001

### 2. TC-name:
Breast cancer dataset model and explanation pipeline correctness

### 3. TC-objective:
Ensure breast cancer data loading and models behave as expected, with model AUC meeting minimum production thresholds.

### 4. TC-input:
- `load_breast_data()`
- `build_glassbox_pipeline()` + split and train
- `build_blackbox_rf_pipeline()` + split and train

### 5. TC-reference-output:
- Loaded breast data has 569 rows and 30 features.
- Logistic regression (glassbox) AUC >= 0.88.
- Random forest (blackbox) AUC >= 0.95.

### 6. TC-harm-risk-info:
HC1-incorrect-info (biased model predictions or calculation errors can mislead diagnosis risk). Verify deterministic thresholds.

### 7. TC-other-info:
- Uses sklearn's `train_test_split` with fixed `random_state=42` and `stratify=y` for stable tests.
- This is a regression-style integration test for model pipelines.

