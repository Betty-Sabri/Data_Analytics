# California Wildfire Damage Analysis and Prediction

## Overview

This project presents a comprehensive analysis of structural damage caused by wildfires in California, with a focus on data quality assessment, feature engineering, and predictive modeling. The objective is to identify key factors influencing fire damage and develop models capable of predicting structural outcomes.

---

## Objectives

* Assess and improve dataset quality through systematic validation
* Identify relationships between structural features and fire damage
* Engineer meaningful features to enhance predictive performance
* Build and evaluate machine learning models for damage classification

---

## Dataset

The dataset contains structural and environmental information related to wildfire incidents, including:

* Building characteristics (roof type, siding, windows, structure category)
* Property attributes (assessed value, year built)
* Geographic data (latitude, longitude)
* Target variable: level of structural damage

---

## Data Quality Assessment

A structured data quality report was conducted, including:

* Data type validation and transformation
* Detection of missing, duplicate, and constant values
* Logical consistency checks across features

### Key Actions

* Removed columns with high missingness (>70%)
* Dropped non-informative constant features
* Identified and corrected invalid entries (e.g. year built, zip codes)

---

## Data Preparation

The dataset was cleaned and prepared using the following strategies:

* Categorical features: imputed using mode
* Numerical features: imputed using median
* Invalid values (e.g. zeros) converted to missing and handled accordingly
* Introduction of "Unknown" category for incomplete categorical data

---

## Exploratory Data Analysis

Exploratory analysis revealed several important patterns:

* Fire-resistant materials (e.g. metal, concrete) are associated with lower damage rates
* Structures with more openings (e.g. windows, vents) exhibit higher vulnerability
* Larger and higher-value buildings demonstrate increased resilience
* Older structures are more likely to sustain severe damage

---

## Feature Engineering

Additional features were constructed to improve analytical depth:

* **Fire Risk Score**: derived from material-based attributes
* **Building Complexity Score**: based on structural characteristics
* **Urban Proximity Indicator**: classification of urban vs rural locations

---

## Modeling Approach

Three supervised learning models were implemented:

### 1. Linear Regression

* Baseline model for interpretability
* Provided insight into feature influence via coefficients

### 2. Logistic Regression

* Binary classification model
* Balanced performance across precision and recall

### 3. Random Forest Classifier

* Ensemble-based model capturing non-linear relationships
* Achieved the highest predictive performance

---

## Model Performance

* Linear Regression: ~77% accuracy
* Logistic Regression: balanced precision (~74%) and recall (~78%)
* Random Forest: highest accuracy, with indications of overfitting

---

## Key Findings

* Structural attributes (roof type, siding, windows) are primary drivers of fire damage
* Property value and building size correlate with increased resilience
* Design elements such as enclosed structures and fire-resistant materials significantly reduce risk

---

## Technologies Used

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn

---

## Project Structure

```
project/
│
├── data/
│   ├── original/
│   ├── modified/
│   └── extended/
│
├── notebooks/
│   ├── data_quality_report.ipynb
│   ├── analysis.ipynb
│   └── modeling.ipynb
│
├── outputs/
│   ├── figures/
│   └── reports/
│
└── README.md
```

