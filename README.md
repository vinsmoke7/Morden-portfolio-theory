# 📊 Portfolio Optimization using Python & Modern Portfolio Theory

A hands-on implementation of **Modern Portfolio Theory (MPT)** to analyze, simulate, and optimize a stock portfolio using historical financial data. This project uses **Monte Carlo simulation** to generate 10,000 portfolio combinations and finds the optimal one based on the **Sharpe Ratio**.

---

## 🚀 Overview

This project helps answer:
- How to allocate capital among multiple assets to maximize return for a given level of risk?
- What is the best portfolio combination (weights) using real historical stock data?
- How do we visualize the **efficient frontier** and the **optimal portfolio**?

---

## 📌 Key Features

✅ Fetches historical stock prices using `yfinance`  
✅ Calculates daily log returns  
✅ Simulates 10,000 random portfolios  
✅ Calculates expected return, volatility, and Sharpe Ratio  
✅ Optimizes the portfolio to maximize Sharpe Ratio  
✅ Visualizes the efficient frontier and highlights the optimal portfolio

---

## 🛠️ Tech Stack

- **Python 3.8+**
- `NumPy` – numerical operations  
- `Pandas` – data handling  
- `Matplotlib` – data visualization  
- `yfinance` – stock price data  
- `SciPy` – optimization (SLSQP)

---

## 📁 Project Structure


You can easily modify this list in the code to analyze your own selection of stocks.

---

## 🧮 Methodology

### 1. **Data Collection**
Using `yfinance`, we pull historical closing prices (2010–2017) for the selected stocks.

### 2. **Return Calculation**
Daily log returns are computed to normalize values and make data comparable across stocks.

### 3. **Portfolio Simulation**
We simulate 10,000 random portfolios, each with:
- Random asset weights (sum to 1)
- Calculated return, volatility, and Sharpe ratio

### 4. **Optimization**
Using `scipy.optimize.minimize`, we find the optimal portfolio:
- **Objective:** Maximize Sharpe Ratio (minimize its negative)
- **Constraints:** Sum of weights = 1, all weights between 0 and 1

### 5. **Visualization**
Efficient frontier is plotted with:
- Color-coded Sharpe Ratios
- Star-marked optimal portfolio point

---

## 📊 Sample Output

📌 **Optimal Weights:**
```text
AAPL: 0.18, WMT: 0.14, TSLA: 0.24, GE: 0.11, AMZN: 0.23, DB: 0.10
