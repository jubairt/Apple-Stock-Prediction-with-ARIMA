# 📈 Time Series Forecasting of Apple Inc. (AAPL) Stock Prices Using ARIMA

## 🧠 Project Overview  
This project applies **Time Series Analysis** with the **ARIMA model** to forecast the closing stock prices of **Apple Inc. (AAPL)**. The goal is to build a reliable predictive model, validate statistical assumptions, and provide clear visual insights into future stock price trends.

---

## 🚀 Objectives  
- Analyze historical stock prices of Apple Inc.  
- Test and ensure **stationarity** of the time series.  
- Identify optimal **ARIMA parameters (p, d, q)** using ACF and PACF plots.  
- Train the ARIMA model to forecast closing prices.  
- Evaluate model performance through residual diagnostics.  
- Generate a **30-day forward forecast** with confidence intervals.  

---

## 🧰 Technologies Used  
- **Language:** Python 3.x  
- **IDE:** VS Code  

**Libraries:**  
- `pandas`, `numpy` – Data wrangling  
- `matplotlib`, `seaborn` – Visualizations  
- `statsmodels` – Statistical modeling & ARIMA  
- `yfinance` – Stock data retrieval  
- `warnings`, `datetime` – Utilities  

---

## 📚 Dataset  
- **Ticker:** AAPL (Apple Inc.)  
- **Time Frame:** January 2020 – January 2025  
- **Frequency:** Daily stock data (`Open`, `High`, `Low`, `Close`, `Volume`)  
- **Focus:** The analysis is performed on the **Closing Prices**.  

---

## 🔍 Exploratory Data Analysis (EDA)  
- Visualized daily closing prices to identify **trends and volatility**.  
- Confirmed no missing values in the dataset.  
- Observed an **overall upward trend** with occasional seasonal-like patterns and sudden market movements.  

---

## 📉 Stationarity Check  
- Applied **Augmented Dickey-Fuller (ADF) test** on the original series → found **non-stationarity** (high p-value).  
- Performed **first-order differencing** → stabilized the mean and removed trend.  
- Re-ran the ADF test → achieved **stationarity** (p-value ≈ 0.0).  

---

## 🔢 Parameter Selection (p, d, q)  
- Differencing order determined: **d = 1**.  
- Based on ACF & PACF plots:  
  - Autoregressive term: **p = 1**  
  - Moving average term: **q = 0**  
- Final ARIMA configuration: **ARIMA(1, 1, 0)**  

---

## 🧠 Model Training  
- Trained **ARIMA(1, 1, 0)** on the stationary series.  
- Verified model convergence and reviewed summary statistics.  
- Coefficients found to be statistically significant.  

---

## 📊 Residual Diagnostics  
- Residual plots showed **no clear patterns**.  
- Verified assumptions of:  
  - **Normality**  
  - **Homoscedasticity**  
  - **Independence**  

---

## 📈 Forecasting  
- Generated **30-day forward forecasts** for closing prices.  
- Visualized forecasted values with **95% confidence intervals**.  
- Predictions aligned with recent historical trends, showing mild variability but overall stability.  

---

## 📝 Conclusion  
The **ARIMA(1, 1, 0)** model effectively captured the dynamics of Apple’s stock closing prices. The results were:  
- **Stable and interpretable forecasts**  
- **Statistically validated assumptions**  
- **Scalable methodology** for other stocks or time series problems  

This project demonstrates the practical use of **statistical modeling in financial forecasting**, offering valuable insights into future stock price movements.  

> 📌 While ARIMA provides a strong baseline, future improvements could include exploring **SARIMA**, **Prophet**, or **LSTM models** for capturing seasonality and nonlinear patterns.

---
