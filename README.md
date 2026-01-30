# 🚀 SpaceX Falcon 9 First Stage Landing Prediction

### Project Overview
The commercial space industry is becoming increasingly competitive, with SpaceX leading the way by reusing the first stage of their Falcon 9 rockets. Reusing a first stage saves approximately **$60 million** per launch. Determining whether the first stage will land successfully allows for accurate cost estimation and risk assessment for future launches.

**Goal:** This project develops an end-to-end machine learning pipeline to predict the landing outcome (Success/Failure) of the Falcon 9 first stage based on payload, launch site, and flight data.

---

## 📊 Executive Summary & Key Findings

After analyzing historical launch data and testing multiple classification algorithms, the project yielded the following insights:

* **Model Performance:** The **Decision Tree** and **Support Vector Machine (SVM)** models achieved the highest predictive accuracy of **~83.33%** on the test set.
* **Key Predictors:** Success is highly correlated with **Payload Mass** and **Orbit Type**. Lighter payloads to Low Earth Orbit (LEO) have higher success rates than heavy payloads to Geostationary Transfer Orbit (GTO).
* **Launch Sites:** KSC LC-39A has the highest success rate among the launch sites analyzed.

---

## 📂 Project Structure

This repository is organized as a data science pipeline, moving from raw data collection to predictive modeling.

| Step | Notebook | Description |
| :--- | :--- | :--- |
| **01** | [**Data Collection (API)**](01_Data_Collection_API.ipynb) | Requesting rocket launch data from the SpaceX REST API. |
| **02** | [**Web Scraping**](02_Data_Collection_WebScraping.ipynb) | Scraping Falcon 9 historical launch records from Wikipedia using BeautifulSoup. |
| **03** | [**Data Wrangling**](03_Data_Wrangling.ipynb) | Cleaning data, handling missing values (imputation), and converting categorical data. |
| **04** | [**EDA (SQL)**](04_EDA_SQL.ipynb) | Querying the dataset using SQL to find launch patterns and statistics. |
| **05** | [**EDA & Visualization**](05_EDA_Visualization.ipynb) | Visualizing success rates and correlations using Matplotlib and Seaborn. |
| **06** | [**Geospatial Analysis**](06_Geospatial_Analysis.ipynb) | Interactive maps using Folium to visualize launch site proximity and coastlines. |
| **07** | [**Machine Learning**](07_Machine_Learning_Models.ipynb) | Building and tuning classification models (Logistic Regression, SVM, KNN, Decision Tree). |

---

## 🛠️ Technologies Used
* **Languages:** Python, SQL
* **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Folium, BeautifulSoup
* **Tools:** Jupyter Notebooks, SpaceX API

---

## 📝 Methodology

1.  **Data Collection:** Used API requests to gather flight data and web scraping to fill in missing historical records.
2.  **Preprocessing:** Filtered for Falcon 9 launches, handled missing values, and applied One-Hot Encoding to categorical variables.
3.  **Exploratory Data Analysis (EDA):** Identified that success rates increase over time and vary significantly by orbit type.
4.  **Model Building:** Trained four models:
    * Logistic Regression
    * Support Vector Machine (SVM)
    * Decision Tree
    * K-Nearest Neighbors (KNN)
5.  **Evaluation:** Used `GridSearchCV` for hyperparameter tuning. All models achieved similar accuracy (~83%), but Decision Tree provided the best interpretability.

---

## 📜 Author
**[Omar Al-Ouran]**
* [LinkedIn Profile](https://www.linkedin.com/in/omar-al-ouran-101193215/) 
