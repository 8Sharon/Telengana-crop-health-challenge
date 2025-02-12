# Telangana Crop Health Challenge

## Overview

The **Telangana Crop Health Challenge** aims to develop a machine learning model capable of classifying the health conditions of various crops in the Telangana state of South-Central India. The model utilizes both historical **Sentinel-2 time series satellite data** and data on **cultivation practices** to assess the health of crops in real-time.

This model will be a vital tool for farmers and government bodies to monitor crop health, enabling them to take proactive measures to prevent crop damage and ultimately improve crop yield.

## Objective

The primary objective of this competition is to build a machine learning model that can:
- Classify the health of crops in Telangana.
- Utilize cultivation practices and Sentinel-2 satellite imagery time series data.
- Provide insights for both farmers and government bodies to monitor crop health and mitigate risks that affect crop yield.

## Dataset

The dataset provided includes:
- **Cultivation Practices**: Information about the cultivation methods, crop types, and agricultural practices.
- **Sentinel-2 Time Series Data**: Satellite imagery data from Sentinel-2 that includes vegetation indices, temperature, and other features related to the crop health.

## Libraries and Dependencies

This project uses several key libraries for data processing, machine learning model training, and evaluation:

- **pandas**: For data manipulation and analysis.
- **numpy**: For numerical operations.
- **lightgbm**: For the gradient boosting model (LGBMClassifier).
- **scikit-learn**: For data preprocessing, model evaluation, and machine learning utilities.
- **seaborn** and **matplotlib**: For data visualization.

## Workflow Overview

The workflow consists of several key steps for data processing, feature engineering, model training, evaluation, and visualization:

### 1. Data Loading and Preprocessing

- **Load the dataset** using pandas to work with crop health data.
- **Handle missing values**: Fill or remove missing data based on the type of features.
- **Categorical variable conversion**: Convert categorical variables into numerical values using encoding techniques such as Label Encoding or One-Hot Encoding.
- **Feature engineering**: Create new features and transform raw data into meaningful input for the model.
- **Time series data preprocessing**: Process historical Sentinel-2 data, ensuring it's ready for machine learning models.

### 2. Feature Engineering

- **Integrating cultivation practices data**: Combine Sentinel-2 time series features with farming data, such as irrigation practices, soil quality, crop types, and fertilizers, to provide comprehensive input for the model.

### 3. Model Training and Evaluation

- **Base Model**: Use **LightGBM (Light Gradient Boosting Machine)** as the base model for classification. LightGBM is a fast and efficient gradient boosting algorithm suitable for large datasets and complex problems.
- **Cross-Validation**: Use **Stratified K-Fold cross-validation** to train the model and assess its performance across different subsets of the data, ensuring the model generalizes well.
  
### 4. Hyperparameter Tuning

- **Optimization**: Tune the hyperparameters of the LightGBM model, such as learning rate, number of trees, depth of trees, and regularization, to enhance performance.
- **Early Stopping**: Implement **early stopping** to halt training once the model's performance stops improving on the validation set, preventing overfitting and saving computation time.

### 5. Model Evaluation

- **Evaluation Metrics**: Evaluate the model using classification metrics  **accuracy**, **F1 score**, and a **detailed classification report** to understand model performance.
  
### 6. Visualization

- **Feature Importance**: Visualize the importance of each feature to understand which ones influence the model's decision-making the most.
- **Class Distribution**: Plot the distribution of classes (crop health conditions) to assess the balance of the dataset and potential model bias.

