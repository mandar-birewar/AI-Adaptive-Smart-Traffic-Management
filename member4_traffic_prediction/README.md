
# Member 4 — Traffic Prediction

## Objective
Estimate near-future traffic counts from recent vehicle-count observations.

## Features
- CSV-based traffic data input
- Weighted moving-average baseline prediction
- Low, medium, and high traffic classification
- Prediction output saved as CSV
- MAE, RMSE, and tolerance-based evaluation
- Unit tests

## Files
- `traffic_predictor.py`: prediction logic
- `traffic_pipeline.py`: CSV processing and prediction output
- `evaluate_model.py`: evaluation metrics
- `test_traffic_predictor.py`: unit tests
- `traffic_data.csv`: sample input data
- `predictions.csv`: generated output

## Run
From the project root:

```bash
python member4_traffic_prediction/traffic_pipeline.py
python member4_traffic_prediction/evaluate_model.py
python -m unittest discover -s member4_traffic_prediction -p "test_*.py"
```

## Limitations
The sample dataset is synthetic. This is a baseline model, not a trained
machine-learning model. Real traffic data and validation are required before
using predictions for signal-control decisions.
