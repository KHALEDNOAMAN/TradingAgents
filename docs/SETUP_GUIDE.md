# TradingAgents - Setup & Strategy Guide

## Quick Setup
```bash
git clone https://github.com/TomoeGozen82/TradingAgents.git
cd TradingAgents
pip install -r requirements.txt
cp .env.example .env  # Add your API keys
python main.py
```

## Architecture
```
Market Data Feed
       |
   Data Pipeline
       |
   +---+---+
   |       |
Technical  Sentiment
Analysis   Analysis
   |       |
   +---+---+
       |
   Trading Agent
       |
   +---+---+
   |       |
  Signal  Risk
  Engine  Manager
   |       |
   +---+---+
       |
   Order Execution
```

## Trading Strategies
| Strategy | Description | Risk Level |
|----------|-------------|------------|
| Momentum | Follow strong price trends | Medium |
| Mean Reversion | Bet on price returning to average | Low-Medium |
| Breakout | Enter on support/resistance breaks | High |
| Sentiment | Trade based on news/social signals | Medium-High |

## Risk Management
- **Position Sizing**: Never risk more than 2% per trade
- **Stop Loss**: Always set stop-loss orders
- **Diversification**: Spread across uncorrelated assets
- **Max Drawdown**: Halt trading at 10% portfolio drawdown

## Backtesting
```bash
python backtest.py --strategy momentum --period 90d --initial 10000
```

## Environment Variables
| Variable | Description |
|----------|-------------|
| `API_KEY` | Exchange API key |
| `API_SECRET` | Exchange API secret |
| `RISK_LIMIT` | Max risk per trade (default: 0.02) |
| `LOG_LEVEL` | Logging verbosity (DEBUG/INFO/WARN) |

## Disclaimer
This is for educational purposes only. Trading involves risk of financial loss. Past performance does not guarantee future results.