<h1 align="center">Crypto_Freq_Trade</h1>

## Overview
Crypto trading is transforming as Algorithmic Trading is being adopted more by start ups and efficient programmers with specific knowledge in Technical Analyis, Machine Learning, and Smart Contracts. We thought it would be fun to test our knowledge and find profitable trading strategies. The idea around Algorithimc Trading in the Crypto Market is that a user can have automated trades based on conditional logic and can be traded at any time. 

## Data Extraction/Processing
Market data was sourced from Binance.US and sentiment data from LunarCrush API's. Historical data from 2018-2021 was used to train the machine learning models. In addition to pulling data at a set interval using REST API's we experimented with using a websocket for continuous live connection to data which we hope to incorporate into our next steps.
We pulled 10 orders per second using the Binance API. We made requests using the client.get_historical_klines function passing the parameters of currency, time interval, and starting period. The end date was ommitted because our models need the latest and most current data to make profitable decisions. 

## Crypto Arbitrage with Solidity in Testing 
We decided to also look for arbitrage opportunites in the Defi Space within crypto Decentralized Exchanges through the power of Smart Contracts and open source protocols. To gain maximum arbitrage performance and knowledge we built a smart contract that swaps tokens between exchanges in a single transaction. For the testing phase we are using the Ropsten network and deploying the Smart Contract on Ropsten Test Network. The Smart Contract can be deployed via Remix.

## Machine Learning Models
<details>
<summary>Recurrent Neural Network</summary>
 
<p align="center" width="100%">
    <img width="50%" src="https://user-images.githubusercontent.com/84649228/137434885-43fd209d-0b3d-46ed-974a-56d48bb73d6a.png"> 
</p>    
  
A recurrent neural network (RNN) is a type of artificial neural network that uses sequential data and time series data. RNN models are known for their ability to take the information from prior inputs and use them to influence the current input and output. The data they use creates a dependency on each input and output giving them the ability to understand the data and make educated predictions.
 
For this project we utilized the recurrent neural network model to see if we could predict the future price of Bitcoin. First, we gathered the API market data from Binance, pulling data from January 1, 2021, up to the current previous day. Like all other machine learning models, we split our data into 80% training and 20% testing data. The graph below breaks down the market data into training and test data. 
  
<p align="center" width="100%">
    <img width="100%" src="https://user-images.githubusercontent.com/84649228/137440957-ab79f3db-3fcc-4c14-9af8-6aa2d45947f1.png"> 
</p>

After we train, test, and split, we are able to build a RNN model using the idea of long short-term memory(LSTM). LSTM is used as a solution to the vanishing gradient problem that is typical of RNN models. Vanishing gradient occurs when multiplying many small numbers together begins to create even more small numbers to the point of minuscule immaterial data, thus leaving the model incapable of predicting. LSTM is solution to fighting this issue is by having hidden layers of the neural network that counter act these issues by using forget, store, update, and controlling the output.

 **RESULTS** 
 
There were many trials of testing this model, and each model scored very well with mean average error score all under 10%. Based on the training for this data, we were able to get the lowest mean average error score of 2.89% and our model closely predicts the actual.

  <p align="center" width="100%">
    <img width="50%" src="https://user-images.githubusercontent.com/84649228/137442785-c284ca16-a752-4243-bdc9-a76ba55224c1.png"> 
</p>
 
  <p align="center" width="100%">
    <img width="100%" src="https://user-images.githubusercontent.com/84649228/137442739-ed91d252-a128-4dea-90c6-f3de4a49ae1c.png"> 
</p>

 
</details>

<details>
<summary>Logistic Regression and Support Vector Machine</summary>
Logistic Regression Model 
Logistic Regression is a parametric classification type of model that is used for predicting binary outcomes with a categorical target.
In our instance we applied technical analysis and created a trading signal as the outcome to predict profitable trades. We used a Short Moving Average strategy, improved the strategy by adjusting the Technical moving average rolling average to the optimal lengths. 
Our Model was able to out perform the actual returns. This was a milestone!!
Logistic Regression Results:
 
Classification Report
 ![Screen Shot 2021-10-15 at 9 01 45 PM](https://user-images.githubusercontent.com/86027898/137573107-5f85a2c0-56cd-43a3-90f5-f1700e3b5d7c.png)
 
Model prediction vs Actual Returns
 ![Screen Shot 2021-10-15 at 9 02 56 PM](https://user-images.githubusercontent.com/86027898/137573146-c5d7d620-71dc-496a-a2bc-a85f1fdaf623.png)
 
Suppor Vector Machine Results:
This is another supervised machine learning model that can produce significant accuracy.

Classification Report
 ![Screen Shot 2021-10-15 at 9 00 22 PM](https://user-images.githubusercontent.com/86027898/137573079-74bd2314-cb1a-42d4-b403-d4b258092b1a.png)

Model prediction vs Actual Returns
 ![Screen Shot 2021-10-15 at 8 57 14 PM](https://user-images.githubusercontent.com/86027898/137572970-a0a0c904-2dbf-4fae-acab-57847b51eba1.png)

 </details>
 
 ## Contributors
 
 [Nathan Duft](https://www.linkedin.com/in/nathan-duft-b746691a6/)
 
 [Ksenia Gorska](https://www.linkedin.com/in/ksenia-gorska/)
 
 [Julia Guanzon](https://www.linkedin.com/in/julia-guanzon/)
 
 [Nansamba Ssensalo](https://www.linkedin.com/in/a-nansamba-ssensalo/)
 
 ## Installation and Libraries
 Python   
 Pandas    
 Sklearn  
 Keras  
 Solidity  
 sqlalchemy  
 python-binance  
 matplotlib  
 import mplfinance as mpl  
 * To run arbitrage download remote open source protocols seen in the Crypto Arbitrage Folder and solidity compiler
 * To run the machine learning models import Sklearn and Keras, view models page for details
 * To pull data from binance api and make requests do pip install python-binance
