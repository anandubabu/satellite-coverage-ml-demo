# satellite-coverage-ml-demo
Quick ML demo predicting satellite constellation coverage from orbital parameters

# Satellite Coverage ML Demo

Quick ML model to predict satellite constellation coverage - replaces slow physics simulations with fast predictions.

## Run It
```bash
pip install numpy matplotlib scikit-learn
python satellite_coverage_ml_demo.py
```

Or open the Jupyter notebook and run all cells.

Generates 100 training samples, trains a model, tests on 10 samples, creates plots.

## Why Random Forest?

I went with Random Forest because it just works - handles the non-linear stuff between altitude/inclination/coverage without needing feature scaling or tons of tuning. Plus you get feature importance built-in. For a quick demo with limited data, tree ensembles are solid and won't randomly fail as i know.

## What I'd Change for Real Data

Actual constellation sims give you time-series coverage, pass predictions, ground station visibility - way richer data. I'd probably use XGBoost or LightGBM to catch temporal patterns and satellite interactions that Random Forest misses. 


