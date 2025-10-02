# SpaceX-Falcon-9-first-stage-Landing-Prediction
Data science &amp; ML labs analyzing SpaceX launch data with Python notebooks and visualizations.
# 🚀 IBM Data Science Capstone Project: SpaceX Launch Success Prediction

## 🌟 Executive Summary

This project aims to analyze historical SpaceX launch data to understand factors influencing launch success and develop a predictive classification model.

* **Goal:** To accurately predict the outcome (`Success` or `Failure`) of a SpaceX launch based on pre-flight and mission parameters.
* **Key Finding:** After hyperparameter tuning with `GridSearchCV`, **all four classification models (Logistic Regression, SVM, Decision Tree, and K-Nearest Neighbors) achieved a final test accuracy of approximately 83.33%**.
* **Most Important Features:** Exploratory Data Analysis (EDA) showed that **Payload Mass** and **Orbit Type** are the strongest predictors of success.
* **Model Performance:** The best-performing model (KNN/SVM/LR) demonstrated **zero False Negatives**, meaning the model never misclassified a successful launch as a failure.

## 🛠️ Methodology & Techniques

This project followed the standard data science lifecycle, incorporating several key technologies and methods:

1.  **Data Collection:** Used the **SpaceX REST API** and **Web Scraping** to collect raw launch data.
2.  **Data Wrangling & Feature Engineering:** Cleaned, processed, performed **One-Hot Encoding** (for categorical features), and **Standardization** (for numerical features $\mathbf{X}$).
3.  **Exploratory Data Analysis (EDA):** Performed analysis using visualizations (Matplotlib/Seaborn) and **SQL queries** to derive key insights (e.g., success rates by orbit and launch site).
4.  **Interactive Visual Analytics:** Created a **Folium** interactive map for proximity analysis and a **Plotly Dash** dashboard for filtering and dynamic visualization.
5.  **Predictive Modeling:** Used Scikit-learn to train and tune four models (LR, SVM, DT, KNN) using **10-fold Cross-Validation (`cv=10`)** via `GridSearchCV`.

