# 🩺 Cancer Prediction using Machine Learning

**Binary classification of breast cancer diagnosis (benign vs. malignant) using Logistic Regression.**

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-ML-F7931E.svg)](https://scikit-learn.org/)
[![License MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

---

## 🎯 Problem Statement

Breast cancer is one of the most common cancers worldwide. Early and accurate diagnosis is critical for treatment outcomes. Pathologists manually examine tissue samples under microscopes, which is time-consuming and subject to inter-observer variability. A machine learning model that can classify tumors as benign or malignant based on computed features (radius, texture, perimeter, area, etc.) could assist pathologists by providing a second opinion.

The Wisconsin Breast Cancer Dataset contains 569 instances with 30 numeric features computed from digitized images of fine needle aspirates (FNA) of breast masses. Features describe characteristics of the cell nuclei present in the image, such as radius, texture, perimeter, area, smoothness, compactness, concavity, concave points, symmetry, and fractal dimension.

---

## 📊 What I Built

A simple ML classification pipeline:

1. **Data Loading**: Load the Cancer dataset from GitHub (YBIFoundation/Dataset)
2. **Preprocessing**: Drop ID and unnamed columns, define target (diagnosis) and features
3. **Train/Test Split**: 70/30 split with random_state=2529 for reproducibility
4. **Model Training**: Logistic Regression with max_iter=5000
5. **Evaluation**: Confusion matrix, accuracy score, classification report

### Key Results

| Metric | Value |
|---|---|
| **Model** | Logistic Regression |
| **Train Size** | 70% |
| **Test Size** | 30% |
| **Evaluation** | Confusion Matrix, Accuracy, Classification Report |

---

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| **Language** | Python 3.8+ |
| **Data Processing** | Pandas |
| **ML Framework** | Scikit-Learn |
| **Model** | Logistic Regression |
| **Evaluation** | Confusion Matrix, Accuracy, Classification Report |

---

## 📁 Project Structure

```
Cancer_Prediction/
├── Cancer_Prediction.ipynb         # Main notebook with full pipeline
├── ml_evaluation_utils.py          # Evaluation utilities (CV, confidence intervals)
├── README.md
└── LICENSE
```

---

## 🔧 How to Run

```bash
# Install dependencies
pip install pandas scikit-learn jupyter

# Run the notebook
jupyter notebook Cancer_Prediction.ipynb
```

---

## 🧪 Engineering Decisions

| Decision | Rationale |
|---|---|
| **Logistic Regression** | Simple, interpretable model that works well for binary classification with structured features. Good baseline before trying more complex models. |
| **70/30 Split** | Standard split ratio for small-medium datasets. Provides enough data for training while reserving sufficient data for evaluation. |
| **max_iter=5000** | Default max_iter (100) was insufficient for convergence with this dataset. Increased to ensure the optimizer finds the optimal solution. |
| **Dropped 'Unnamed: 32'** | This column was empty/null in the dataset — dropping it prevents noise in the model. |
| **Random State 2529** | Fixed random state ensures reproducibility of the train/test split across runs. |

---

## ⚠️ Limitations

- **No cross-validation**: The current pipeline uses a single train/test split. Cross-validation would provide more reliable performance estimates.
- **No confidence intervals**: Model predictions lack uncertainty quantification. Bootstrapped confidence intervals would be needed for clinical use.
- **No feature scaling**: Logistic Regression is sensitive to feature scales. StandardScaler should be applied for optimal performance.
- **Simple model**: Logistic Regression may not capture non-linear relationships. Ensemble methods (XGBoost, Random Forest) could improve performance.

---

## ⚠️ Disclaimer

This is an educational project for learning ML concepts. It is not intended for clinical use. Medical diagnosis requires qualified professionals and validated clinical tools.

---

*Built as part of MSc Data Science coursework — demonstrating fundamental ML classification pipeline.*
