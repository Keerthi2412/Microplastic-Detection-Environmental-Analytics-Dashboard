# Water Samples Dataset - Machine Learning

## 1. Overview

This module performs machine learning analysis on the cleaned water sample fact dataset used in the Microplastic Water Quality Analytics project.

The fact dataset contains measurements collected from different water sources and locations.

The dataset provides the primary contamination information required for microplastic analysis.

---

## 2. Dataset

### Input Dataset

`cleaned_fact_water_samples.csv`

### Main Information

The dataset contains water quality and microplastic-related attributes such as:

- Sample ID
- Timestamp
- Location ID
- Water Temperature
- pH Level
- Turbidity
- Dissolved Oxygen
- Average Particle Size
- Dominant Polymer
- Dominant Morphology
- Microplastic Count
- Risk Level

---

## 3. ML Objective

The objective is to analyze the relationship between water quality parameters and microplastic contamination.

The main prediction target is:

`Microplastic_Count_per_m3`

Since the target is numerical, this is a regression problem.

---

## 4. Machine Learning Algorithm

### Random Forest Regressor

Random Forest Regressor is used to predict the microplastic concentration.

The algorithm is suitable because:

- It can model non-linear relationships.
- It can handle multiple input features.
- It works well with mixed environmental variables.
- It is relatively robust to outliers.
- It provides feature importance.

---

## 5. Data Preparation

The following steps are performed:

1. Load the cleaned dataset.
2. Check dataset shape.
3. Check missing values.
4. Check duplicate records.
5. Convert timestamp into datetime format.
6. Extract time-based features.
7. Select relevant ML features.
8. Separate features and target.
9. Encode categorical variables.
10. Split data into training and testing datasets.

---

## 6. Feature Engineering

The timestamp is used to create:

- Hour
- Day
- Month
- Day of Week

These features help the model identify possible temporal patterns in contamination.

---

## 7. Target Variable

The prediction target is:

`Microplastic_Count_per_m3`

The model attempts to estimate the number of microplastic particles per cubic meter of water.

---

## 8. Model Training

The Random Forest Regressor is trained using:

- Number of estimators: 300
- Random state: 42
- Test size: 20%
- Parallel processing: Enabled

Categorical variables are converted using One-Hot Encoding.

---

## 9. Model Prediction

The trained model is used to generate:

`Predicted_Microplastic_Count`

The prediction results contain:

- Sample ID
- Timestamp
- Location ID
- City
- State
- Actual Microplastic Count
- Predicted Microplastic Count
- Prediction Error
- Absolute Error

---

## 10. Risk Prediction

Predicted microplastic concentration is converted into a risk category.

Example:

| Predicted Count | Risk Level |
|---|---|
| < 100 | Low |
| 100–349 | Medium |
| 350–699 | High |
| >= 700 | Critical |

These thresholds are project-defined thresholds for dashboard demonstration and should not be presented as regulatory limits unless supported by an authoritative standard.

---

## 11. Model Evaluation

The regression model is evaluated using:

### MAE

Mean Absolute Error measures the average difference between actual and predicted values.

### RMSE

Root Mean Squared Error gives more weight to larger prediction errors.

### R² Score

R² measures how well the model explains variation in the target variable.

---

## 12. Visualization

The notebook generates:

- Actual vs Predicted plot
- Prediction Error Distribution
- Feature Importance
- Model evaluation metrics

---

## 13. Output

The model generates:

`ml_predictions.csv`

This file contains the actual and predicted microplastic concentrations and predicted risk levels.

---

## 14. Notebook

The implementation is available in:

`water_samples_model.ipynb`

---

## 15. Technologies

- Python
- Pandas
- NumPy
- Jupyter Notebook
- Matplotlib
- Seaborn

---

## 16. Future Improvement

The water sample model can be improved by incorporating:

- Location information
- Weather conditions
- Polymer characteristics
- Historical contamination trends
- Time-based validation
- Hyperparameter tuning

These features are incorporated into the final combined ML model.
