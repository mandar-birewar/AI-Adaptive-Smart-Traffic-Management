# Member 4 — Traffic Prediction

## Overview
This module predicts short-term traffic vehicle counts from historical observations and classifies predicted traffic levels as LOW, MEDIUM, or HIGH.

## Features
- Weighted moving-average traffic prediction
- Trend-adjusted prediction model
- Traffic-level classification
- CSV-based traffic data input and prediction output
- Model evaluation using MAE, RMSE, and accuracy within five vehicles
- Unit tests for prediction behavior

## Files
- `traffic_predictor.py` — weighted moving-average predictor
- `trend_predictor.py` — trend-adjusted predictor
- `traffic_data.csv` — sample traffic observations
- `traffic_pipeline.py` — generates predictions from the sample data
- `predictions.csv` — generated prediction results
- `evaluate_model.py` — evaluates baseline predictions
- `evaluate_trend.py` — evaluates predictions saved by the pipeline
- `compare_baselines.py` — compares prediction baselines
- `compare_trend.py` — compares the trend model with the last-value baseline
- `test_traffic_predictor.py` — predictor unit tests
- `test_sumo_traffic_adapter.py` — adapter unit tests
- `sumo_traffic_adapter.py` — optional SUMO/TraCI adapter

## How to Run

From the project root:

```bash
python -m unittest discover -s member4_traffic_prediction -p "test_*.py"
python member4_traffic_prediction/traffic_pipeline.py
python member4_traffic_prediction/evaluate_trend.py
```

## Sample Evaluation
On the provided sample dataset, the weighted-average pipeline produced:

- MAE: 7.00 vehicles
- RMSE: 7.53 vehicles
- Predictions within five vehicles: 36.4%

These results use a small synthetic sample and are not a guarantee of real-world performance.

## Limitations
- Evaluation uses a small sample dataset.
- SUMO live integration requires SUMO and TraCI to be installed and configured.
- Live SUMO integration has not been verified in this environment.