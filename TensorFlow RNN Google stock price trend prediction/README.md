
# Google Stock Price Prediction

* This project uses a Recurrent Neural Network (RNN) with Long Short-Term Memory (LSTM) layers to predict the Google stock price based on historical stock price data. The model is built using Keras and trained on stock price data from 2012 to 2016, and then tested on stock prices from 2017.

* The goal of this project is to predict future stock prices based on past price data using an LSTM-based RNN. LSTM networks are particularly good at time-series prediction problems because they can learn from sequences of data and capture long-term dependencies.

* The model is trained on Google stock prices from 2012 to 2016, using 60 timesteps to predict the next stock price. The prediction is then tested on Google stock prices from January 2017.

## Dataset

The dataset used in this project consists of two CSV files:
- `Google_Stock_Price_Train.csv`: Training set containing stock prices from 2012 to 2016.
- `Google_Stock_Price_Test.csv`: Test set containing stock prices from January 2017.

## Model Architecture

The model is a Recurrent Neural Network (RNN) with 4 LSTM layers, each followed by dropout regularization to prevent overfitting. The model takes 60 timesteps (60 days of stock prices) as input and outputs a single predicted stock price.

- **Input layer**: Sequence of 60 stock prices (timesteps).
- **Hidden layers**: Four LSTM layers with 50 units each, followed by 20% dropout.
- **Output layer**: Dense layer that predicts the next stock price.

The model is compiled with the Adam optimizer and uses Mean Squared Error (MSE) as the loss function.
