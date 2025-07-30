# Volatility-Forecasting-Using-LSTM

# Project Overview:

This project applies Long Short-Term Memory (LSTM) neural networks to forecast financial market volatility. The notebook demonstrates how deep learning can be used to model the time-varying nature of volatility in financial time series data, offering potential applications in risk management, derivatives pricing, and algorithmic trading.

Key features of the project:

- Data preprocessing and log return calculation
- Volatility estimation using feature engineered datas
- LSTM model design and training
- Performance evaluation and visualization
- Comparison of predicted vs. actual volatility

# Model Overview:

| Layer Type        | Units | Return Sequences | Activation | Recurrent Activation | Dropout | Input Shape               |
|-------------------|-------|------------------|------------|-----------------------|---------|----------------------------|
| LSTM (1st Layer)  | 128   | Yes              | tanh       | sigmoid               | —       | (timesteps, features)     |
| Dropout           | —     | —                | —          | —                     | 0.2     | —                          |
| LSTM  (2nd Layer) | 64    | No               | tanh       | sigmoid               | —       | —                          |
| Dropout           | —     | —                | —          | —                     | 0.2     | —                          |
| Dense (Output)    | 1     | —                | linear     | —                     | —       | —                          |

**Compilation:**
- **Loss Function:** Huber loss (δ = 1.0)
- **Optimizer:** Adam (learning rate = 0.001)

# Source:
- Data is taken from yahoo finance
