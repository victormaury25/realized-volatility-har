# Realized Volatility Forecasting using HAR Model

## Overview
This project implements a realized volatility (RV) forecasting framework using the Heterogeneous Autoregressive (HAR) model. The objective is to model and forecast short-horizon volatility dynamics using high-frequency price data, with an emphasis on out-of-sample evaluation and realistic backtesting.

The project is intended as a quantitative research exercise and portfolio piece for quantitative finance roles.

---

## Methodology

### Data
- High-frequency (5-minute) cryptocurrency price data obtained from Binance via the `ccxt` API
- Daily realized volatility constructed from intraday log-returns
- Log-transformation applied to stabilize variance and improve model performance

### Model
- HAR model with daily, weekly, and monthly realized volatility components
- Linear regression framework estimated on rolling windows
- Designed to capture volatility persistence across heterogeneous time horizons

### Backtesting
- Walk-forward forecasting approach to avoid look-ahead bias
- Out-of-sample forecasts evaluated using standard regression metrics
- Focus on short-term volatility prediction accuracy

---

## Results
The HAR model demonstrates the ability to capture persistent volatility dynamics and provides reasonable short-horizon forecasts of realized volatility. Results highlight the relevance of multi-scale volatility components and support the use of realized volatility as a benchmark for further risk or derivatives analysis.

---

## Skills Demonstrated
- Financial econometrics and volatility modeling  
- High-frequency data aggregation and preprocessing  
- Time-series regression and walk-forward validation  
- Python: `numpy`, `pandas`, `statsmodels`, `scikit-learn`, `ccxt`

---

## Repository Structure

```text
realized-volatility-har/
├── README.md
├── requirements.txt
├── notebooks/
│   └── RV_forecasting.ipynb
└── data/
    └── README.md
