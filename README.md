# Bank Marketing Campaign Classification
## Addressing Imbalanced Classification with Multiple Models and Feature Selection Strategies

## Objective
This repository aims to address the problem of imbalanced classification by implementing and evaluating different machine learning models combined with feature selection strategies. The process involves tuning hyperparameters, selecting the best subset of features, and calibrating model probabilities to achieve optimal performance.

## Dataset Description
The dataset used in this repository comes from a bank marketing campaign. The goal is to predict whether a client will subscribe to a term deposit based on various features. The dataset includes both categorical and numerical features:

- **ID:** Unique identifier for each client.
- **age:** Age of the client.
- **job:** Type of job.
- **marital:** Marital status.
- **education:** Level of education.
- **default:** Whether the client has credit in default.
- **balance:** Account balance.
- **housing:** Whether the client has a housing loan.
- **loan:** Whether the client has a personal loan.
- **contact:** Contact communication type.
- **day:** Last contact day of the month.
- **month:** Last contact month of the year.
- **duration:** Duration of the last contact in seconds.
- **campaign:** Number of contacts performed during this campaign.
- **pdays:** Number of days since the client was last contacted from a previous campaign.
- **previous:** Number of contacts performed before this campaign.
- **poutcome:** Outcome of the previous marketing campaign.
- **subscribed:** Target variable indicating whether the client subscribed to a term deposit.

## Methodology
### 1. Data Preprocessing
- **Encoding Categorical Features:** Used Label Encoding.
- **Handling Numerical Features:** Applied log transformation and Yeo-Johnson transformation.
- **Scaling Features:** Employed StandardScaler and RobustScaler.

### 2. Initial Evaluation for Imbalanced Classification Approaches
- **Methods Evaluated:**
  - SMOTETomek
  - Class Weights
  - Calibrated Probability
- **Validation:** 3-repeated stratified 5-fold cross-validation.
- **Metric:** AUPRC (Average Precision Score).

### 3. Hyperparameter Tuning and Feature Selection
- **Models Implemented:**
  - Random Forest
  - XGBoost
  - KNN
  - Logistic Regression
- **Feature Selection Strategies:**
  - Mutual Information
  - Pearson Correlation
- **Optimization Techniques:**
  - Optuna
- **Calibration:** Used CalibratedClassifierCV for probability calibration.
- **Evaluation Metrics:**
  - AUPRC (Average Precision Score)
  - ROC AUC
  - Confusion Matrix

