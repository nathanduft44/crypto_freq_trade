# Crypto_Freq_Trade
The idea behind RNNs is to make use of sequential information. In a traditional neural network we assume that all inputs (and outputs) are independent of each other. But for many tasks that’s a very bad idea. If you want to predict the next word in a sentence you better know which words came before it. RNNs are called recurrent because they perform the same task for every element of a sequence, with the output being depended on the previous computations. Another way to think about RNNs is that they have a “memory” which captures information about what has been calculated so far. In theory RNNs can make use of information in arbitrarily long sequences, but in practice they are limited to looking back only a few steps.


## 
The goal of this project is to create a algorithmic trading strategy based around conditional logic that weighs buy and sell points for a few crypto currencies(TBD). The focus is predicting short trends(High frequency time period) using Recurrent Neural Netoworks and TA. 
## Data
Market data was sourced from Binance.us and sentiment data from LunarCrush API's. Historical data from 2018-2021 was used to train the machine learning models. In addition to pulling data at a set interval ( a 1 minute pull on a 30 min loopback )using REST API's we experimented with using a websocket for continuous live connection to data which we hope to incoporate into our next steps. 
## Machine Learning Models
<details>
<summary>Recurrent Neural Network</summary>
 
<p align="center" width="100%">
    <img width="50%" src="https://user-images.githubusercontent.com/84649228/137434885-43fd209d-0b3d-46ed-974a-56d48bb73d6a.png"> 
</p>    
  
A recurrent neural network (RNN) is a type of artificial neural network that uses sequential data and time series data. RNN models are known for their ability to take the information from prior inputs and use them to influence the current input and output. The data they use creates a dependency on each input and output giving them the ability to understand the data.
 
For this project we utilized the recurrent neural network model to see if we could predict the future price of Bitcoin. First, we gathered the API market data from Binance, pulling data from January 1, 2021, up to the current previous day. Like all other machine learning models, we split our data into 80% training and 20% testing data. The graph below breaks down the market data into training and test data. 
  
<p align="center" width="100%">
    <img width="100%" src="https://user-images.githubusercontent.com/84649228/137440957-ab79f3db-3fcc-4c14-9af8-6aa2d45947f1.png"> 
</p>

After we train, test, and split, we are able to build a model using the idea of long short-term memory(LSTM). LSTM is used as a solution to the vanishing gradient problem that is typical of RNN models. Vanishing gradient occurs when multiplying many small numbers together begins to create even more small numbers to the point of minuscule immaterial data. The more the data trains, the more long term dependencies will influence the data, thus overfitting occurs. LSTM solution to fighting this issue is by having hidden layers of the neural network.
  
There were many trials of testing this model and each model scored very well for mean average error score (all <10%). Based on the training for this data, we were able to get the lowest mean average error score of 2.89%

  <p align="center" width="100%">
    <img width="80%" src="https://user-images.githubusercontent.com/84649228/137442785-c284ca16-a752-4243-bdc9-a76ba55224c1.png"> 
</p>
 
  <p align="center" width="100%">
    <img width="100%" src="https://user-images.githubusercontent.com/84649228/137442739-ed91d252-a128-4dea-90c6-f3de4a49ae1c.png"> 
</p>

We tested more and we believe that the best and most accurate predictive model used was : ___
  


</details>


## DAY 1 implement machine learning LSTM to predict future prices of crypto currencies
First we want to pull Financial data of crypto currencies [BTC, ETH, SOL, ADA]
Prep Data
Build neural network model
Test the model
Make prediction

## Build logic and choose Technical Indicators
