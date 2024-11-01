This is a project application of Deep Q-Learning (DQN) that manages a portfolio of stocks in the most optimal way for the funds to be spread across
different assets to increase returns. The model employs historical stock prices from Yahoo Finance, training a reinforcement learning agent to determine
the best way to allocate funds across a portfolio of selected stocks.

Introduction
This project is meant to solve portfolio allocation problems in a stock market environment using Deep Q-Networks.
The agent learns how to balance and manage a portfolio based on historical stock price data with the objective of maximizing the total value of the portfolio over time.

Libraries Required
Make sure you have the following libraries installed:
numpy
pandas
matplotlib
seaborn
tensorflow
keras
yfinance

Install the required libraries using pip as follows:
pip install numpy pandas matplotlib seaborn tensorflow keras yfinance

Dataset
The yfinance API brings stock data raw fashion and has the history value based on a couple of stock tickers. For the given project, I have used the set consisting of
App (AAPL)
Google (GOOGL)
Microsoft (MSFT)
Amazon (AMZN)
Tesla (TSLA)
Dates Taken
Jan 1, 2018- to Jan 1, 2023
End
The equilibrium of money across the selected resources and getting feedback through gains or losses in the portfolios.
Major components of the environment:
Balance: initial sum put in
Actions: percentage distribution of portfolio, at each time step over assets
Observation: present prices of stocks, the current states, and remaining balance.
Reward: increase in the value of portfolios, at every step.

Working of the RL Agent
The agent is making use of the Deep Q-Learning so that it maximizes the return on the portfolio. In this, the action or the choice of actions for portfolio allocations by a DQN agent takes place with the influence of the given state of the market and also the balance is learned at each trade that it performed after gaining the rewards accordingly.

Agent Aspects:
It possesses the structure of its policy in a type of feedforward neural network having connected layers.
This strategy can be defined under Epsilon-Greedy: An exploration-exploitation algorithm that helps a trade in balancing both actions.
Experience Replay: The agent stores and reuses past experiences to improve learning stability.

Training the Agent
At every episode, the agent:
Takes the current market state.
Chooses an action (allocation of funds).
Executes the action and receives a reward based on the portfolio's performance.
Stores the experience and trains the network using experience replay.
Hyperparameters like number of episodes, timesteps, and batch size can be tuned to improve training performance.

Visualization
The model comes with the functionality of showing stock price over time in order to trace the history of chosen assets. A graph of the stock prices from 2018 to 2023 for the selected tickers is shown in order to help analyze the market behavior.

How to Run
Run this project
git clone <repository_url>
cd portfolio-management-rl
pip install -r requirements.txt
python train.py

Future Improvements
More Assets: Increase the number of tickers and assets considered.
Advanced RL Algorithms: Try other RL algorithms such as PPO, DDPG, or A3C to see if you can improve performance.
Risk Management: Introduce risk metrics like the Sharpe ratio to balance risk vs. reward.
Live Trading: Extend the model to handle live trading by integrating with a live broker API.

References
Yahoo Finance API Documentation
Deep Q-Learning in Reinforcement Learning
TensorFlow DQN Implementation
