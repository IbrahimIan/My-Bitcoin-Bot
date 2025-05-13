# My-Bitcoin-Bot
This is a BTC/USD trading bot designed to work with MetaTrader 5. The bot uses technical analysis strategies to identify potential buy and sell opportunities in the BTC/USD market. It can be easily deployed and tested in your MetaTrader 5 environment.
# BTC/USD Trading Bot for MetaTrader 5

## Overview

This is a BTC/USD trading bot designed to work with MetaTrader 5. The bot uses technical analysis strategies to identify potential buy and sell opportunities in the BTC/USD market. It can be easily deployed and tested in your MetaTrader 5 environment.

## Features

- Moving Average Crossover Strategy (default) for generating trading signals
- RSI Strategy as an alternative option
- Real-time price data fetching from MetaTrader 5
- Automatic trade execution
- Performance tracking and analysis
- Trading history and logs
- Customizable trading parameters

## Requirements

- MetaTrader 5 trading platform
- Python 3.7 or higher
- MetaTrader5 Python package
- pandas, numpy for data analysis

## Installation Instructions

### Option 1: Using the Installer

1. Run the installer script:
   ```
   python install_mt5_bot.py
   ```

2. Follow the on-screen instructions to:
   - Install required dependencies
   - Configure the bot
   - Set up the integration with MetaTrader 5

### Option 2: Manual Installation

1. Make sure you have Python 3.7+ installed
2. Install the required dependencies:
   ```
   pip install MetaTrader5 pandas numpy
   ```
3. Copy the `mt5_btc_trader.py` file to your preferred location
4. Configure your MetaTrader 5 path in the script if necessary

## Usage

1. Start MetaTrader 5 and log into your account
2. Ensure BTC/USD (or BTCUSD) pair is available
3. Run the bot script:
   ```
   python mt5_btc_trader.py
   ```
   Alternatively, run it from the Scripts section in MetaTrader 5.

## Configuration Options

You can customize the bot's behavior by modifying the parameters in the main section of `mt5_btc_trader.py`:

- `symbol`: Trading pair symbol (default: "BTCUSD")
- `initial_balance`: Initial portfolio balance for tracking (default: 10000.0)
- `trading_fee`: Trading fee as decimal (default: 0.001 for 0.1%)
- `position_size`: Position size as decimal (default: 0.25 for 25%)
- `update_interval`: Update interval in seconds (default: 60)
- `short_window`: Short moving average window (default: 20)
- `long_window`: Long moving average window (default: 50)

## Strategies

### Moving Average Crossover Strategy (Default)

This strategy generates buy signals when the short-term moving average crosses above the long-term moving average, and sell signals when the short-term moving average crosses below the long-term moving average.

### RSI Strategy

The RSI (Relative Strength Index) strategy generates buy signals when the RSI falls below an oversold threshold, and sell signals when the RSI rises above an overbought threshold.

## Performance Tracking

The bot tracks various performance metrics:

- Total return (absolute and percentage)
- Maximum drawdown
- Sharpe ratio
- Win/loss ratio

Performance data is saved to a JSON file which can be analyzed later.

## Safety and Disclaimer

This bot is provided for educational and research purposes only. Use it at your own risk. Always monitor your trades and be prepared to intervene manually if necessary. Cryptocurrency trading involves significant risk and past performance is not indicative of future results.

## Customization

The bot's modular design allows for easy customization and extension:

- Add new trading strategies by subclassing the TradingStrategy class
- Modify the trade execution logic in the MT5Trader class
- Implement additional performance metrics in the PerformanceTracker class

## Troubleshooting

- Ensure MetaTrader 5 is running before starting the bot
- Check that your MT5 platform has access to BTC/USD price data
- Verify that Python and required packages are properly installed
- Check your internet connection
- Review the terminal output for any error messages

## Support

For issues, feature requests, or questions, please contact the developer or submit an issue through the project's repository.

---

**Copyright © 2025 BTC/USD Trading Bot**
