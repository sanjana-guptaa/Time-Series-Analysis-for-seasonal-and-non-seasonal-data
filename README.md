# Time Series Analysis

This repository contains two projects demonstrating time series analysis using the Box-Jenkins methodology. The first project predicts Bitcoin prices (non-seasonal data), and the second forecasts airline passenger traffic (seasonal data). 

---

## **Project 1: Bitcoin Price Prediction (Non-Seasonal Data)**

### **Motivation and Introduction**
Bitcoin is known for its high volatility and global financial influence. Predicting Bitcoin prices is essential for traders, investors, and financial analysts to manage risks and strategize effectively.

### **Data Preprocessing**
- Aggregated hourly Bitcoin price data into daily intervals.
- Key variables:
  - Open, High, Low, Close prices.
  - Trading volume.
- Steps:
  - Handled missing values.
  - Converted timestamps to readable date formats.

### **Box-Jenkins Methodology**
- **Stationarity Check**:
  - Applied Augmented Dickey-Fuller (ADF) test.
  - Used first differencing to achieve stationarity.
- **Model Identification**:
  - Selected ARIMA(0,1,0) based on AIC and BIC.
- **Model Diagnostics**:
  - Evaluated residuals using Ljung-Box test.

### **Forecasting**
- Forecasted Bitcoin prices for the next 30 days using ARIMA(0,1,0).
- The forecast highlights Bitcoin's high volatility.
  
### **Statistical and Practical Conclusions**
- The model captures short-term trends effectively.
- Reliable for short-term financial planning but limited for long-term predictions due to Bitcoin's erratic nature.

---

## **Project 2: Airline Passenger Traffic Prediction (Seasonal Data)**

### **Motivation and Introduction**
Airline passenger traffic exhibits seasonal patterns, peaking during holidays and summers. Accurate forecasting aids airlines in resource optimization, scheduling, and customer service.

### **Data Preprocessing**
- Dataset: Monthly international airline passenger totals (1949–1960).
- Key attributes:
  - Month of observation.
  - Number of passengers.
- Steps:
  - Handled missing values.
  - Applied log transformation to stabilize variance.

### **Box-Jenkins Methodology**
- **Stationarity Check**:
  - ADF test indicated non-stationarity; applied seasonal differencing.
- **Model Identification**:
  - Selected SARIMA(0,1,1)(0,1,1)[12] based on AIC and BIC.
- **Model Diagnostics**:
  - Residuals passed Ljung-Box test and revealed no significant patterns.

### **Forecasting**
- Forecasted the next 24 months of passenger traffic.
- Seasonal peaks and troughs were accurately predicted.

### **Statistical and Practical Conclusions**
- The model effectively captures seasonal patterns.
- Provides actionable insights for resource allocation and strategic planning.

---

# License
This repository is licensed under the MIT License.
