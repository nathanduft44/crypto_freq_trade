# Crypto_Freq_Trade
The idea behind RNNs is to make use of sequential information. In a traditional neural network we assume that all inputs (and outputs) are independent of each other. But for many tasks that’s a very bad idea. If you want to predict the next word in a sentence you better know which words came before it. RNNs are called recurrent because they perform the same task for every element of a sequence, with the output being depended on the previous computations. Another way to think about RNNs is that they have a “memory” which captures information about what has been calculated so far. In theory RNNs can make use of information in arbitrarily long sequences, but in practice they are limited to looking back only a few steps.


## 
The goal of this project is to create a algorithmic trading strategy based around conditional logic that weighs buy and sell points for a few crypto currencies(TBD). The focus is predicting short trends(High frequency time period) using Recurrent Neural Netoworks and TA. 
## Data
Pull minute data from a 30 min lookback period and run TA on that.
Still unknown for the Machine learning models.
## Backtest the algorithm and optimize RNN.



## DAY 1 implement machine learning LSTM to predict future prices of crypto currencies
First we want to pull Financial data of crypto currencies [BTC, ETH, SOL, ADA]
Prep Data
Build neural network model
Test the model
Make prediction

## Build logic and choose Technical Indicators
