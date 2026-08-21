# CHIS 2024 Health Outcomes and Healthcare Utilization

This repository contains the modeling workflow for a team machine-learning study using the 2024 California Health Interview Survey (CHIS) Adult Public Use File. The study evaluates two outcomes: CHIS-defined chronic risk-factor control and the number of doctor visits reported in the past 12 months.

The work is predictive rather than causal. Direct CHIS measures used to determine `RISK_CONTROL` were excluded from the classification predictors to reduce target leakage.

## Research questions

1. To what extent can demographic, socioeconomic, health, behavioral, and chronic-condition information classify CHIS-defined chronic risk-factor control when the direct measures used to determine control are excluded?
2. How much additional predictive value do insurance, healthcare-affordability, and access-to-care measures provide beyond the base characteristics for classification?
3. To what extent can the available CHIS characteristics predict annual doctor-visit utilization, and how much additional predictive value is provided by insurance and healthcare-access measures?
4. How consistent is predictive performance across race/ethnicity, poverty, insurance, and urban/rural subgroups?

## Modeling workflow

The final modeling cohort contains 11,700 adults and uses a fixed 80/20 train/test split with 9,360 training respondents and 2,340 test respondents. Two predictor sets were defined: a 17-variable base set and a 24-variable expanded set that adds seven insurance, affordability, and healthcare-access measures.

The model families include:

- Logistic Regression for classification
- Linear Regression and Elastic Net for regression
- Decision Tree classification and regression
- Random Forest classification and regression
- Artificial Neural Network classification and regression

Model selection and tuning were performed with the training data before final held-out test evaluation. Five-fold cross-validation was used for tuned models where applicable.

## Repository structure

```text
notebooks/
├── 01_shared_cleaning_and_split.ipynb
├── 02_logistic_linear_elastic_net.ipynb
├── 03_decision_tree.ipynb
├── 04_random_forest.ipynb
└── 05_ann.ipynb
```

## Data access

CHIS data are not redistributed in this repository. The source data should be obtained directly from the UCLA Center for Health Policy Research. The shared cleaning and split notebook documents the preparation of the modeling cohort and the fixed train/test files used by the model notebooks.

## Contributors

- Alexis Parker
- Krystal Marroquin
- Sandipta Khare
- Ivan Lopez

Developed for IST 347: Machine Learning in Healthcare at Claremont Graduate University.