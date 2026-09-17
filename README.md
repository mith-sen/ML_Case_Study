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

## AI-Assistance Disclosure

Per the project guideline (Section 7.5), generative AI (Claude, Anthropic) was used for **code
scaffolding** of the classification notebook: structuring sections, writing the preprocessing
pipeline, model-training/evaluation boilerplate, and plotting code. AI was **not** used to generate
data interpretation, analysis conclusions, or feature-engineering justification — these are marked
with `[TEAM MEMBER ...]` placeholders in the notebook and must be completed by the responsible team
member after personally inspecting the plots and results, per the academic integrity requirement.

## Outstanding Items Before Submission

- [ ] Fill in all `[TEAM MEMBER SHOULD WRITE A DATA-SPECIFIC OBSERVATION ...]` Markdown placeholders
      in the EDA section
- [ ] Fill in the `[TEAM MEMBER TO VERIFY AND COMPLETE]` justification for the engineered
      `approval_rate` feature
- [ ] Prepare for viva questions on algorithm choice, metric interpretation, and preprocessing
      decisions
