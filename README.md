# 📋 QuantZ Week 4 Game Documentation

**Developed by Shashank Raj and used by QuantZ**

## Table of Contents
1. [Introduction](#1-introduction)
2. [Games Overview](#2-games-overview)
   - [Portfolio Pursuit](#21-portfolio-pursuit)
   - [Algorithmic Arena](#22-algorithmic-arena)
3. [Game Setup](#3-game-setup)
   - [Installation](#31-installation)
   - [Running the Games](#32-running-the-games)
4. [Portfolio Pursuit Game Mechanics](#4-portfolio-pursuit-game-mechanics)
   - [Game Objective](#41-game-objective)
   - [Game Rules](#42-game-rules)
   - [Game Parameters](#43-game-parameters)
   - [Scoring System](#44-scoring-system)
   - [Player Interactions](#45-player-interactions)
   - [Key Strategies](#46-key-strategies)
5. [Algorithmic Arena Game Mechanics](#5-algorithmic-arena-game-mechanics)
   - [Game Objective](#51-game-objective)
   - [Game Rules](#52-game-rules)
   - [Game Parameters](#53-game-parameters)
   - [Scoring System](#54-scoring-system)
   - [Strategy Development](#55-strategy-development)
6. [Visualizations](#6-visualizations)
7. [Best Practices](#7-best-practices)
8. [Conclusion](#8-conclusion)

---

## 1. Introduction

This documentation provides a detailed overview of the interactive games developed by **Shashank Raj** and used by **QuantZ** to enhance students’ understanding of quantitative finance concepts. The games offer a unique learning experience that integrates real-world investment and trading strategies with simulated environments.

The Week 4 games are designed to enable players to engage with advanced financial metrics, understand the dynamics of market conditions, and test out trading algorithms in a risk-free setting. The games covered in this documentation are:

1. **Portfolio Pursuit** 💼 - A portfolio management game that focuses on effective capital allocation and risk management.
2. **Algorithmic Arena** 🤖 - A strategy-building game that allows players to design and implement trading algorithms.

These games serve as powerful tools to facilitate experiential learning, enabling students to grasp complex financial theories through interactive simulations.

## 2. Games Overview

### 2.1. Portfolio Pursuit 💼

**Portfolio Pursuit** is a comprehensive investment management simulation where players allocate their virtual capital across various asset classes over multiple rounds, each with its unique market conditions. The game aims to teach players how to balance risk and return effectively, adapt to changing market dynamics, and employ strategic decision-making to achieve the highest returns.

#### Key Features:
- **Dynamic Market Conditions:** Each round introduces a new market condition, such as Bull Market, Bear Market, Sector Boom, etc., impacting the performance of assets.
- **Multiple Asset Classes:** Players can invest in Stocks, Bonds, Commodities, and ETFs, each with different expected returns and volatilities.
- **Score-Based System:** Players earn points based on portfolio returns, Sharpe ratio, and risk management. Penalties are incurred for negative returns and high Value at Risk (VaR).

### 2.2. Algorithmic Arena 🤖

**Algorithmic Arena** challenges players to design, develop, and test trading algorithms over multiple rounds under varying market conditions. The game enables players to explore how different strategies perform in bull, bear, sideways, and volatile markets.

#### Key Features:
- **Strategy Customization:** Choose from strategies like Moving Average Crossover, Mean Reversion, RSI, and Bollinger Bands.
- **Parameter Tuning:** Adjust critical parameters like window periods, RSI thresholds, and volatility levels to optimize strategy performance.
- **Performance Metrics:** Players receive feedback on strategy returns, capital growth, and strategy robustness.

## 3. Game Setup

### 3.1. Installation

To run the games in a Jupyter Notebook environment, ensure that the following packages are installed:

```bash
pip install -q ipywidgets
jupyter nbextension enable --py widgetsnbextension --sys-prefix --quiet
```

### 3.2. Running the Games

After installing the required packages, simply run the cells containing the game code in your Jupyter Notebook. Each game will display an introductory interface with a "Start Game" button. Click on it to initiate gameplay.

## 4. Portfolio Pursuit Game Mechanics

### 4.1. Game Objective

The objective of **Portfolio Pursuit** is to allocate capital effectively among a variety of assets over a series of 10 rounds. Players aim to maximize returns while managing risk, responding to dynamically changing market conditions each round.

### 4.2. Game Rules

1. **Starting Capital:** Each player starts with an initial capital of $10,000.
2. **Asset Allocation:** Allocate capital among assets like Stock A, Stock B, Bond A, Commodities, and ETFs. Ensure the total allocation does not exceed your current capital.
3. **Market Conditions:** Market conditions vary each round, including scenarios like Bull Market, Bear Market, Stable Market, and Sector Booms. Each condition affects asset performance differently.
4. **Scoring and Penalties:** Earn points for positive returns and good Sharpe ratio. Penalties are applied for negative returns and high Value at Risk (VaR).

### 4.3. Game Parameters

| Parameter      | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `mean_return`  | Average return of the asset over time, updated dynamically each round.      |
| `volatility`   | Standard deviation of returns, indicating the asset's risk level.           |
| `NUM_ROUNDS`   | Total number of rounds in the game (set to 10).                             |
| `market_event` | Randomly selected event that impacts returns and volatility each round.     |

### 4.4. Scoring System

| Performance Metric         | Points/ Penalties                               |
|----------------------------|-------------------------------------------------|
| Portfolio Return > $500    | +10 points                                       |
| Portfolio Return > $200    | +7 points                                        |
| Portfolio Return > $0      | +5 points                                        |
| Negative Return            | +5 penalties                                     |
| Sharpe Ratio > 0.5         | +5 points                                        |
| Sharpe Ratio > 0.2         | +3 points                                        |
| High VaR (Value at Risk)   | +5 penalties for VaR < -500, +3 for VaR < -200   |

### 4.5. Player Interactions

- **Start Game:** Initializes the game and displays the portfolio allocation interface.
- **Proceed to Next Round:** Validates the player's allocation, calculates returns based on market conditions, and updates the game state for the next round.
- **End Game:** Ends the game after 10 rounds, displays the final score, and provides an evaluation of the player's performance.

### 4.6. Key Strategies

- **Diversification:** Spread your capital across multiple assets to reduce risk.
- **Market Condition Analysis:** Adapt your allocations based on current and expected market conditions.
- **Risk Management:** Consider each asset's volatility and the market condition impact before making allocations.

## 5. Algorithmic Arena Game Mechanics

### 5.1. Game Objective

The objective of **Algorithmic Arena** is to design trading algorithms and test them under varying market conditions. Players must choose the appropriate strategy and fine-tune parameters to achieve optimal performance over 10 rounds.

### 5.2. Game Rules

1. **Initial Capital:** Each player starts with $10,000.
2. **Strategy Selection:** Choose a trading strategy each round, such as Moving Average Crossover or RSI Strategy.
3. **Parameter Adjustment:** Modify parameters like moving averages, RSI periods, and volatility thresholds.
4. **Market Conditions:** The market changes each round, impacting your strategy performance.
5. **Scoring and Penalties:** Earn points based on strategy returns. Penalties are applied for significant losses or underperformance.

### 5.3. Game Parameters

| Parameter       | Description                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| `strategy_name` | Name of the selected trading strategy.                                      |
| `market_event`  | Market condition affecting strategy performance (Bull Market, Bear Market). |
| `capital`       | Player's available capital at the start of each round.                      |

### 5.4. Scoring System

| Performance Metric            | Points/ Penalties                                   |
|-------------------------------|-----------------------------------------------------|
| Profit per Round > $0         | +1 point per $100 profit                             |
| Strategy Return > 0.07        | +5 points (bonus for high returns)                   |
| Strategy Return < -0.05       | +5 penalties (for large losses)                      |

### 5.5. Strategy Development

- **Parameter Optimization:** Tune parameters like lookback periods, thresholds, and RSI levels for better performance.
- **Market Condition Analysis:** Adapt strategy parameters based on the market environment (e.g., higher lookback period for bull markets).
- **Performance Evaluation:** Review strategy performance each round and refine parameters accordingly.

## 6. Visualizations

Both games include interactive visualizations to help players track their performance:

- **Portfolio Value Over Time:** A line chart displaying the player's capital across the rounds.
- **Asset Mean Returns and Volatilities Over Time:** Plots the mean returns and volatilities for each asset class over the 10 rounds.

## 7. Best Practices

To maximize performance in both games, consider the following best practices:

- **Analyze Market Conditions:** Each round presents a unique set of market conditions that impact asset and strategy performance. Adapt your decisions accordingly.


- **Monitor Portfolio Metrics:** Pay attention to key metrics like Sharpe Ratio, Value at Risk (VaR), and Portfolio Standard Deviation.
- **Refine Strategies Regularly:** Adjust strategy parameters and asset allocations to respond to market fluctuations.
- **Balance Risk and Return:** Strive for a balance between high returns and low risk by diversifying your portfolio or selecting stable strategies.

## 8. Conclusion

The Week 4 games—**Portfolio Pursuit** and **Algorithmic Arena**—are designed to deepen players' understanding of investment management and trading strategies. Through dynamic market simulations and interactive strategy testing, players can hone their decision-making skills and develop a nuanced understanding of risk and return in quantitative finance. Enjoy the games and may your virtual portfolios and algorithms outperform the markets!

