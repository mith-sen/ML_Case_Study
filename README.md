# ML Capstone — Classification Track (Review 1, Part A)

## Scope

This part of the repository covers the **Classification track** only, as required for Review 1 Part A
of the 23CSE301 Machine Learning capstone project. Regression and Clustering tracks (and Classification
Part B) are out of scope here and are owned by other team members / covered in Review 2.

## Dataset

- File: `data/classification.csv`
- 4,424 rows, 37 columns (36 features + 1 target)
- Target column: `Target` — three classes (`Dropout`, `Enrolled`, `Graduate`)
- No missing values, no duplicate rows (see the Dataset Audit section of the notebook)

## Models Implemented (Review 1, Part A)

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
jupyter notebook notebooks/classification.ipynb
```

Run all cells top to bottom. The notebook is reproducible (`random_state=42` used throughout).

## Repository Structure

```
project/
├── data/
│   └── classification.csv
├── notebooks/
│   └── classification.ipynb
├── requirements.txt
├── README.md
└── .gitignore
```

