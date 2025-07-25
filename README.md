# Simple Moving Average Backtest on SMH

## Project Summary

This project demonstrates a **complete backtest pipeline** for a classic rule-based trading strategy:  
> **Buy when 20-day moving average crosses above the 50-day moving average. Otherwise, sell or keep cash in money markets.**

The strategy is tested on **SMH ((VanEck Semiconductor ETF))** and compared to a **buy-and-hold baseline** using real financial metrics extracted from _yfinance_:

- Sharpe Ratio  
- CAGR (Compound Annual Growth Rate)  
- Max Drawdown  
- Equity curve visualization

---

## Why This Project Matters

This notebook is built with **quantitative finance interviewers in mind**:
- Full transparency of logic and math behind the strategy
- Readable and modular Python code
- Clean, well-labeled performance evaluation
- Critical evaluation of strategy shortcomings

This notebook showcases my ability to:
- Work with time series and financial data
- Build backtesting frameworks from scratch
- Explain financial metrics clearly
- Think critically about real-world performance

---

## Strategy Intuition

- Moving averages smooth out price data and help identify trend direction.
- A **20/50-day crossover** is a classic "momentum-following" signal.
- The system avoids buying in sideways or bearish conditions.

---

## Tools Used

| Tool | Purpose |
|------|---------|
| `yfinance` | Pull historical SPY data |
| `pandas` | Data manipulation & rolling indicators |
| `numpy` | Math for Sharpe, CAGR, drawdown |
| `matplotlib` | Visualize equity curves |
| `Python` | Pure logic, no black-box tools |

---

## Results Snapshot

| Metric          | Strategy        | Buy & Hold       |
|-----------------|------------------|------------------|
| Sharpe Ratio    | 0.60             | 0.75             |
| CAGR            | 11.29%           | 20.09%           |
| Max Drawdown    | -36.73%          | -49.17%          |

**Interpretation:**
- Strategy reduces drawdown but underperforms in return and Sharpe.
- Shows ability to build **risk-managed systems**, not just return-maximizing ones.

---

## Takeaways

- Fully working backtest logic from scratch
- Quantitative evaluation with industry-relevant metrics
- Interprets risk vs return tradeoffs
- Prepares foundation to incorporate ML-based trading signals (see next project)

---
