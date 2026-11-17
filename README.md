
# AI-Driven Diabetes Health Monitoring

Research on clinical diabetes-status classification,
retinal image analysis, explainable AI, and a proposed
IoT-based healthcare monitoring architecture.

## Overview

This repository provides research materials for
AI-assisted diabetes-related healthcare analysis.

The framework consists of:

- Clinical diabetes-status classification
- Diabetic retinopathy severity analysis
- Explainable AI (SHAP and Grad-CAM)
- Proposed IoT-enabled physiological monitoring
- Conceptual personalized recommendation support

The clinical and retinal components are evaluated
independently. No patient-level multimodal fusion
or physical IoT deployment is demonstrated.

## Clinical Machine Learning Experiment

Dataset: CDC NHANES 2007–2018
Selected records: 5,000
Classes: 2,500 diagnosed / 2,500 not diagnosed
Features: Age, Sex, Race/Ethnicity, BMI,
Waist Circumference, HbA1c, Fasting Glucose

Evaluated models:
- Random Forest
- XGBoost
- LightGBM
- CatBoost

Evaluation:
- Stratified 80/20 train-test split
- Five-fold cross-validation on training data
- Training-fold preprocessing
- Independent held-out test evaluation

## CatBoost Held-Out Results

| Metric | Result |
|---|---|
| Accuracy | 86.00% |
| Precision | 87.97% |
| Sensitivity | 83.40% |
| Specificity | 88.60% |
| F1-score | 85.63% |
| ROC-AUC | 0.9386 |

These metrics describe classification of existing
self-reported physician-diagnosed diabetes status,
not future diabetes complications.

## Visualizations

### SHAP Feature Importance

![SHAP](figures/clinical/shap.png)

### Confusion Matrix

![Confusion Matrix](figures/clinical/confusion_matrix.png)

### ROC Curve

![ROC Curve](figures/clinical/roc_curve.png)

## Retinal Image Analysis

The research also examines diabetic retinopathy
severity classification using CNN-based and
transformer-based approaches.

Retinal training scripts, patient-level split
manifests, and complete evaluation artifacts
are not included in this repository.

The retinal visualization, when included,
is provided with its provenance and
validation limitations.

## Proposed IoT Framework

IoT-based monitoring and personalized healthcare
recommendations are conceptual extensions.
No real-sensor deployment or clinical validation
of these components is claimed.

## Reproducibility

See `notebooks/clinical_training_nhanes.ipynb`
for the clinical experimental workflow.

Data source metadata is documented under
`data/metadata/`.

## Limitations

The NHANES subset is artificially balanced,
and evaluation results do not directly
represent population-level performance.

Retinal datasets may introduce domain shift.
Clinical validation is needed before deployment.

## Disclaimer

This repository is intended for academic research
and is not a medical diagnostic system.
