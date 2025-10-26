# USD/IDR Forecast (Binder)

This repo reproduces the *Lakhal (2024)* workflow on another FX pair (USD/IDR) using **open-source tools** in the browser via **Binder**.

## Run in your browser (no installs)
1. Create a **GitHub repo** and upload the files in this folder (or upload the zip I provided).
2. Open this URL in your browser, replacing `YOUR_USER` and `YOUR_REPO`:
   
   `https://mybinder.org/v2/gh/YOUR_USER/YOUR_REPO/HEAD?labpath=usd_idr_forecast.ipynb`

3. Wait for Binder to build, then run the notebook cells top-to-bottom.

## What's inside
- `usd_idr_forecast.ipynb`: End-to-end pipeline
  - Data: Yahoo Finance (`USDIDR=X`), daily -> monthly close
  - Tests: ADF, KPSS
  - Models: ARIMA/ARMA (via statsmodels/pmdarima), LSTM (via TensorFlow CPU)
  - Metrics: MAE, MSE
  - Plots: actual vs predictions

> Tip: If Binder struggles with TensorFlow, you can skip the LSTM section (there's a toggle in the notebook) and still run ARIMA only.
