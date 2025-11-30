# Stroke Prediction Analysis 🏥

## Project Overview
This project applies **Supervised Machine Learning** techniques to predict the likelihood of a patient suffering a stroke based on demographic and health parameters (age, gender, BMI, smoking status, etc.).

This analysis was performed as the Final Project for the Supervised Learning course.

## 🥅 Goal
The objective is to build a binary classification model that can identify high-risk patients. Given the severe class imbalance (only ~5% of patients had a stroke), the project focuses on optimizing **Recall** rather than just Accuracy, to ensure potential stroke cases are not missed.

## 📂 Data Source
The dataset used is the **Stroke Prediction Dataset** from Kaggle.
* **Source:** [Kaggle - Stroke Prediction Dataset](https://www.kaggle.com/fedesoriano/stroke-prediction-dataset)
* **Description:** 5110 rows, 12 columns.
* **Cleaning:** Missing BMI values were imputed using the median. Categorical features were one-hot encoded.

## 🛠️ Methodology
1.  **EDA:** Analyzed correlations and class imbalance.
2.  **Preprocessing:** Handled missing values and used One-Hot Encoding for categorical variables.
3.  **Modeling:** Trained three models with `class_weight='balanced'`:
    * Logistic Regression
    * Decision Tree
    * Random Forest

## 📊 Key Results
| Model | Accuracy | Recall (Stroke Cases) | Conclusion |
|-------|----------|-----------------------|------------|
| Random Forest | 95% | 0.00 | Failed (Accuracy Paradox) |
| **Logistic Regression** | **75%** | **0.80** | **Best Model (High Sensitivity)** |

**Conclusion:** While Random Forest had higher accuracy, it failed to identify positive cases. **Logistic Regression** proved to be the superior model for this medical context because it successfully identified 80% of the at-risk patients.

## 💻 How to Run
1.  Clone the repository.
2.  Open the `.ipynb` file in Jupyter Notebook or Google Colab.
3.  Ensure `healthcare-dataset-stroke-data.csv` is in the same directory.
