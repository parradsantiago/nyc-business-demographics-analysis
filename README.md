# 🗽 NYC Business Density & Demographic Predictor

## 📋 Project Overview
This Data Science project analyzes the relationship between New York City's neighborhood demographics and local economic activity (Business vs. Individual licenses). Through a complete ETL process, Exploratory Data Analysis (EDA), and predictive modeling, the project identifies which demographic factors most accurately predict business density across different ZIP codes.

## 🚀 Key Findings
* **Predictive Accuracy:** Validated that demographic composition explains **91% of the variability** in commercial business density.
* **Business Correlation:** Identified a critical correlation of **0.90** between the Asian population percentage and corporate license density.
* **Individual Entrepreneurship:** Hispanic-majority areas exhibit the highest self-employment density (**6.2** vs. 2.1 in white-majority areas).
* **Market Leader:** "Home Improvement Salesperson" emerged as the dominant industry for individual licenses across all analyzed sectors.

## 🧠 Model Justification: Why Linear Regression?
Multiple Linear Regression was selected as the supervised learning algorithm for this analysis due to the following technical considerations:

1. **Nature of the Target:** Since the dependent variable (`biz_density`) is continuous, regression provides the most appropriate statistical framework.
2. **Interpretability:** Unlike "black-box" models, Linear Regression allows for the extraction of **exact coefficients** (e.g., the +295 impact factor for the Asian population), enabling data-driven business decisions.
3. **Efficiency:** As the EDA revealed strong linear relationships, this model achieved high precision (**R²: 0.91**) without the risk of overfitting associated with more complex architectures.
4. **Occam’s Razor:** The simplest explanation that fits the data is often the best. The model's performance confirmed that a linear approach was sufficient for high-granularity sociodemographic forecasting.

## 📊 Model Performance Metrics
* **R2 Score:** 0.9110
* **Mean Absolute Error (MAE):** 1.4491
* **Feature Coefficients (Top Impact):**
    * `percent_asian_non_hispanic`: +295.22
    * `percent_black_non_hispanic`: +216.73
    * `percent_white_non_hispanic`: +44.13

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** Pandas, Scikit-Learn, Matplotlib, Seaborn.
* **Tools:** Jupyter Notebooks / VS Code.

## 📁 Repository Structure
* `nyc_analysis.ipynb`: Main notebook containing the ETL flow, EDA, and Modeling.
* `nyc_business_final_dataset.csv`: Final processed dataset including model predictions.
* `README.md`: Project documentation and methodology.