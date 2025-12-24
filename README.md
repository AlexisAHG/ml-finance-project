# Machine Learning Finance Project  
## Bankruptcy Prediction (Taiwan)

Academic machine learning project focused on **predicting corporate bankruptcy**
using financial indicators from Taiwanese companies.

---

## Project overview
This project studies bankruptcy data from the **Taiwan Economic Journal**
covering the years **1999–2009**.
A company is labeled as bankrupt according to the business regulations of the
**Taiwan Stock Exchange**.

The goal is to build reliable machine learning models capable of detecting
early signs of bankruptcy based on financial ratios.

---

## Objectives
- Explore and understand a high-dimensional financial dataset
- Clean and preprocess the data for modeling
- Handle class imbalance and outliers
- Train and compare multiple classification models
- Evaluate performance using appropriate metrics

---

## Dataset
- **6,819 companies**
- **96 columns** (95 features + target)
- Financial ratios such as:
  - Debt Ratio
  - Borrowing Dependency
  - Current Liability to Assets
  - Profit / Net Income Ratio

The dataset is **highly imbalanced**, with far fewer bankrupt companies than
non-bankrupt ones.

---

## Data preprocessing
Key preprocessing steps:
- **Outlier treatment**  
  Values below the 15% quantile or above the 85% quantile were capped to reduce
  noise while preserving information.
- **Feature reduction**  
  Principal Component Analysis (PCA) was applied to reduce dimensionality  
  (from 95 features to ~20–27 components).
- **Class imbalance handling**  
  Borderline SMOTE was used to balance bankrupt and non-bankrupt classes.

---

## Models used
This is a **binary classification** problem.  
The following models were trained and compared:

- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier
- CatBoost Classifier
- LightGBM Classifier
- Stacking Classifier

Hyperparameters were optimized using **Grid Search**.

---

## Evaluation metrics
Models were evaluated using:
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrices

Tree-based models (Random Forest, XGBoost, CatBoost) showed the best performance.

---

## Results
- Tree-based models clearly outperform linear models
- Feature importance analysis highlights strong financial indicators related
  to bankruptcy risk
- The final models achieve strong predictive performance despite data imbalance

---

## Repository structure

```text
.
├── TaiwanBankruptcy.ipynb      # Main analysis notebook
├── code_snippets.ipynb         # Utility and experimentation code
├── data.csv                    # Dataset
├── presentation/               # Slides and final report
│   ├── ml-finance-project-presentation.pdf
│   ├── ml-finance-project-report.pdf
│   └── README.md
└── README.md

---

## Presentation & report
The full **project presentation slides** and **final report** are available in the  
[`presentation`](./presentation) folder.

---

## Academic context
This project was developed as part of a **Machine Learning / Finance academic course**.

This repository is an **individual presentation repository** of a **group project**  
and is shared for **educational and portfolio purposes only**.
