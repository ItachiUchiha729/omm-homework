# OMM Homework — Arbitrage-Free Implied Volatility

This repository contains the completed and executed Lecture 3 assignment on Black–Scholes inversion, arbitrage-free smile fitting, out-of-sample validation, and constrained Kalman temporal smoothing.

The analysis uses the included full-day `NVDA_20241014.parquet` data, selects the short-dated 2024-11-15 expiry, and fits all 390 one-minute snapshots. Per-minute forwards are inferred robustly from call–put parity. The curve uses OTM puts converted to call-equivalent prices below the forward and OTM calls above it.

## Run results

- 390/390 one-minute fits accepted by the constrained optimizer
- Dense-grid static-arbitrage constraint minimum: `4.168e-05`
- 52,072 one-minute-ahead quote comparisons
- Outside bid/offer: `55.3176%`
- Price RMSE: `0.023416`; price bias: `-0.000334`
- 389/389 constrained Kalman projections successful
- Slack-constraint Kalman identity check: exact to reported numerical precision

The executed notebook contains the smile, ATM time-series, and ACF figures plus the full derivation, validation, assumptions, and limitations. The original instructions are included as `Exercise Lecture 3.pdf`.

## Run locally

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook Exercise_Lecture_3_Solutions.ipynb
```

Then select the `.venv` Python kernel and run all cells.
