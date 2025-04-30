# Energy Consumption Forecasting for Smart Grids using Deep Learning

This project applies and compares three advanced deep learning models — **LSTM**, **Bidirectional LSTM (BiLSTM)**, and **Transformer** — to forecast annual energy consumption from historical smart grid data.

### Objective:

To improve energy management and grid stability by:
- Accurately forecasting energy consumption
- Supporting demand response planning
- Enhancing renewable integration and reducing costs

### Technologies Used:

- Python (Google Colab)
- TensorFlow / Keras
- Pandas, NumPy, Scikit-learn
- Matplotlib
- MinMaxScaler
- Dataset Source: Kaggle (preprocessed energy data till 2024)

### Model Architectures

#### LSTM Model:
- 2 stacked LSTM layers (64 units)
- Dropout layers (0.2) to prevent overfitting
- Dense output layer

#### BiLSTM Model
- 2 Bidirectional LSTM layers with dropout
- Dense layers for final regression output
- Achieved **best performance** in our comparison

#### Transformer Model
- Custom self-attention encoder with:
  - Multi-head attention
  - Position-wise feed-forward layers
- More scalable, but slightly less accurate in this setup

### Results

| Model       | RMSE    | MAE     |
|-------------|---------|---------|
| LSTM        | 0.0352  | 0.0129  |
| BiLSTM      | 0.0323  | 0.0128  |
| Transformer | 0.0633  | 0.0291  |

>  BiLSTM emerged as the most accurate model for smart grid demand forecasting.
