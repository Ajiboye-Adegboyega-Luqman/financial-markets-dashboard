# 📈 Financial Markets Dashboard

Pulling **live market data** with Python and turning it into an interactive **Power BI dashboard** — analysing price, return, risk, and correlation for six major companies (2022–2024).

## 📌 Overview

This project fetches three years of daily stock prices straight from Yahoo Finance via an API, engineers the key financial metrics in Python, and presents them in an interactive Power BI dashboard. It demonstrates the full analyst workflow: **collect live data → engineer metrics → visualise for decision-makers.**

![dashboard.png.png](dashboard.png)

## 🏢 Companies analysed

AAPL, MSFT, GOOGL, AMZN, JPM (a bank, for contrast) and TSLA — a mix of big tech and finance.

## 🔧 Tools & methods

- **Python** — `yfinance` (live data), `pandas` (metrics), `matplotlib` (charts)
- **Power BI** — interactive dashboard with a company slicer, KPI cards, and charts
- **Metrics engineered** — daily returns, annualised volatility, 50-day moving averages, and a correlation matrix

## 📊 What the dashboard shows

- **KPI cards** — number of companies, trading days, and latest date in the data
- **Closing price over time** — price trend for all six companies
- **Price vs 50-day moving average** — trend-smoothing for a selected company
- **Risk by company (volatility)** — annualised volatility, ranked
- **Company slicer** — click any company to filter every visual at once

## 📈 Key findings

1. **Risk varies hugely by company.** TSLA is by far the most volatile (~55%+ annualised), while JPM (the bank) is the steadiest (~23%). Higher potential reward comes with much bigger swings.
2. **Tech stocks move together.** AAPL, MSFT, GOOGL and AMZN show fairly high positive correlation — they tend to rise and fall as a group.
3. **JPM is more independent**, which makes it a useful diversifier: mixing it with tech spreads risk better than holding tech alone.
4. **Moving averages** smooth out daily noise and reveal each stock's underlying trend across the period.

## ✅ How to reproduce

​```bash
# 1. Run the notebook to pull live data and export the CSV
pip install yfinance pandas matplotlib
# open and run 01-markets.ipynb  -> creates data/market_data_for_powerbi.csv

# 2. Open markets_dashboard.pbix in Power BI Desktop
#    (it loads the CSV and renders the dashboard)
​```

## 📂 Files

- `01-markets.ipynb` — Python: pulls live data and engineers the metrics
- `markets_dashboard.pbix` — the interactive Power BI dashboard
- `dashboard.png` — screenshot of the dashboard
- `data/market_data_for_powerbi.csv` — the prepared dataset

## 🔮 What I'd do next

- Add a portfolio view (combine the stocks and show blended return vs risk).
- Include a Sharpe-ratio measure to compare risk-adjusted performance.
- Schedule the notebook to refresh the data automatically.

---
*Part of my data analytics portfolio — [github.com/Ajiboye-Adegboyega-Luqman](https://github.com/Ajiboye-Adegboyega-Luqman)*
