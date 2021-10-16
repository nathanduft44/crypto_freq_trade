# Crypto_Freq_Trade
## Overviw
Crypto trading is transforming as Algorithmic Trading is being adopted more by start ups and efficient programmers with specific knowledge in Technical Analyis, Machine Learning, and Smart Contracts. We thought it would be fun to test our knowledge and find profitable trading strategies. The idea around Algorithimc Trading in the Crypto Market is that a user can have automated trades based on conditional logic and can be traded at any time. 
## Data Extraction/Processing
Market data was sourced from Binance.US and sentiment data from LunarCrush API's. Historical data from 2018-2021 was used to train the machine learning models. In addition to pulling data at a set interval ( a 1 minute pull on a 30 min loopback for Lunar Crush Sentiment )using REST API's we experimented with using a websocket for continuous live connection to data which we hope to incoporate into our next steps.
Binance.US
We were able to pull 10 orders per second using the Binance API. The process was making a request using the client.get_historical_klines function with parameters that stated which Currency, time interval, and starting period. We left out the end date because our models needed the latest current data to make profitable decisions.  
## Crypto Arbitrage with Solidity in Testing 
We decided to also look for arbitrage opportunites in the Defi Space within crypto Decentralized Exchanges through the power of Smart Contracts and open source protocols. To gain maximum arbitrage performance and knowledge we built a smart contract that swaps tokens between exchanges in a single transaction. For the testing phase we are using the Ropsten network and deploying the Smart Contract on Ropsten Test Network. The Smart Contract can be deployed via Remix.
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

