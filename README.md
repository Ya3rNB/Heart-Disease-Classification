# Heart-Disease-Classification
A complete machine learning workflow (EDA, Feature Engineering, and Classification) to predict the likelihood of heart disease.

# ❤️ Heart Disease Prediction Project

This project is an end-to-end machine learning workflow designed to classify whether a patient has a high likelihood of heart disease, based on a set of clinical features.

This is a classic **binary classification** problem, focusing on robust feature analysis, model training, and meaningful performance evaluation for a medical dataset. The dataset (`heart.csv`) is included in this repository.

---

## 🎯 Project Goal

The objective is to analyze 13 clinical features (such as age, blood pressure, cholesterol, etc.) from the included dataset and build a reliable classification model to predict the presence or absence of heart disease (the `target` variable).

---

## 🛠️ Project Workflow

My methodology followed these key data science stages:

### 1. Data Cleaning & Exploratory Data Analysis (EDA)
First, the dataset was analyzed to understand its structure and find patterns:
* **Target Variable Analysis:** Checked the distribution of the `target` variable (0 vs 1) to ensure the classes were reasonably balanced.
* **Feature Analysis:** Visualized the distributions of key features like `age`, `chol` (Cholesterol), and `trestbps` (Resting Blood Pressure).
* **Correlation Heatmap:** A heatmap was generated to analyze the correlation between different features and their relationship with the `target` variable.

### 2. Feature Engineering & Preprocessing
To prepare the data for modeling, the following steps were taken:
* **Categorical Feature Encoding:** Converted categorical features (like `sex`, `cp` (Chest Pain Type), `thal`) into a numerical format (e.g., One-Hot Encoding).
* **Numerical Feature Scaling:** Applied **Standardization** (StandardScaler) to all numerical features. This is critical to ensure that features with different scales (e.g., `age` vs. `cholesterol`) are treated equally by the model.

### 3. Model Training & Evaluation
This phase focused on training a robust classifier and, more importantly, evaluating it correctly.
* **Data Splitting:** The data was split into a training set (to teach the model) and a validation set (to test its performance on unseen data).
* **Model Training:** A robust classification model was trained on the standardized, processed data.
* **Performance Metrics:** Since this is a medical classification, relying only on "Accuracy" is not enough. The model was evaluated using a comprehensive set of metrics:
    * **Confusion Matrix:** To understand the types of errors—specifically False Positives vs. **False Negatives** (which are very dangerous in medical cases).
    * **Accuracy, Precision, and Recall:** To measure overall correctness, reliability of positive predictions, and the model's ability to find all actual positive cases.
    * **AUC-ROC Curve:** To evaluate the model's overall ability to discriminate between the two classes (disease vs. no disease).

### 4. Feature Importance
* After training, the model was analyzed to determine which features were the most predictive. This step is crucial for **interpretability**—understanding *why* the model makes certain predictions (e.g., `cp`, `thal`, and `ca` are often strong predictors).

---

## 💡 Key Learnings from This Project
* This project highlights the importance of choosing the **correct evaluation metrics** for classification, especially in a medical context where false negatives (missing a disease) are critical.
* Demonstrated the necessity of **feature scaling** (like Standardization) for optimizing model performance.
* Gained experience in building an end-to-end classification pipeline, from initial EDA to model interpretation and evaluation.
