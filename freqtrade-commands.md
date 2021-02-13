# optimize data
freqtrade hyperopt --hyperopt MyFirstHyperopt --hyperopt-loss SharpeHyperOptLossDaily --strategy MyFirstStrategy --config config.json -e 500 --spaces all

# backtest data
freqtrade backtesting -s MyFirstStrategy -c config.json

## download data
freqtrade download-data -t 5m -c config.json

## trade
freqtrade trade --strategy MyFirstStrategy -c config.json

# trades
"ADA/USD",
"ALGO/USD",
"ATOM/USD",
"BAT/USD",
"BCH/USD",
"DASH/USD",
"EGLD/USD",
"EOS/USD",
"ETH/USD",
"HNT/USD",
"IOTA/USD",
"LINK/USD",
"LTC/USD",
"NEO/USD",
"ONE/USD",
"RVN/USD",
"VTHO/USD",
"XLM/USD",
"XTZ/USD"


# ROI table:
    minimal_roi = {
        "0": 0.20115,
        "19": 0.04606,
        "55": 0.0137,
        "159": 0
    }

# Stoploss:
    stoploss = -0.31937

# Trailing stop:
    trailing_stop = True
    trailing_stop_positive = 0.0143
    trailing_stop_positive_offset = 0.01817
    trailing_only_offset_is_reached = True

# Buy hyperspace params:
    buy_params = {
     'rsi-enabled': False, 'rsi-value': 20, 'trigger': 'bb_lower3'
    }

# Sell hyperspace params:
    sell_params = {
        'sell-rsi-enabled': True,
        'sell-rsi-value': 92,
        'sell-trigger': 'sell-bb_middle'
    }