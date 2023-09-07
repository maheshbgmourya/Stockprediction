# Stockprediction
# Stock Price Prediction
##  Stock Price Prediction using LSTM
This repository demonstrates stock price prediction using LSTM (Long Short-Term Memory) neural networks. We utilize historical stock price data for Apple Inc. (AAPL) obtained from Yahoo Finance and build an LSTM model to predict future stock prices. The model is trained on a portion of the data and tested on unseen data to evaluate its predictive performance.
*Procedure*
*Data Collection:* Historical stock price data for AAPL is acquired from Yahoo Finance through the utilization of the yfinance library. The dataset encompasses daily closing prices spanning from '2012-01-01' to '2023-07-18'.

*Data Preprocessing*: The closing price data undergoes Min-Max normalization, scaling it to the [0, 1] range, which is advantageous for enhancing neural network training. Subsequently, the dataset is partitioned into training and testing subsets. The training subset encompasses 80% of the data, while the testing subset comprises the remaining 20%.

*Model Architecture*: An LSTM neural network is constructed using Keras. This model is comprised of two LSTM layers, each with 50 units, followed by two dense layers with 25 and 1 unit, respectively. The model is configured with the Adam optimizer and employs the mean squared error (MSE) loss function.

*Model Training*: The training process entails fitting the model to the training dataset with a batch size of 1 and running for 10 epochs. The LSTM layers are instrumental in capturing temporal dependencies present in the stock price data.

*Prediction*: Post-training, the model is deployed to forecast future stock prices. To make predictions, the model is fed with the most recent 60 days
