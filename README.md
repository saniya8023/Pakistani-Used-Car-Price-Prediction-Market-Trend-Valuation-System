# 🚗 AutoValuate PK — Used Car Price Prediction in Pakistan

AutoValuate PK is an end-to-end Machine Learning pipeline designed to predict used car prices in Pakistan. It processes raw vehicle listing data, engineers key market features, and applies ensemble learning algorithms to deliver accurate price estimates.

---

## 📌 Project Overview

Understanding used car prices in Pakistan can be difficult due to vehicle depreciation, varying conditions, and location-based trends. **AutoValuate PK** solves this by cleaning raw listings, creating domain-specific features, and training machine learning models to output reliable valuations.

* **Primary Algorithm:** Random Forest Regressor
* **Test Accuracy ($R^2$):** ~0.9230 (92.3% variance explained)
* **Optimization:** Hyperparameter tuning validated using `RandomizedSearchCV` with 5-Fold Cross-Validation.

---

## 🛠️ What is in this Project?

1. **Data Preprocessing & Cleaning:**
   * Handled missing values, removed duplicates, and managed outliers using Winsorization.
   * Encoded text-based categorical features (e.g., fuel type, transmission, city) into numerical inputs.

2. **Domain-Driven Feature Engineering:**
   * Expanded the feature space from **16 raw features** to **23 engineered features**.
   * Created temporal metrics (`days_since_post`, `post_month`, `is_weekend`).
   * Generated vehicle usage indicators (`usage_intensity`, vehicle age relative to mileage).
   * Applied regional city tiering to capture geographical demand differences.

3. **Multi-Model Benchmark & Selection:**
   * Evaluated multiple algorithms, including Linear Regression, XGBoost, and Random Forest.
   * **Random Forest** achieved the best stability and accuracy on unseen test data.

---

## 📊 Model Performance & Results

| Model | $R^2$ Score | RMSE (PKR) | Notes |
| :--- | :---: | :---: | :--- |
| **Random Forest (Final Model)** | **~0.9230** | **~1,348,207** | High accuracy, excellent generalization. |
| **XGBoost Regressor** | ~0.9094 | ~1,462,000 | Strong baseline performance. |
| **Random Forest (Tuned)** | ~0.9186 | ~1,351,938 | Confirmed default parameters perform optimally. |

---

## 📥 How to Access & Run

To run and explore this project, simply download the repository files:

1. Download the `Car_Price_Prediction.ipynb` notebook and dataset files directly from this repository.
2. Open the notebook in **Jupyter Notebook**, **VS Code**, or **Google Colab**.
3. Run all cells to execute the data processing, feature engineering, and model training pipelines.
