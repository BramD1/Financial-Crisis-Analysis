# 📊 Project Title: Financial Analysis with Time Series Prediction
## 📝 Overview
This is a Financial Analysis project to check the stock price performance of a company known as AGG Power Solutions. In this notebook, I am aiming to gather insights regarding how the company performs during the 2008 financial crisis that is happening in the United States of America. The second part of the notebook is a time series prediction of the stock, where I predict how the company performs one yar after the recovery period (2010). This analysis will hopefully provide an interesting insight for potential investors of this company.

## Dashboard Link (Tableau):
https://public.tableau.com/app/profile/bramantyo.anandaru.suyadi/viz/AGG_stock_bram/Dashboard1?publish=yes

## 📂 Dataset
Source: https://www.kaggle.com/datasets/borismarjanovic/price-volume-data-for-all-us-stocks-etfs?resource=download 

Size: 3201 rows × 7 columns

Description: The data is gathered from Kaggle stock price dataset. The code of the stock I use is `agg.us.txt`

## 🔧 Technologies Used
Programming Language: Python

Libraries: Pandas, SciPy, Matplotlib, Seaborn, Plotly, Statsmodels, Scikit-learn.

Tools: Jupyter Notebook, Tableau

## 🚀 Implementation Part 1
### 1️ Data Loading & Cleaning
In this part, there are no missing value, only useless column which is OpenInt.
### 2️ Data Analysis 
I gathered insight which makes it possible to answer these questions:
1. What does the company look like in 6 years overall? (2005-2010)
2. What did the company look like 2 years before the crisis? (2005-2006)
3. What does the company look like 2 years during the crisis? (2007-2008)
4. During that time, which quarter and which year is the worst for the company so that we know when to buy or sell during crisis? 
5. What does the company look like 2 years after the crisis? (2009-2010)
6. Are there any correlation between trade volume and closing price?
7. Compare the difference of performance of those years (the 3 period divided to: before, during, and after crisis)
8. Bonus Part 2: Predict how the stock price will look like a year after 2010 (This is next part)
### 3 Result and Conclusion
Overall stock price seems to be always increasing, but there is a price fall detected in 2006 and 2008. Among the 3 period divided, the 2 years after the crisis seems to be the period where the company achieve the most success. The best time to invest according to the analysis in notebook was during the 4th quartile of 2008.

## 🚀 Implementation Part 2 (Time Series)
### 1 Data Loading and Filtering
This is the part where I extract the stock market data from the year 2005-2011 because I want to test if I can create a good forecasting model using time series.
### 2 Time Series EDA (Exploratory Data Analysis)
This Data Analysis is different compared to before because the insight I gathered here will only be used for the model training. The insight I want to see are:
1. Decomposition
2. Stationary
3. ACF & PACF
### 3 Model Training
The model that I choose for the prediction is SARIMA instead of ARIMA because of the seasonality detected during decomposition, and it has better score metric-wise (MAE & MAPE) compared to ARIMA
### 4 Model Evaluation
The score for the MAE is 1.674107, while the MAPE is 0.018089
### 5 Conclusion
The model has successfully predict an upward trend of the stock movement. If an investor was to buy the stock at 2010 or before, he/she is making a good decision.

📬 Connect With Me
💼 Linkedin: https://www.linkedin.com/in/bramantyo-anandaru-suyadi-0b9729208/ 