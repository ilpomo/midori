![Header image of the midori's project repository. Photo by <a href="https://unsplash.com/it/@resourcedatabase?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Resource Database</a> su <a href="https://unsplash.com/it/foto/un-primo-piano-di-un-oggetto-bianco-e-nero-k_jj6N5fU-8?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Unsplash</a>
  ](docs/header.png)

# midori: a simple trading system

> <div style="text-align: justify; font-style: italic;">Programming is science dressed up as art because most of us 
> don’t understand the physics of software and it’s rarely, if ever, taught. The physics of software is not algorithms, 
> data structures, languages and abstractions. These are just tools we make, use, throw away. The real physics of 
> software is the physics of people–specifically, our limitations when it comes to complexity, and our desire to work 
> together to solve large problems in pieces. This is the science of programming: make building blocks that people can 
> understand and use easily, and people will work together to solve the very largest problems.</div>
> 
> <div style="text-align: right; font-weight: bold">Pieter Hintjens</div>

Midori is a trading system that allows you to connect to your favourite exchanges to download both historical intraday 
and real-time data; it lets you create custom trading strategies, backtest them and run them live. It tries to do it in 
the most simple, essential and effective way.

## Features

- Connect to your favourite exchanges and download both historical intraday and real-time data.
- Build your trading strategies starting from a vanilla one and combining built-in trading indicators.
- Model your trading strategies though an interactive web dashboard, tweak their configuration parameters and iterate.
- Backtest your trading strategies and choose the best parameters given your risk profile.
- Paper-test your trading strategies before running them live.
- Run your trading strategies live from your notebook, workstation, private server or cloud solution.
- Remotely control your trading system through a private Telegram Bot and receive real-time notifications.

## Design

- Designed over [the actor model](https://en.wikipedia.org/wiki/Actor_model)
  - Multiprocessing
  - ZeroMQ asynchronous PUB/SUB IPC sockets
- Flat files based on Polars instead of database
  - No need to learn SQL
  - Query data using the built-in client's class methods
- Single user
- Multi-exchange
- Multi-asset
- Multi-strategy
- Rage against dependencies
- More...

## Acknowledgments

To my family, for always supporting me.  
To my girlfriend, for also putting up with me.  
To my friends, for lightening my load during the heaviest moments.  
To the open-source community, for teaching me without asking for anything in return.  
E a Patato, che mi manca in ogni istante.
