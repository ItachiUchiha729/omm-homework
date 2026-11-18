# OMM Homework — Arbitrage-Free Implied Volatility

This repository contains the completed and executed Jupyter notebook for the Lecture 3 assignment on Black–Scholes inversion, arbitrage-free smile fitting, and temporal filtering.

The committed notebook runs end-to-end with deterministic synthetic option quotes because the referenced OPRA/Dropbox dataset was not supplied. To use real data, set `DATA_PATH` in the first code cell to a compatible Parquet file.

## Run locally

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook Exercise_Lecture_3_Solutions.ipynb
```

Then select the `.venv` Python kernel and run all cells.
