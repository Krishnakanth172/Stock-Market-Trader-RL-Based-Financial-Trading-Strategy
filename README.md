This project applies Deep Q-Learning (DQN) to manage a portfolio of stocks, optimizing the allocation of funds across several assets 
to maximize returns. The model uses historical stock prices from Yahoo Finance and trains a reinforcement learning agent to determine 
the best allocation of funds across a portfolio of selected stocks.

Introduction
This project explores the use of Deep Q-Networks (DQN) to solve portfolio allocation problems in a stock market environment. 
The agent learns to balance and manage a portfolio using historical stock price data, aiming to maximize the total value of the portfolio over time.

Libraries Required
Ensure you have the following libraries installed:
numpy
pandas
matplotlib
seaborn
tensorflow
keras
yfinance

To install the required libraries, run the following:
pip install numpy pandas matplotlib seaborn tensorflow keras yfinance

Dataset
The stock data is fetched directly using the yfinance API, which provides historical data for various stock tickers. 
The selected tickers in this project are:
Apple (AAPL)
Google (GOOGL)
Microsoft (MSFT)
Amazon (AMZN)
Tesla (TSLA)
The dataset spans from January 1, 2018 to January 1, 2023.

Environment Setup
The portfolio management environment (PortfolioEnv) simulates stock market trading, taking actions such as distributing a percentage 
of funds across the selected assets and receiving feedback in the form of portfolio gains or losses.

Key elements of the environment include:
Balance: The initial investment amount.
Actions: The portfolio distribution (percentage) across the assets.
Observation: The current stock prices, positions held, and available balance.
Reward: The change in portfolio value at each timestep.

How the RL Agent Works
The agent uses Deep Q-Learning to maximize the return of the portfolio. The DQN agent selects actions (portfolio allocations)
based on the current state of the market and the balance, learning over time from the rewards obtained after each trade.

Key aspects of the agent:
Neural Network Architecture: The agent's policy is approximated using a neural network with fully connected layers.
Epsilon-Greedy Strategy: To balance exploration and exploitation.
Experience Replay: The agent stores and reuses past experiences to improve learning stability.

Training the Agent
During each episode, the agent:
Receives the current market state.
Chooses an action (allocation of funds).
Executes the action, receiving a reward based on the portfolio's performance.
Stores the experience and trains the network using experience replay.
Parameters like the number of episodes, timesteps, and batch size can be adjusted to improve training performance.

Visualization
The model includes a stock price visualization feature to help track historical trends for the selected assets. A graph of stock prices from 2018 to 2023 for the selected tickers is shown to assist in analyzing market behavior.

How to Run
To run this project:
git clone <repository_url>
cd portfolio-management-rl
pip install -r requirements.txt
python train.py

Future Improvements
Additional Assets: Expand the number of tickers and assets considered.
Advanced RL Algorithms: Experiment with other RL algorithms like PPO, DDPG, or A3C for better performance.
Risk Management: Incorporate risk metrics like Sharpe ratio to balance risk vs. reward.
Live Trading: Extend the model to handle real-time trading by integrating with a live broker API.

References
Yahoo Finance API Documentation
Deep Q-Learning in Reinforcement Learning
TensorFlow DQN Implementation
