# time_series_analysis_stock_price_data

# 📈 Time Series Analysis of Stock Prices (Quant-Oriented Project)

## 🚀 Overview

This project performs time series analysis on historical stock price data of Reliance Industries to extract insights relevant to quantitative trading and financial modeling.

The goal is to understand key statistical properties of financial time series such as trend, volatility, autocorrelation, and stationarity.

---

## 📊 Dataset

* Source: Yahoo Finance (via yfinance)
* Asset: RELIANCE.NS (NSE)
* Frequency: Daily
* Features:

  * Open
  * High
  * Low
  * Close
  * Adj Close
  * Volume

---

## ⚙️ Project Workflow

### 1. Data Ingestion & Cleaning

* Loaded CSV using pandas
* Removed inconsistent header rows from raw data
* Converted `Date` column to datetime format
* Set `Date` as index for time series operations

---

### 2. Time Series Visualization

* Plotted closing price over time
* Observed overall trend and fluctuations
* Identified volatility patterns

---

### 3. Resampling (Time Aggregation)

* Converted daily data to monthly averages
* Reduced noise to reveal long-term trends

---

### 4. Autocorrelation Analysis (ACF)

* Measured dependency of current price on past values
* Observed strong autocorrelation in raw price series

---

### 5. Stationarity Testing (ADF Test)

* Applied Augmented Dickey-Fuller test
* Result: Price series is **non-stationary**
* Insight: Financial time series often exhibit trends

---

### 6. Differencing

* Applied first-order differencing
* Removed trend component from the series
* Achieved near-stationary behavior

---

### 7. Moving Average (Smoothing)

* Applied rolling mean (window = 30)
* Smoothed short-term fluctuations
* Highlighted underlying trend

---

### 8. Returns Analysis

* Calculated percentage returns
* Observed near-random behavior
* Reduced autocorrelation compared to raw prices

---

## 📌 Key Insights

* Stock prices are **non-stationary** due to trends
* Raw prices exhibit **high autocorrelation**
* Differencing helps stabilize the series
* Returns behave closer to a **random process**
* Moving averages help identify long-term trends

---

## 🧠 Quant Relevance

This project demonstrates foundational concepts used in:

* Quantitative trading
* Statistical arbitrage
* Time series modeling (ARIMA, etc.)
* Signal generation and feature engineering

---

## 🛠️ Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Statsmodels

---

## 📁 Project Structure

```
.
├── data/
│   └── stock_data.csv
├── stocks.ipynb
└── README.md
```

---

## 📌 Conclusion

This project builds a strong foundation in time series analysis for financial data, covering essential concepts like stationarity, autocorrelation, and transformations.

These techniques are critical for developing quantitative trading strategies and predictive models.

---
