# Stock Price Prediction using LSTM (PyTorch)

This project demonstrates how to build a Long Short-Term Memory (LSTM) model using PyTorch to predict stock prices based on historical closing prices from Yahoo Finance.

## Overview
The script:
1. Downloads historical stock price data (default: Microsoft `MSFT`) using Yahoo Finance.
2. Scales and sequences the data for time-series prediction.
3. Builds and trains an LSTM model in PyTorch.
4. Evaluates performance using RMSE (Root Mean Squared Error).
5. Visualizes actual vs predicted prices and prediction errors.

## Requirements
Make sure you have Python 3.8+ and install the required libraries:
```bash
pip install numpy pandas matplotlib yfinance torch scikit-learn
```

## Usage
Run the script directly:
```bash
python stock_lstm.py
```

By default, it predicts Microsoft (`MSFT`) stock prices starting from `2020-01-01`. You can modify the `ticker` variable to change the stock.

## Key Parameters
- **`ticker`**: Stock ticker symbol (default: `MSFT`).
- **`seq_length`**: Number of previous days used for prediction (default: 30).
- **`hidden_dim`**: Hidden layer size in LSTM (default: 32).
- **`num_epochs`**: Training epochs (default: 200).
- **`learning_rate`**: Learning rate for optimizer (default: 0.01).

## Model Architecture
- **LSTM** with 2 layers and hidden size of 32.
- Fully connected layer to output a single price prediction.

## Output
- Predicted vs Actual stock price plot.
- Prediction error plot.
- RMSE score for both training and testing sets.

## Example Visualization
The output includes:
- **Blue line**: Actual stock prices
- **Green line**: Predicted prices
- **Red line**: Prediction error over time

## License
This project is for educational purposes only and should not be used for real investment decisions.
