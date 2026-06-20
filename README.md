# Retail-Sales-Forecasting-Using-VARMAX-Model-with-Marketing-and-Customer-Behavior-Factors

https://colab.research.google.com/drive/1laaf_hhhg4h3kDi68eWvZGDwX7M25k2k#scrollTo=gzE0NKvcvRDu

## Project Overview

This project focuses on forecasting retail sales using the VARMAX (Vector Autoregressive Moving Average with Exogenous Variables) model. The objective is to predict future sales performance by considering both internal sales variables and external business factors such as discounts, marketing expenditure, customer footfall, online orders, and economic conditions.

The VARMAX model is particularly suitable for this problem because retail sales are influenced not only by historical sales patterns but also by external variables that directly impact customer purchasing behavior.

---

## Dataset Information

**Dataset Name:** Retail Sales Forecast Dataset

**Total Records:** 25,000 Transaction Records

**Data Type:** Retail Business Transactions

### Variables Used

### Endogenous Variables (Forecast Targets)

* Sales_Amount
* Units_Sold

### Exogenous Variables (External Factors)

* Discount_Percent
* Marketing_Spend
* Customer_Footfall
* Online_Orders
* Economic_Index

---

## Project Objectives

* Forecast future retail sales performance.
* Analyze the impact of external business factors on sales.
* Evaluate forecasting accuracy using statistical metrics.
* Generate future sales predictions for business decision-making.

---

## Technologies Used

* Python
* Google Colab
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Statsmodels
* Scikit-Learn

---

## Methodology

### 1. Data Preprocessing

* Loaded retail sales dataset.
* Converted date column to datetime format.
* Aggregated transaction data into daily observations.
* Handled missing values using Forward Fill (ffill).

### 2. Exploratory Data Analysis

* Visualized sales trends.
* Generated correlation heatmap.
* Identified relationships between variables.

### 3. Stationarity Testing

The Augmented Dickey-Fuller (ADF) Test was applied to verify stationarity.

| Variable     | Result     |
| ------------ | ---------- |
| Sales_Amount | Stationary |
| Units_Sold   | Stationary |

Since both variables were stationary, differencing was not required.

---

## VARMAX Model

### Model Configuration

VARMAX(2,1)

Where:

* p = 2 (Autoregressive Order)
* q = 1 (Moving Average Order)

The model incorporates both historical sales information and external business variables.

---

## Correlation Analysis Findings

| Relationship                     | Correlation |
| -------------------------------- | ----------- |
| Customer_Footfall ↔ Units_Sold   | 0.83        |
| Customer_Footfall ↔ Sales_Amount | 0.61        |
| Online_Orders ↔ Units_Sold       | 0.68        |
| Online_Orders ↔ Sales_Amount     | 0.50        |
| Discount_Percent ↔ Sales_Amount  | 0.04        |

### Key Insight

Customer Footfall and Online Orders were identified as the strongest drivers of retail sales performance.

---

## Model Performance

### Information Criteria

| Metric         | Value     |
| -------------- | --------- |
| Log Likelihood | -18852.36 |
| AIC            | 37758.72  |
| BIC            | 37895.42  |
| HQIC           | 37810.28  |

### Forecast Accuracy Metrics

| Metric | Value   |
| ------ | ------- |
| MAE    | 7424.84 |
| RMSE   | 9718.66 |

---

## Future Forecast

A 7-day sales forecast was generated using assumed future values of:

* Discount Percentage
* Marketing Spend
* Customer Footfall
* Online Orders
* Economic Index

### Forecast Observation

* Sales are expected to gradually decline and stabilize.
* Units sold are expected to remain around 138–150 units per day.
* Overall business demand remains stable.

---

## Results

### Achievements

* Successfully built a VARMAX forecasting model.
* Evaluated model performance using statistical metrics.
* Analyzed the impact of external business factors.
* Generated future retail sales forecasts.
* Supported data-driven business decision-making.

---

## Conclusion

The VARMAX(2,1) model successfully forecasted retail sales using both internal sales variables and external business factors. The ADF test confirmed stationarity, eliminating the need for differencing. Correlation analysis revealed that Customer Footfall and Online Orders are the most influential variables affecting sales performance. The model achieved satisfactory forecasting performance with an MAE of 7424.84 and RMSE of 9718.66. Future forecasts indicate stable demand and sales patterns, demonstrating the effectiveness of VARMAX for retail sales forecasting and business planning.

---

## Prepared by

**Sugumar Ranganathan, M.B.A.,**

