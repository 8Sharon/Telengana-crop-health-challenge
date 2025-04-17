# 🌾 Telangana Crop Health Challenge

Leveraging satellite imagery and agricultural practices to predict and protect crop health in Telangana, India.

![Crop Monitoring](https://cropnuts.com/wp-content/uploads/2024/10/Website-Images-650-%C3%97-407-px-5.png)

---

## ⚠️ Disclaimer

All datasets, information, and reports within this repository are fictional and created solely for illustrative purposes to showcase advanced predictive machine learning techniques. They do not include any real proprietary, confidential, or sensitive information related to any company, organization, or individual.

---

## 📑 Table of Contents

1. [Problem Statement](#problem-statement)  
2. [Overview](#overview)  
3. [Objective](#objective)  
4. [Dataset](#dataset)  
5. [Libraries and Dependencies](#libraries-and-dependencies)  
6. [Workflow Overview](#workflow-overview)  
   - [1. Data Loading and Preprocessing](#1-data-loading-and-preprocessing)  
   - [2. Feature Engineering](#2-feature-engineering)  
   - [3. Model Training and Evaluation](#3-model-training-and-evaluation)  
   - [4. Hyperparameter Tuning](#4-hyperparameter-tuning)  
   - [5. Model Evaluation](#5-model-evaluation)  
   - [6. Visualization](#6-visualization)  
7. [Contacts](#contacts)

---

## 🧩 Problem Statement

Agricultural productivity in Telangana is highly dependent on effective monitoring and early detection of crop stress, disease, or poor health conditions. With the availability of remote sensing data and agricultural practice records, there is an opportunity to build a predictive model that provides real-time insights into crop health.

This challenge seeks to create a robust machine learning model that uses satellite imagery (Sentinel-2) and farming practice data to classify crop health. Such a model can empower farmers and policymakers to act quickly and improve yield outcomes.

---

## 🌱 Overview

The **Telangana Crop Health Challenge** focuses on classifying the health condition of crops across Telangana using historical **Sentinel-2 satellite imagery time series** and **cultivation practices data**. This predictive model will provide a critical tool for timely intervention in agriculture.

It has the potential to:

- Predict crop health status across different regions
- Help stakeholders take proactive decisions
- Reduce yield loss through early intervention

---

## 🎯 Objective

The primary goals of the project are:

- To build a machine learning model that classifies crop health as Healthy, stressed, diseased or pests.
- To leverage satellite imagery and agricultural practice data in combination.
- To deliver actionable insights to farmers and agricultural departments.

---

## 📦 Dataset

The dataset consists of two major components:

1. **Cultivation Practices Data**  
   - Crop type  
   - Irrigation methods  
   - Soil properties  
   - Fertilizer usage e.t.c 

---

## 🧰 Libraries and Dependencies

This project leverages the following Python libraries:

- `pandas` – Data manipulation and wrangling  
- `numpy` – Numerical operations  
- `lightgbm` – Fast and scalable gradient boosting classifier  
- `scikit-learn` – Preprocessing, evaluation, and cross-validation  
- `seaborn`, `matplotlib` – Visualization and plotting  

Install dependencies with:

``bash pip install pandas numpy lightgbm scikit-learn matplotlib seaborn
## 🔄 Workflow Overview

### 1. Data Loading and Preprocessing

- Load CSV, GeoTIFF, or other satellite datasets using `pandas` and geospatial libraries.
- Handle missing values appropriately (e.g., imputation or removal).
- Encode categorical variables using **Label Encoding** .
- Normalize numerical variables to ensure consistent scale.
- Align and synchronize **Sentinel-2** time series data with cultivation records using timestamps or geolocation keys.

---

### 2. Feature Engineering

- Merge **satellite data** with **agricultural data** based on geo-coordinates, timestamps, or farm ID.
- Aggregate satellite features over custom time windows (e.g., weekly/monthly rolling means).
- Calculate derived features like:
  - Crop growth rate
  - Drought index
  - Lag-based vegetation indices
- Encode **seasonal trends** and **spatial zones** to capture environmental patterns.

---

### 3. Model Training and Evaluation

- Use **LightGBM Classifier** as the base model for high-performance classification.
- Apply **Stratified K-Fold Cross-Validation** to maintain class balance across folds.
- Evaluate performance metrics for each fold to ensure consistent generalization.

---

### 4. Hyperparameter Tuning

- Tune key parameters like:
  - `learning_rate`
  - `num_leaves`
  - `max_depth`
  - `min_child_samples`
  - `subsample`
- Use search methods like `GridSearchCV`, `RandomizedSearchCV`, or **Optuna**.
- Implement **Early Stopping** to halt training when no improvement is observed on the validation set.

---

### 5. Model Evaluation

- Evaluate model using:
  - ✅ **Accuracy**
  - 🎯 **F1 Score**
  - 📋 **Classification Report** (Precision, Recall, F1 per class)
---

### 6. Visualization

- 📊 **Feature Importance Plot** – Highlight key drivers influencing predictions.
- 📉 **Class Distribution Plot** – Analyze class balance for potential bias.
- 🌿 **Time Series Trend Analysis** – Visualize vegetation index changes across time to detect anomalies or patterns.

---

## 📬 Contacts

For questions, collaboration, or feedback:

- 📧 Email: [njerisharon611@gmail.com](njerisharon611@gmail.com)    
- 🌐 GitHub: [Telangana-Crop-Health](https://github.com/8Sharon/Telengana-crop-health-challenge)


