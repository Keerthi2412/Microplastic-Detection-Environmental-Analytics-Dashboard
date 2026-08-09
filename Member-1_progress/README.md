Location Dataset - Machine Learning
----------------------------------------
1. Overview
This module performs machine learning analysis on the cleaned location dimension dataset used in the Microplastic Water Quality Analytics project.

The dataset contains geographical and environmental information about different water sampling locations.

The purpose of this module is to demonstrate how location-related information can be used for machine learning classification.

---

## 2. Dataset

### Input Dataset

`dim_locations_cleaned.csv`

### Dataset Information

The dataset contains information such as:

- Location ID
- Location Name
- Water Body Type
- Latitude
- Longitude
- City
- State
- Nearby Industry Type

### Target Variable

The target variable used for classification is:

`Water_Body_Type`

### Input Features

The model uses:

- Latitude
- Longitude
- City
- State
- Nearby Industry Type

---

## 3. Objective

The objective is to develop a machine learning classification model that predicts the type of water body based on geographical and location-related characteristics.

This model is mainly used as an ML demonstration because the location dataset does not contain direct microplastic contamination measurements.

---

## 4. Machine Learning Algorithm

### Random Forest Classifier

Random Forest Classification is used because it can handle:

- Numerical features
- Categorical features after encoding
- Non-linear relationships
- Multiple classes

---

## 5. Data Preparation

The following preprocessing steps were performed:

1. Loaded the cleaned location dataset.
2. Checked missing values.
3. Checked duplicate records.
4. Selected relevant features.
5. Separated input features and target variable.
6. Applied One-Hot Encoding to categorical variables.
7. Split the dataset into training and testing sets.

---

## 6. Model Training

The Random Forest Classifier was trained using:

- Number of estimators: 100
- Random state: 42
- Test size: 20%

The model was implemented using a Scikit-learn Pipeline.

---

## 7. Model Prediction

After training, the model predicts:

`Water_Body_Type`

for the test records.

The prediction output contains:

- Location ID
- Location Name
- City
- State
- Actual Water Body Type
- Predicted Water Body Type

---

## 8. Model Evaluation

The following metrics are used:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

The evaluation results are used to compare the actual and predicted water body types.

---

## 9. Important Limitation

The location dataset contains only a small number of records and multiple water-body categories.

Therefore, this model should be considered a demonstration model and should not be treated as a production-level prediction system.

The main project ML model is developed using the combined dataset containing water quality, location, polymer and weather information.

---

## 10. Notebook

The complete implementation is available in:

`ML_model(Dataset-2).ipynb`

The notebook contains:

1. Data loading
2. Data inspection
3. Feature selection
4. Data preprocessing
5. Model training
6. Model prediction
7. Model evaluation
8. Confusion matrix

---

## 11. Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook
- Matplotlib
- Seaborn

---

## 12. Project Role

This module is handled by the ML & Documentation Lead.

Responsibilities include:

- ML experimentation
- Model training
- Prediction
- Evaluation
- Documentation
- Reporting ML results
