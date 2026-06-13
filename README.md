# 📱 Mobile Phone Price Range Prediction

## Overview

This project focuses on building a Machine Learning classification model to predict the **price range of a mobile phone** based on its technical specifications and hardware features.

The dataset contains various smartphone attributes such as battery capacity, RAM, camera specifications, screen dimensions, processor speed, and network capabilities. Since the dataset does not include a predefined target variable, a custom **price_range** feature is engineered using key specifications such as RAM, battery power, and screen resolution.

The final model classifies mobile phones into different price categories, helping manufacturers understand market positioning and enabling consumers to estimate a device's price segment based on its specifications.

---

## Problem Statement

The objective is to develop a classification model capable of predicting a smartphone's price range using its technical features.

### Key Tasks

* Perform Exploratory Data Analysis (EDA)
* Create a target variable (`price_range`)
* Preprocess and scale data
* Train multiple classification models
* Evaluate model performance using classification metrics
* Compare model results and select the best-performing model

---

## Dataset Features

The dataset contains features such as:

| Feature       | Description               |
| ------------- | ------------------------- |
| battery_power | Battery capacity (mAh)    |
| blue          | Bluetooth support         |
| clock_speed   | Processor speed (GHz)     |
| dual_sim      | Dual SIM support          |
| fc            | Front camera megapixels   |
| four_g        | 4G support                |
| int_memory    | Internal memory (GB)      |
| m_dep         | Mobile depth              |
| mobile_wt     | Weight of mobile phone    |
| n_cores       | Number of processor cores |
| pc            | Primary camera megapixels |
| px_height     | Screen resolution height  |
| px_width      | Screen resolution width   |
| ram           | RAM capacity              |
| sc_h          | Screen height             |
| sc_w          | Screen width              |
| talk_time     | Battery talk time         |
| three_g       | 3G support                |
| touch_screen  | Touch screen support      |
| wifi          | WiFi support              |

---

## Exploratory Data Analysis (EDA)

The following analyses were performed:

* Distribution of battery power
* Distribution of clock speed
* Analysis of 4G-enabled devices
* Correlation heatmap
* Feature relationship analysis
* Outlier detection
* Summary statistics

### Sample Visualizations

* Histogram of Battery Power
* Count Plot of 4G Support
* Clock Speed Distribution
* Correlation Matrix Heatmap

---

## Feature Engineering

Since the dataset did not contain a target variable, a custom **price_range** column was generated using important numerical features such as:

* RAM
* Battery Power
* Screen Resolution
* Internal Memory

Phones were categorized into predefined classes:

| Price Range | Category  |
| ----------- | --------- |
| 0           | Low-End   |
| 1           | Mid-Range |
| 2           | High-End  |
| 3           | Premium   |

---

## Data Preprocessing

The following preprocessing steps were applied:

* Missing value verification
* Feature scaling using StandardScaler
* Train-Test Split
* Feature selection
* Data validation

---

## Machine Learning Models

The following classification algorithms were evaluated:

### 1. Logistic Regression

* Baseline classification model

### 2. Decision Tree Classifier

* Easy interpretability
* Handles non-linear relationships

### 3. Random Forest Classifier

* Ensemble learning approach
* Reduces overfitting

### 4. XGBoost Classifier (Optional)

* Boosting-based algorithm
* High predictive performance

### 5. K-Nearest Neighbors (KNN)

* Distance-based classification

---

## Model Evaluation

Models were evaluated using:

* Accuracy Score
* Precision
* Recall
* F1-Score
* Confusion Matrix
* Classification Report

### Evaluation Metrics

```python
from sklearn.metrics import (
    accuracy_score,
    classification_report,
    confusion_matrix
)
```

---

## Project Workflow

```text
Data Collection
       ↓
Exploratory Data Analysis
       ↓
Feature Engineering
       ↓
Data Preprocessing
       ↓
Model Training
       ↓
Model Evaluation
       ↓
Performance Comparison
       ↓
Final Model Selection
```

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* XGBoost (Optional)
* Jupyter Notebook

---

## Project Structure

* Mobile-Price-Range-Prediction
  * dataset
    * mobile_data.csv
  * notebooks
    * Mobile_Price_Prediction.ipynb
* README.md


## Results

The trained model successfully classified smartphones into different price segments using hardware specifications and achieved competitive classification performance.

Key findings:

* RAM was one of the strongest predictors of price range.
* Screen resolution significantly influenced pricing.
* Internal memory and battery capacity contributed to classification performance.
* Ensemble models generally outperformed individual models.

---

## Future Improvements

* Use real market price data instead of a generated target variable.
* Hyperparameter tuning using GridSearchCV.
* Deploy the model using Flask or Streamlit.
* Integrate feature importance visualization.
* Build an interactive web application for price range prediction.

---

## Author

**Ayush Uniyal**

Aspiring Data Scientist | Machine Learning Enthusiast | SQL & Python Learner

Feel free to connect and provide feedback on the project.
