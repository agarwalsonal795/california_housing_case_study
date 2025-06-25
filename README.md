# 🏠 California Housing Price Prediction Using Random Forest Regression
**Author:** Sonal Agarwal

This study focuses on predicting California housing prices using machine learning 
techniques, with data sourced from Kaggle. We tested 


This repository contains a **machine learning project** focused on **predicting California housing prices** using **Random Forest Regression**. The project leverages the **California Housing dataset** from Kaggle and compares multiple regression models, including Linear Regression, Ridge, Lasso, Decision Tree, and Random Forest. Among these, Random Forest emerged as the most accurate, achieving a validation R² score of 0.83. Its strength lies in handling complex patterns, reducing overfitting, and effectively processing both numerical and categorical data. Through preprocessing, feature engineering, and tuning, we enhanced model performance, highlighting the value of machine learning in tackling real-world challenges. This research offers important insights for professionals in real estate, urban development, and policy-making, demonstrating how machine learning can effectively forecast housing prices and support informed decision-making.

---

## 📌 Project Overview

- **Objective:** Predict **median house values** in California using **supervised learning** techniques.
- **Dataset:**  
  - Source: [California Housing Dataset (Kaggle)](https://www.kaggle.com/datasets/camnugent/california-housing-prices)  
  - Size: **20,640 rows**, **9 features**  
  - Features include: **median income**, **housing age**, **rooms**, and **ocean proximity**.

- **Models Compared:**
  - Linear Regression
  - Ridge Regression
  - Lasso Regression
  - Decision Tree
  - Random Forest Regression (Best Performer)

---

## 🛠️ Methodology

### 1. Data Preprocessing

- **Missing Values:**  
  Imputed missing values in `total_bedrooms` with the **median**.

- **Feature Engineering:**  
  Created new features:  
  - `rooms_per_household`  
  - `bedrooms_per_room`  
  - `population_per_household`

- **Categorical Encoding:**  
  - Converted `ocean_proximity` into numerical columns via **one-hot encoding**.
  - Removed rare categories for clarity.

- **Feature Scaling:**  
  - Standardized **numerical features** for fair comparison across models.

---

### 2. Exploratory Data Analysis (EDA)

- Analyzed **feature distributions** and **correlations**.
- Identified **`median_income`** as the most influential feature on housing prices.
- Visualized:
  - Data distributions
  - Missing values
  - Feature correlation heatmaps

---

### 3. Model Training and Evaluation

- **Train-Test Splits:**  
  Tested various splits: **80/20**, **75/25**, **85/15**, **70/30**.

- **Evaluation Metrics:**  
  - **RMSE (Root Mean Squared Error)**
  - **R² Score**

- **Cross-Validation:**  
  Ensured **model robustness** across folds.

- **Hyperparameter Tuning:**  
  Performed **GridSearchCV** to optimize:  
  - `n_estimators`  
  - `max_depth`  
  - `min_samples_leaf`

---

### 4. Model Comparison

| Model              | Validation R² | Strengths                          | Weaknesses                 |
|--------------------|---------------|------------------------------------|----------------------------|
| Linear Regression  | ~0.65         | Simple, interpretable              | Cannot capture non-linearities |
| Ridge Regression   | ~0.65         | Reduces overfitting               | Limited for non-linear data    |
| Lasso Regression   | ~0.65         | Feature selection                 | Struggles with non-linearities |
| Decision Tree      | 1.0 (Overfit) | Captures non-linear patterns      | Prone to overfitting           |
| **Random Forest**  | **0.83**      | Handles non-linearities, reduces overfitting, works with mixed data | Computationally intensive |

---

## ✅ Key Findings

- **Best Model:**  
  **Random Forest Regression**, achieving:  
  - **Validation R² Score:** 0.83  
  - **RMSE:** ~$23,950  

- **Feature Importance:**  
  Top predictors:  
  - Median Income  
  - House Age  
  - Average Rooms  

- **Scalability:**  
  Robust for **medium-sized datasets**, adaptable to **other regions** or **similar prediction tasks**.

---

## 🚧 Limitations & Future Work

### Limitations:

- **Computationally intensive**, especially with large hyperparameter grids.
- Less **interpretable** compared to linear models.
- Dataset has a **price cap at $500,000**, limiting prediction for high-end properties.

### Future Scope:

- Explore **advanced ensemble models**: XGBoost, LightGBM.
- Apply **resampling techniques** to handle any **data imbalance**.
- Investigate **feature selection** for model simplification and efficiency.

---

## 🚀 Usage

### 1. Clone the Repository:

```bash
git clone https://github.com/your-username/california-housing-prediction.git
cd california-housing-prediction
```

2. Run the Analysis:
Open and run the main Jupyter notebook or Python script for:
- Data preprocessing
- Model training
- Evaluation and visualization of results

📚 References
California Housing Dataset - Kaggle

Scikit-learn Documentation

📜 License
This project is for educational and research purposes only.
