# Foecasting# Predictive Analytics for Oncology Sales: Leveraging Prophet, XGBoost, and Ensemble Modeling

In the highly competitive and dynamic pharmaceutical landscape, forecasting sales with precision can make or break market strategies. This project demonstrates how advanced machine learning techniques, like **Prophet**, **XGBoost**, and **Ensemble Learning**, can be used to predict oncology sales, with a focus on incorporating **external factors** such as competitor activity, economic conditions, and healthcare spending. 

The goal is to provide accurate, actionable sales forecasts that can help pharmaceutical companies optimize their strategies in real-time, from production planning to marketing.

## Project Overview

### 1. **Synthetic Data Generation**
This project generates synthetic datasets simulating oncology sales, incorporating:
- **Monthly sales data** with seasonality, competitor activity, and market changes.
- **Competitor activity**: Product launches, marketing campaigns, and pricing strategies.
- **External factors**: Economic indicators such as **GDP growth** and **healthcare spending**, which can significantly impact sales.

### 2. **Forecasting Models**
We employ three powerful models to forecast future oncology sales:
- **Prophet**: A robust time-series model that takes into account seasonality, holidays, and external regressors (e.g., competitor launches, GDP growth).
- **XGBoost**: A tree-based model, trained to predict sales by capturing complex, non-linear relationships between sales and various external factors.
- **Ensemble Learning**: Combining the predictions from Prophet and XGBoost using a **linear regression** meta-model. This approach aims to improve overall forecast accuracy by leveraging the strengths of both models.

### 3. **Model Evaluation**
The performance of each model is evaluated using **Mean Absolute Percentage Error (MAPE)**, a key metric in forecasting accuracy:
- Lower MAPE values indicate higher accuracy.
- The **Ensemble Meta-model** is expected to outperform individual models, combining the benefits of both **time-series** and **machine learning** techniques.

### 4. **Visualization**
We provide visual insights into:
- **Actual vs. predicted sales** for the last 12 months.
- Comparative performance of **Prophet**, **XGBoost**, and the **Ensemble Meta-model**.

## How to Run the Project
1. **Clone the repository** and navigate to the project directory.
2. **Install required dependencies** using the following command:

```bash
pip install pandas numpy matplotlib seaborn prophet xgboost scikit-learn
python sales_forecasting.py

## Results

The performance of the models was evaluated using **Mean Absolute Percentage Error (MAPE)**, where a lower MAPE indicates higher forecasting accuracy. Here are the results:

- **Prophet Model**: MAPE = **5.56%**
  - Prophet performs well in handling seasonality and external factors, providing a reliable forecast with a low error margin.
  
- **Tuned XGBoost Model**: MAPE = **8.37%**
  - Although XGBoost excels in capturing non-linear patterns, its performance here was slightly worse than Prophet's due to limited features and potential overfitting.

- **Ensemble Meta-model**: MAPE = **4.28%**
  - The **Ensemble Meta-model**, which combines the strengths of both Prophet and XGBoost, provides the most accurate forecasts, with a **significant improvement** in forecast accuracy.

### Conclusion:
The **Ensemble Meta-model** outperformed both **Prophet** and **XGBoost** individually, validating the power of combining different model types for more reliable and robust predictions in sales forecasting. The **MAPE of 4.28%** is indicative of a highly accurate model, making it valuable for strategic decision-making in the pharmaceutical industry.
