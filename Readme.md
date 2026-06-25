# AI/ML Engineering Internship — DevelopersHub Corporation

This repository contains my submission for the AI/ML Engineering Internship tasks.
Out of 6 available tasks, I completed **Tasks 1, 3, and 6**.

---

## Task 1: Exploring and Visualizing the Iris Dataset

**Objective:**
Load, inspect, and visualize the Iris dataset to understand feature distributions and relationships between species.

**Dataset:**
Iris Dataset (loaded via seaborn)

**Approach:**
- Loaded and inspected data using pandas (`.shape`, `.info()`, `.describe()`)
- Visualized feature relationships using pairplots
- Examined distributions using histograms
- Identified outliers using box plots
- Generated a correlation heatmap between numeric features

**Key Findings:**
- `petal_length` and `petal_width` show the strongest correlation and most clearly separate the three species visually.
- This explains why simple linear models (e.g., Logistic Regression) achieve very high accuracy on this dataset — the classes are nearly linearly separable on just two features.

**Notebook:** `task 1/task.ipynb`

---

## Task 3: Heart Disease Prediction

**Objective:**
Predict whether a patient is at risk of heart disease based on health metrics, using binary classification.

**Dataset:**
UCI Heart Disease Dataset (via Kaggle, combined multi-source version)

**Models Applied:**
- Logistic Regression (with feature scaling)
- Decision Tree Classifier (max depth 4)

**Approach:**
- Checked and handled missing values
- Performed EDA: class distribution check, correlation heatmap
- Split data with stratified sampling to preserve class balance
- Scaled features for Logistic Regression (distance-based model); left Decision Tree unscaled (tree-based model doesn't require it)
- Evaluated using Accuracy, Confusion Matrix, Classification Report, and ROC-AUC
- Extracted feature importance from the Decision Tree

**Key Results:**
- Most important predictive features: [list top 2-3 from your feature importance chart]

**Key Insight:**
ROC-AUC was used alongside accuracy because, in a medical context, false negatives (missed disease cases) carry more risk than false positives — a single accuracy number doesn't capture this trade-off.

**Notebook:** `task 3/task3.ipynb`

---

## Task 6: House Price Prediction

**Objective:**
Predict house prices based on property features (area, bedrooms, location, etc.) using regression.

**Dataset:**
House Price Prediction Dataset (via Kaggle)

**Models Applied:**
- Linear Regression (with feature scaling)
- Gradient Boosting Regressor

**Approach:**
- Identified and one-hot encoded categorical features (e.g., location, furnishing status)
- Scaled numerical features for Linear Regression
- Trained Gradient Boosting on raw features (tree-based, scale-invariant)
- Evaluated using MAE, RMSE, and R²
- Visualized predicted vs actual prices
- Extracted top 10 important features from Gradient Boosting

**Key Results:**
- Gradient Boosting outperformed Linear Regression, since it captures non-linear relationships and feature interactions that a linear model cannot represent.

**Notebook:** `task 6/task6.ipynb`

---

## Tech Stack
- Python, pandas, NumPy
- scikit-learn
- matplotlib, seaborn
- Jupyter Notebook

## Author
Taha Tabassum — [github.com/tahatabassum](https://github.com/tahatabassum)