# Simple Moving Average Backtest on SMH

## Project Summary 

This project demonstrates a **complete backtest pipeline** for a classic rule-based trading strategy:  
> **Buy when 20-day moving average crosses above the 50-day moving average. Otherwise, sell or keep cash in money markets.**

The strategy is tested on **SMH (VanEck Semiconductor ETF)** and compared to a **buy-and-hold baseline** using real financial metrics extracted from _yfinance_:

- Sharpe Ratio  
- CAGR (Compound Annual Growth Rate)  
- Maximum Drawdown  
- Equity Curve visualization

---


## Strategy Intuition

- Moving averages smooth out price data and help identify trend direction.
- A **20/50-day crossover** is a standard "momentum-following" signal.
- The system avoids buying in sideways or bearish conditions.

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
- Strategy reduces drawdown but underperforms in return and Sharpe.
- Shows ability to build **risk-managed systems**, not just return-maximizing ones.

---
