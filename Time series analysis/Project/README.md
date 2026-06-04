# Forecasting Financial Instruments' Prices with VECM and ARIMA Models

Time Series Analysis — home-taken project (Spring 2026).

This project compares the **out-of-sample forecasting accuracy** of two competing approaches for a pair of
**cointegrated** financial-instrument prices:

1. a **bivariate Vector Error Correction Model (VECM)**, which models the two series jointly and exploits their
   common long-run (cointegrating) relationship, and
2. two **independent univariate ARIMA models**, one per series, built with the **Box–Jenkins** procedure.

Both sets of forecasts are produced for the same hold-out window and scored with the ex-post forecast error
measures (MAE, MSE/RMSE, MAPE, AMAPE).

## Data

`TSA_2025_2026_PROJECT_DATA_TOPIC_1.csv` — daily prices of ten instruments (`y1`…`y10`), 600 observations.

- **In-sample:** first 575 observations (identification, estimation, diagnostics).
- **Out-of-sample:** last 25 observations (used only to score the forecasts).

## What the notebook does

| Part | Content |
|------|---------|
| A | Checking cointegration with the Engle–Granger procedure (ADF integration order → OLS cointegrating regression → ADF on residuals) |
| B | VECM: Johansen test (trace + max-eigenvalue), estimation, interpretation of β/α/Γ, reparametrization into a VAR, IRF, FEVD, residual diagnostics, forecast and ex-post errors |
| C | Box–Jenkins ARIMA for each series: identification (ACF/PACF), estimation with information criteria (AIC/SBC/HQIC), residual diagnostics (Ljung–Box), forecasting |
| D | Comparing VECM vs ARIMA forecasts on the out-of-sample window |

## Key results

- All ten series are **I(1)**; `y1` and `y4` are identified as a **cointegrated** pair.
- The Johansen test confirms exactly **one cointegrating vector** (rank r = 1).
- Long-run relationship: **`y1 ≈ 2·y4 − 139.4`** (the same vector is recovered by both Engle–Granger OLS and Johansen).
- Adjustment coefficients have the expected opposite signs; adjustment is statistically significant in the `y4`
  equation, so the system corrects mainly through `y4` while `y1` is close to weakly exogenous.
- On the 25-observation hold-out, the **VECM beats both ARIMA models on every error measure** (RMSE, MAPE, AMAPE)
  for both series — the expected payoff from exploiting the cointegrating relationship.

## How to run

```bash
pip install numpy pandas matplotlib statsmodels
jupyter notebook "Project/Forecasting Prices of Financial Instruments with VECM and ARIMA Models.ipynb"
```

Then run all cells top to bottom (the notebook is self-contained and reads the CSV from the `Project` folder).

## Repository structure

```
Project/
├── Forecasting Prices of Financial Instruments with VECM and ARIMA Models.ipynb
└── TSA_2025_2026_PROJECT_DATA_TOPIC_1.csv
```

## Tools

Python · NumPy · pandas · matplotlib · statsmodels (`adfuller`, `coint`, `coint_johansen`, `VECM`, `VAR`, `ARIMA`).
