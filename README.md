# ML Capstone — Classification Track (Review 1, Part A)

## Scope

This part of the repository covers the **Regression and Classification track** only, as required for Review 1 Part A
of the 23CSE301 Machine Learning capstone project. 

## Dataset


- File: `data/classification.csv, data/regression.csv`

## Models Implemented (Review 1, Part A)

# Regression

1. Linear Regression 
2. Ridge Regression
3. Lasso Regression
4. ElasticNet Regression 
5. Polynomial Regression 
6. Decision Tree Regressor
7. Random Forest Regressor 
8. Gradient Boosting Regressor 
9. Support Vector Regressor (SVR) 
10. K-Nearest Neighbors Regressor

#Classification

1. Logistic Regression
2. K-Nearest Neighbors (KNN)
3. Gaussian Naive Bayes
4. Decision Tree Classifier
5. Support Vector Machine (SVC)

Each model is evaluated with Accuracy, Weighted F1-score, and a Confusion Matrix, using the same
80:20 stratified train/test split and the same leakage-safe preprocessing pipeline
(`ColumnTransformer` + `Pipeline`, fit on training data only).

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook notebooks/regression.ipynb
jupyter notebook notebooks/classification.ipynb
```

Run all cells top to bottom. The notebook is reproducible (`random_state=42` used throughout).

## Repository Structure

```
project/
├── data/
    └── data.csv
│   └── SeoulBikeData.csv
├── notebooks/
    └── classification.ipynb
    └── regression.ipyn
├── requirements.txt
├── README.md

```

