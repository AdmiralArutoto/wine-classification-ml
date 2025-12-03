
#  Wine Classification — Supervised Learning Project

This repository contains a complete end-to-end supervised learning workflow for classifying wines into three categories based on their chemical properties.
The project is implemented in a single, well-structured Jupyter Notebook located inside the notebooks/ directory.





##  Project Structure

```bash
wine-classification-ml/
│
├── notebooks/
│   └── Wine_classification_supervised_learning_upgraded.ipynb
│
├── datasets/
│   └── wine_description.txt
│   └── wine_test.csv
│   └── wine_train.csv
│
├── requirements.txt
├── .gitignore
└── README.md
```




## Project Overview

This project demonstrates a full machine learning pipeline, including:

- Data loading (train & test sets)
- Exploratory Data Analysis (EDA)
    - Correlation analysis
    - Feature distributions
    - Outlier inspection
    - Class balance visualization
- Feature engineering
    - Removal of highly correlated features
- Model selection
    - KNN pipeline with scaling
    - Decision Tree model
    - Hyperparameter tuning using GridSearchCV
- Model training
- Model evaluation on a held-out test set
    - Accuracy
    - F1-macro score
    - Classification report
    - Confusion matrix
- Baseline model comparison
    - Logistic Regression
    - Random Forest

Everything is implemented cleanly inside one notebook.




## Dataset

The project uses the classic Wine dataset, consisting of:

- 13 numeric chemical features, such as alcohol, malic acid, magnesium, flavanoids, color intensity, hue, etc.
- Target: Wine class (0, 1, 2)

This is a multiclass classification problem, and the notebook focuses on F1-macro, which balances performance across all classes.




## Models Implemented

The notebook explores several algorithms:

✔ K-Nearest Neighbors (KNN)

- Uses StandardScaler

- Tuned over n_neighbors, weights, and metric

- Selected as one of the best performers

✔ Decision Tree Classifier

- Tuned using entropy criterion and depth constraints

✔ Logistic Regression (baseline)

- Pipeline with scaling

✔ Random Forest (baseline)

- 200 trees

- Strong general-purpose performance

All models are evaluated on the same test split for fair comparison.





## How to Run

1. Create a virtual environment

```bash
python3 -m venv .venv
source .venv/bin/activate
```
2. Install dependencies
```bash
pip install -r requirements.txt
```
3. Open the notebook
```bash
#vscode-
code .
```
Then open:
```bash
notebooks/Wine_classification_supervised_learning_upgraded.ipynb
```

