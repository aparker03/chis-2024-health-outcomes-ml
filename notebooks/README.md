# Notebooks

Upload the final notebooks in the following order so the repository reads as a single workflow:

1. `01_shared_cleaning_and_split.ipynb` — shared cohort preparation and fixed train/test split
2. `02_logistic_linear_elastic_net.ipynb` — Logistic Regression, Linear Regression, and Elastic Net
3. `03_decision_tree.ipynb` — Decision Tree classification and regression
4. `04_random_forest.ipynb` — Random Forest classification and regression
5. `05_ann.ipynb` — Artificial Neural Network classification and regression

The model notebooks use the same held-out test respondents. The Decision Tree, Random Forest, and ANN workflows compare the 17-variable base and 24-variable expanded predictor sets. The Logistic Regression, Linear Regression, and Elastic Net workflow uses the expanded 24-variable set.
