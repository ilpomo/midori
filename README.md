![`open-trading` header image.](docs/header.jpg)

![Repo size](https://img.shields.io/github/repo-size/ilpomo/open-trading?color=70e000)
![License](https://img.shields.io/github/license/ilpomo/open-trading?color=70e000)

# open-trading: a simple trading system

`open-trading` is a trading system that allows you to connect to your favourite exchanges to download both historical 
intraday and real-time data; it lets you also create custom trading strategies, backtest them and run them live. It 
tries to do it in the most simple, essential and effective way.

## Features

### Integrated Data Acquisition Pipeline

Connect to your favourite exchanges and download both **historical intraday** (trades, OHLCV 1m+) and **real-time** 
(orderbook, L1-L2) data.

### Trading Strategy Builder

Build your custom trading strategies starting from one of the available templates and combine your favourite technical 
indicators to generate your trading signals.

### Interactive Dashboard

Visualize your trading strategies while you are building them, tweak indicators parameters and see how they adapt in 
price chart. This will allow you to easily filter all those indicators parameters that when combined would never 
generate any trading signal, reducing by a lot the backtest to run.

### Backtesting Suite

Proper backtesting is hard, but `yolo_mode=True`. Define a gazillion parameter combinations, massively backtest them all 
by parallelizing the computation<sub>and cooking your hardware, lol</sub>, visualize the performance 
<sub>normal</sub>distribution and choose the one you prefer<sub>it's the most frequent one, right? Right?!</sub>.

### Paper Trading

You, pussy.

### Live Trading

Deploy them live without needing to configure any third-party service, directly from your notebook, workstation, private 
server or cloud solution. The entire platform is extremely efficient and scalable, probably you will not need expensive 
hardware for even the most complex strategies.

### Private Telegram Bot

Set up a private Telegram bot that acts as a notification system for the platform's trading activity and as a remote 
control interface:
- Activate or deactivate any trading strategy.
- Activate or deactivate notifications for API updates.
- Tweak strategies parameters on-the-fly, while live trading without rebooting<sub>Microsoft can't, just 
  saying</sub>.

## Design

- Designed over [the actor model](https://en.wikipedia.org/wiki/Actor_model) through [open-core lib](https://github.com/ilpomo/open-core)
  - Parallelism through multi-processing for CPU bound tasks
  - Concurrency based on multi-threading for I/O bound tasks
  - Concurrency based on Asyncio for network-related tasks
  - [ZeroMQ](https://github.com/zeromq/pyzmq) asynchronous PUB/SUB IPC/INPROC sockets
- Custom database-like class based on [Polars](https://github.com/pola-rs/polars/)
  - Flat files in Apache Parquet format
  - No need to learn SQL
  - Query data using built-in methods
- Single user
- Multi-exchange
- Multi-asset
- Multi-strategy
- More...

## Installation

```sh
pip install open-trading
```

## Dependencies

`open-trading` will always try to reduce dependencies to the extreme minimum. The current dependencies are specified in 
the `requirements.txt` file::

- **Polars**: Blazingly fast DataFrames in Rust, Python, Node.js, R, and SQL
- **PyZMQ**: Python bindings for ZeroMQ, a high-performance asynchronous messaging library.
- **python-telegram-bot**: a library to build Telegram bots.

Ensure you have the latest versions of these dependencies installed.

## Acknowledgments

To my family, for always supporting me.  
To my girlfriend, for also putting up with me.  
To my friends, for lightening my load during the heaviest moments.  
To the open-source community, for teaching me without asking for anything in return.  
E a Patato, che mi manca in ogni istante.
