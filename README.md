# 🩺 Cancer Prediction using Machine Learning
### Clinical Decision Support for Benign vs. Malignant Classification

<p align="center">
<img src="https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python">
<img src="https://img.shields.io/badge/Scikit--Learn-ML-F7931E?style=for-the-badge&logo=scikitlearn">
<img src="https://img.shields.io/badge/XGBoost-High%20Accuracy-2EAD33?style=for-the-badge">
<img src="https://img.shields.io/badge/Metrics-ROC--AUC%20|%20F1-8E44AD?style=for-the-badge">
<img src="https://img.shields.io/badge/Health%20AI-Diagnostic%20Assistant-red?style=for-the-badge">
</p>

---

## 🌟 Overview

Early diagnosis is the most critical factor in increasing survival rates for cancer patients. This project develops a high-precision **Supervised Machine Learning** system designed to distinguish between **Benign** (non-cancerous) and **Malignant** (cancerous) tumors. By analyzing cellular features such as texture, radius, and symmetry, the model acts as a reliable second-opinion tool for healthcare professionals.



---

## 🎯 Key Features

* ✅ **Binary Classification:** Specializes in high-stakes differentiation between benign and malignant states.
* ✅ **Feature Importance Analysis:** Identifies which medical markers (e.g., clump thickness, bare nuclei) contribute most to the diagnosis.
* ✅ **Multi-Model Bake-off:** Benchmarks Logistic Regression, Decision Trees, Random Forest, and XGBoost to ensure the highest clinical reliability.
* ✅ **Holistic Evaluation:** Prioritizes **Recall** and **F1-Score** to minimize dangerous False Negatives in a medical context.

---

## 🧠 Tech Stack

| Category | Tools |
| :--- | :--- |
| **Language** | Python 3.8+ |
| **ML Framework** | Scikit-learn, XGBoost |
| **Data Handling** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn |
| **Environment** | Jupyter Notebook |

---

## 📁 Project Structure

```bash
Cancer_Prediction/
├── src/
│   └── Cancer_Prediction.ipynb    # Main pipeline: cleaning, training, & evaluation
├── docs/
│   ├── Cancer_Prediction_intro.txt  # Project goals & clinical context
│   └── Cancer_Prediction_report.txt # Final metrics & model comparison
├── requirements.txt                 # Project dependencies
└── README.md                        # Documentation

```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone [https://github.com/G-Narendra/Cancer_Prediction.git](https://github.com/G-Narendra/Cancer_Prediction.git)
cd Cancer_Prediction

```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt

```

### 3️⃣ Start the Analysis

```bash
jupyter notebook Cancer_Prediction.ipynb

```

---

## 📊 Methodology & Evaluation

### Data Preprocessing

The model processes high-dimensional medical data (such as the Wisconsin Breast Cancer dataset), focusing on:

* **Feature Scaling:** Normalizing cell measurements to a uniform range for better model convergence.
* **Correlation Mapping:** Identifying multi-collinearity between features like `radius` and `perimeter`.

### Performance Metrics

In medical AI, **Recall** is prioritized over Accuracy to ensure no malignant cases are missed:

* **ROC-AUC Score:** Measures the model's ability to distinguish between classes.
* **Confusion Matrix:** Provides a clear breakdown of True Positives and False Negatives.
* **Precision/Recall:** Balances the cost of over-diagnosis vs. missed diagnosis.

---

## 🚀 Future Roadmap

* [ ] **Explainable AI (XAI):** Integrating SHAP or LIME to explain *why* a specific prediction was made.
* [ ] **Cross-Cancer Support:** Extending the model to handle lung and prostate cancer datasets.
* [ ] **Cloud Deployment:** Building a secure API to allow real-time diagnostic testing via a web interface.

---

## Engineering Decisions & Challenges Solved

| Challenge | Decision | Why |
|---|---|---|
| Binary classification with medical consequences | Multiple model comparison (Logistic Regression, SVM, Random Forest, XGBoost) | No single model is universally best — comparing them reveals which approach handles this specific data distribution best |
| Feature scaling affects distance-based models | StandardScaler applied before SVM and KNN, not before tree models | Trees are scale-invariant; SVM/KNN are not — applying scaling uniformly wastes computation and can hurt tree models |
| High-dimensional feature space | PCA for dimensionality reduction + feature importance analysis | Reduces noise and computation while identifying which features actually drive predictions |
| Model interpretability vs accuracy trade-off | Report both accuracy metrics AND feature importance for the best model | Medical stakeholders need to understand predictions, not just trust them |

## 👨‍💻 Author

**Narendra (G‑Narendra)** AI | ML | Python | Full Stack | GenAI Enthusiast

📧 [Email Me](mailto:narendragandikota2540@gmail.com) | 💼 [LinkedIn](https://linkedin.com/in/g-narendra/) | 👨‍💻 [GitHub](https://github.com/G-Narendra)

---

<p align="center">⭐ If you find this project useful, feel free to give it a star! 🚀</p>
