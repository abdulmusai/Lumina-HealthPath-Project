# Lumina-HealthPath-Project
It is tailored to match the enterprise scope of Lumina HealthPath and communicates the clinical value to medical auditors, engineers, and stakeholders alike.
# Project PathFinder 🩺 📈
### Automated Metabolic Risk Stratification Pipeline | Lumina HealthPath

[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-latest-orange.svg)](https://scikit-learn.org/)
[![AWS SageMaker](https://img.shields.io/badge/AWS-SageMaker-FF9900.svg)](https://aws.amazon.com/sagemaker/)

## 📋 Overview
Project PathFinder transitions Lumina HealthPath's diagnostic workflow from reactive, descriptive Excel macros to a predictive machine learning framework. Operating within an ecosystem processing longitudinal health records and wearable metrics for 200+ partner hospitals, this pipeline automates clinical risk screening. 

By applying an interpretable, audited **Logistic Regression** model, PathFinder reliably flags high-risk metabolic patients ahead of chronic onset while scaling to absorb a projected 500% surge in quarterly patient data.

---

## 🔬 Business & Clinical Objectives
* **Mitigate Staff Bottlenecks:** Replaces manual clinical record screening with automated classification, eliminating a projected $1.2M annual operational staffing deficit.
* **Prioritize Clinical Safety:** Optimizes the decision boundary specifically for a **Recall score ≥ 0.85**, capping the False Negative Rate below 15% to guarantee critical cases are not missed.
* **Audit-Ready Compliance:** Ensures full interpretability for medical auditors by ranking exact feature weights (Odds Ratios) over black-box deep learning alternatives.

---

## 🛠️ Data Pipeline Architecture & Methodology

### Phase 1: Data Engineering & Robust Imputation
* **Leakage Prevention:** Strict 80/20 train-test splitting applied prior to calculating any statistical data parameters.
* **Median Imputation:** Automated handling of wearable telemetry dropouts (missing `NaN` values) using training medians to maintain resilience against clinical outliers.
* **Standardization:** Feature distribution scaling utilizing `StandardScaler` to ensure metabolic markers with disparate ranges (e.g., Blood Glucose vs. BMI) don't unfairly bias the model weights.

### Phase 2: Model Development & Clinical Calibration
* **Class Balancing:** Configured with `class_weight='balanced'` within `liblinear` to natively penalize misclassified high-risk patients.
* **Threshold Adjustment:** Shunted clinical decision thresholds downward (from 0.5 to custom levels) to favor sensitivity over precision, strictly satisfying the safety recall mandates.

---

## 🚀 Key Deliverables Included
1. **Interactive Jupyter Notebook:** Clean, PEP8-compliant pipeline detailing the entire lifecycle from raw data loading through to mathematical scaling.
2. **Auditor Interpretability Matrix:** A transparent log-odds report converting model coefficients into human-readable Clinical Odds Ratios.
3. **Validation Artifacts:** Labeled Confusion Matrices evaluating False Positives vs. False Negatives at optimized thresholds.

---

## 🛠️ Tech Stack
* **Language:** Python
* **Core Libraries:** Scikit-Learn, Pandas, NumPy, Seaborn, Matplotlib
* **Target Infrastructure:** AWS SageMaker (Inference), PostgreSQL Data Warehouse, Tableau (Stakeholder Dashboards)
