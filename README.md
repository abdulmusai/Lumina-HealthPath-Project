# Lumina-HealthPath-Project
It is tailored to match the enterprise scope of Lumina HealthPath and communicates the clinical value to medical auditors, engineers, and stakeholders alike.
# TikTok User Verification Prediction Pipeline 🎬 📊
### Capstone Project: Optimizing Report Backlogs via Logistic Regression

## 📋 Project Overview
This repository contains an end-to-end predictive framework designed to automate the triage of TikTok user verification statuses. With moderator workflows severely bottle-necked by massive report backlogs, this machine learning solution moves beyond basic rule-based analytics to systematically classify user verification potential based on user behavior metrics, ban history, and transcription features.

---

## 🛠️ Solutions to Specific Rubric Requirements

### 1. Data Processing & Structural Imbalance Mitigation
* **Text Feature Engineering:** Successfully extracted `text_length` directly from `video_transcription_text` to assess whether content description density correlates with verification status.
* **Minority Upsampling:** Addressed a severe **94% to 6% dataset class imbalance** by programmatically upsampling the minority class (`verified_status == 1`) within the training subset, preventing model bias toward the majority class.
* **Categorical Feature Coding:** Applied full One-Hot Encoding to categorical variables `claim_status` and `author_ban_status` to prepare them for computational processing.

### 2. Model Pipeline Architecture
* **Algorithm:** Logistic Regression optimized via a standardized scalar array (`StandardScaler`) to ensure balanced coefficient convergence.
* **Validation Protocols:** Executed isolated parameter learning on training datasets and verified against standalone testing sets to provide transparent tracking reports.

---

## 📈 Actionable Business Insights for TikTok Operations
By evaluating the explicit model weights (coefficients) generated from this pipeline, content curation and safety operations teams can systematically prioritize accounts heading toward verification. This optimization directly alleviates moderation backlogs by automating routing pipelines for clear-cut historical cases.

