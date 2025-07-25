# Simple Moving Average Backtest on SMH

## Project Summary 

This project demonstrates a **complete backtest pipeline** for a classic rule-based trading strategy:  
> **Buy when 20-day moving average crosses above the 50-day moving average. Otherwise, exit the position and remain in cash**

The strategy is tested on **SMH (VanEck Semiconductor ETF)** and compared to a **buy-and-hold baseline** using real financial metrics extracted from _yfinance_:

- Sharpe Ratio  
- CAGR (Compound Annual Growth Rate)  
- Maximum Drawdown  
- Equity Curve visualization

---


## Strategy Intuition

- Moving averages smooth out price data and help identify trend direction.
- A **20/50-day crossover** is a standard "momentum-following" signal.
- The system avoids buying in bearish conditions.

---

## Tools 

| Tool | Purpose |
|------|---------|
| `yfinance` | Extract SMH historical data |
| `pandas` | Data manipulation & rolling indicators |
| `numpy` | Math for Sharpe, CAGR, drawdown |
| `matplotlib` | Visualize equity curves |

---

## Results Snapshot

| Metric          | Strategy        | Buy & Hold       |
|-----------------|------------------|------------------|
| Sharpe Ratio    | 0.19             | 0.24             |
| CAGR            | 1.70%            | 2.22%            |
| Max Drawdown    | -69.61%          | -93.10%          |

**Interpretation:**

- Both approaches show very low Sharpe ratios, indicating weak risk-adjusted returns.
- The strategy has slightly lower volatility, but also slightly lower return compared to buy-and-hold.
- Importantly, the strategy significantly reduces max drawdown (69.6% vs 93.1%), suggesting better capital protection in extreme scenarios.
- These results reflect the limits of simple moving average rules on certain assets and underscore the need for improved signal filtering, asset selection, or ML enhancement.

---

**Note:** This strategy is not recommended for real trading. As a college student exploring quant finance, this project was a way to build foundational skills in backtesting, performance evaluation, and model interpretation.

---
