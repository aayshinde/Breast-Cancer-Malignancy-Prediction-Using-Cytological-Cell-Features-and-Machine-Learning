# Breast Cancer Malignancy Prediction Using Cytological Cell Features and Machine Learning

This repository contains a **bioinformatics / biomedical ML project** that predicts whether a breast tumor is **benign or malignant** using **cytological features** extracted from fine-needle aspirate (FNA) samples.

The project focuses on:
- Using **machine learning** to classify tumors
- Understanding **which cell-level abnormalities** are most associated with malignancy
- Demonstrating a **research-grade analysis pipeline** suitable for a course project

---

## 🧬 Biological Question

> **Which cytological cell features best distinguish benign from malignant breast tumors, and can machine learning accurately predict malignancy based on these features?**

The features used (e.g., clump thickness, uniformity of cell size/shape, bare nuclei, mitoses) are established **morphological hallmarks of cancer** and are routinely evaluated in cytopathology.

---

## 📊 Dataset

- **Type:** Breast cancer cytology dataset (tabular, CSV)
- **Samples:** 699 patient records
- **Features:** 9 numerical cytological measurements + 1 class label  
  (benign = 0, malignant = 1)
- **Typical features include:**
  - `clump_thickness`
  - `unif_cell_size`
  - `unif_cell_shape`
  - `marg_adhesion`
  - `single_epith_cell_size`
  - `bare_nuclei`
  - `bland_chrom`
  - `norm_nucleoli`
  - `mitoses`

> **Note:** The raw dataset is not created by this project; it is a standard, publicly available diagnostic dataset.

---

## 🧠 Analytical Approach

**Machine Learning (Logistic Regression, Random Forest, SVM, XGBoost)**

The analysis is implemented in a Jupyter Notebook and includes:

- Data cleaning & preprocessing:
  - ID column removal (if present)
  - Conversion of numeric-like columns
  - Missing value imputation (median)
  - Feature scaling (for LR/SVM)
  - Train–test split with stratification
- Supervised classification using:
  - **Logistic Regression**
  - **Random Forest**
  - **Support Vector Machine (RBF)**
  - **XGBoost**
- Model selection & evaluation:
  - Cross-validation & basic hyperparameter tuning (`GridSearchCV`)
  - Metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC
  - Confusion matrix
  - ROC and Precision–Recall curves

---

## 🔍 Interpretability & Bioinformatics-Relevant Visualizations

To make the model **biologically meaningful**, the project includes:

- **Correlation heatmap** of cytological features
- **Boxplots** of key features split by class (benign vs malignant)
- **PCA plot** to visualize sample separation in feature space
- **Feature importance**:
  - Random Forest feature importances
  - XGBoost feature importances
- **Permutation importance** to see which features affect AUC
- **Partial Dependence Plots** (PDP) for top features, showing how a feature’s value changes the predicted risk
- **Learning curve** to see performance vs train size
- **Bootstrap 95% confidence interval** for test AUC

These visualizations help connect machine learning results back to **biological interpretation**.

---

## 🏗️ Project Structure

Example structure (may vary slightly):

```text
.
├── cancer.csv                      # Dataset (not always committed)
├── Cancer_Bioinformatics_Unique.ipynb
├── README.md
├── AI_USAGE.md
└── (optional) figures/             # Saved plots (ROC, PR, PCA, etc.)
