🩺 Breast Cancer Malignancy Prediction Using Cytological Cell Features and Machine Learning

This repository contains a bioinformatics and machine learning project that predicts whether a breast tumor is benign or malignant using quantitative cytological features obtained from fine-needle aspirate (FNA) samples.

The project follows a complete research-style workflow, including data preprocessing, exploratory analysis, model training, evaluation, and biological interpretation.

🧬 Biological Question

Which cytological features best distinguish benign from malignant breast tumors, and can machine learning accurately predict malignancy based on these features?

The nine FNA-derived features used here reflect cell morphology changes that occur during malignant transformation, such as nuclear enlargement, irregular shapes, abnormal chromatin, and mitotic activity.

📊 Dataset Overview

Dataset: Breast Cancer Wisconsin (Diagnostic)

Samples: 699 patient records

Input Features (9 cytological measurements):

clump_thickness

unif_cell_size

unif_cell_shape

marg_adhesion

single_epith_cell_size

bare_nuclei

bland_chrom

norm_nucleoli

mitoses

Target Label:

0 = benign

1 = malignant

The dataset is publicly available and not created in this project.

🧠 Analytical & ML Approach

The complete workflow is implemented in Jupyter Notebook and includes:

Preprocessing

Removal of non-informative ID column

Conversion of all values to numeric

Median imputation for missing values

StandardScaler for models requiring feature scaling (Logistic Regression, SVM)

Stratified 80/20 train–test split

ML Models Trained

Logistic Regression

Random Forest

Support Vector Machine (RBF kernel)

XGBoost

Model Evaluation

Accuracy, Precision, Recall, F1-score

ROC–AUC

Precision–Recall curves

Confusion matrices

GridSearchCV hyperparameter tuning

🔍 Bioinformatics-Relevant Interpretability & Visualizations

To connect ML insights to biological meaning, the project includes:

Correlation heatmap of cytological features

Boxplots comparing benign vs malignant morphology

PCA projection of samples

Feature importance from Random Forest & XGBoost

Permutation importance (model-agnostic)

Partial Dependence Plots (PDPs) for top predictors

Learning curve for model capacity evaluation

Bootstrap confidence intervals for AUC

These visualizations reveal which cellular abnormalities are strongest predictors of malignancy.

🏗️ Project Structure

Example directory layout:

.
├── cancer.csv                        # Dataset
├── Cancer_Bioinformatics_Unique.ipynb
├── README.md
├── AI_USAGE.md
├── requirements.txt                  # Added for reproducibility

🚀 Reproducibility

This repository includes a requirements.txt file listing all necessary Python packages so that anyone can recreate the exact computational environment.


📘 Summary

This project demonstrates how machine learning and cytological morphology can be combined to assist in breast cancer diagnosis.
The results show that SVM and XGBoost achieve the highest predictive performance, and important features such as bare nuclei, uniformity of cell size, and uniformity of cell shape play the largest roles in distinguishing malignant cells.
