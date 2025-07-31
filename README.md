# Walmart Sales Analysis & Forecasting

This repository contains a comprehensive analysis of Walmart's sales data, a dashboard for interactive insights, and a predictive model to forecast future weekly sales. The project leverages machine learning to provide actionable business intelligence.

## 📋 Table of Contents
* [🚀 Project Overview](#-project-overview)
* [📊 Dashboard](#-dashboard)
* [📈 Data Analysis & Insights](#-data-analysis--insights)
    * [Data Preprocessing](#data-preprocessing)
    * [Key Visualizations](#key-visualizations)
* [🧠 Predictive Modeling](#-predictive-modeling)
    * [Methodology](#methodology)
    * [Model Performance](#model-performance)
    * [Actual vs. Predicted Sales](#actual-vs-predicted-sales)
* [📁 Dataset](#-dataset)
* [📧 Contact](#-contact)
* [🔒 Security](#-security)

---

## 🚀 Project Overview

The primary goals of this project are:
* To perform an in-depth exploratory data analysis (EDA) to understand sales trends and key influencing factors.
* To create a dynamic dashboard for visualizing key performance indicators (KPIs) and data relationships.
* To develop and evaluate a machine learning model to accurately predict weekly sales.

## 📊 Dashboard

An interactive dashboard was created to provide a high-level overview of the sales data. It allows for filtering by month and holiday status to quickly explore different scenarios.

The dashboard includes key metrics such as:
* **Total Sales:** The overall sales volume.
* **Number of Stores:** The total number of stores in the dataset.
* **Average Fuel Price:** The average fuel price over the period.
* **Average Unemployment Rate:** The average unemployment rate across the stores.

It also features visualizations for:
* **Top 10 Stores by Sales:** A bar chart showing the highest-performing stores.
* **Sales Trends:** A line chart showing the sum and average of weekly sales over the years.
* **Sales by Holiday:** A pie chart illustrating the distribution of sales during holiday and non-holiday weeks.
* **Correlation Plots:** Scatter plots showing the relationship between sales and various economic factors (Unemployment, Fuel Price, CPI).
<img width="764" height="450" alt="image" src="https://github.com/user-attachments/assets/bb1ddcc3-cf9d-4cf9-8191-a1b0aaec5138" />


## 📈 Data Analysis & Insights

The analysis was performed using Python libraries such as `pandas`, `numpy`, `matplotlib`, and `seaborn`.

### Data Preprocessing
* The `Date` column was converted to datetime objects, and new features like `Year`, `Month`, and `Day` were extracted.
* Duplicate rows were checked and no duplicates were found.
* Log transformation was applied to the `Weekly_Sales` to normalize the distribution for better model performance.

### Key Visualizations
Several plots were generated to visualize the data distribution and relationships:

**Weekly Sales Trend Over Years**
The line plot below shows the overall weekly sales trend. The data reveals strong seasonality, with significant peaks and troughs throughout the year.

<img width="1233" height="547" alt="image" src="https://github.com/user-attachments/assets/0aee7fb9-5212-413a-8fbf-0a8b5c1c218d" />


**Distribution of Prediction Errors**
This histogram shows that the model's predictions are centered around an error of zero, indicating that the model is, on average, unbiased. The bell-shaped curve suggests that most predictions are close to the actual values, with larger errors being less frequent.

<img width="850" height="547" alt="image" src="https://github.com/user-attachments/assets/883186f5-ee51-4366-bf07-2c81da8aa8ed" />


## 🧠 Predictive Modeling

### Methodology
A machine learning model was developed to predict weekly sales.
* **Model:** A `RandomForestRegressor` was chosen for its robustness and ability to handle complex relationships in the data.
* **Feature Engineering:** Lag features (`Weekly_Sales_Lag_1`, `Weekly_Sales_Lag_2`, etc.) and a moving average feature (`Weekly_Sales_MA_4`) were created to capture temporal dependencies.
* **Train-Test Split:** The data was split based on a specific date (`01-08-2012`) to simulate a real-world forecasting scenario, with data before this date used for training and data after for testing.

### Model Performance
The model's performance was evaluated using standard regression metrics.

<img width="286" height="74" alt="image" src="https://github.com/user-attachments/assets/aa49744f-563d-415a-848e-9bb5c8af057a" />


The high R-squared value (`0.9908`) indicates that the model explains a significant portion of the variance in the weekly sales data. The MAE and RMSE values are also quite low relative to the sales figures, suggesting a high degree of predictive accuracy.

### Actual vs. Predicted Sales
The line plot below compares the actual weekly sales with the model's predictions on the test set. The model effectively captures the overall trend and major fluctuations in sales.

<img width="1466" height="701" alt="image" src="https://github.com/user-attachments/assets/999b8997-4a47-4749-b3d9-3565be262b20" />


## 📁 Dataset

The dataset used for this project is "Walmart Data Analysis and Forcasting" from Kaggle.
* **Dataset Link:** [https://www.kaggle.com/datasets/asahu40/walmart-data-analysis-and-forcasting](https://www.kaggle.com/datasets/asahu40/walmart-data-analysis-and-forcasting)
* The dataset contains historical sales data for 45 Walmart stores, including key features like weekly sales, store size, holiday flags, and macroeconomic indicators (temperature, fuel price, CPI, and unemployment).

---

## 📧 Contact

For any questions, suggestions, or collaboration opportunities, feel free to contact me:
* **Email:** mridulchawla20@gmail.com

## 🔒 Security

This project is for educational and analytical purposes only. It does not handle any sensitive data, and all data used is publicly available from Kaggle. No security vulnerabilities are known or intended.
