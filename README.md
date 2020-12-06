# 📈 Fullstack Trading App (Backtesting Engine)

A full-stack Python-based trading system for strategy development, backtesting, and market data analysis using the Alpaca API and historical minute-level stock data.

---

## 🚀 Overview

This project implements a **quant trading backtesting engine** focused on the *Opening Range Breakout (ORB)* strategy. It simulates trades on historical stock data stored in a SQLite database and evaluates performance across multiple tickers.

Key features:
- Backtesting engine built with **Backtrader**
- Historical market data stored in **SQLite**
- Strategy-based trading simulation
- Multi-stock batch testing
- Opening Range Breakout strategy implementation
- Performance evaluation per stock

---

## 🧠 Strategy: Opening Range Breakout (ORB)

The strategy defines an **opening range** during the first minutes of market open and trades based on breakouts above or below this range.

### Core logic:
- Calculate high/low during opening range period
- Enter long when price breaks above range
- Exit on reversal or profit/loss thresholds
- Liquidate positions near market close

---

## 🏗️ Tech Stack

- Python
- Backtrader
- Pandas
- SQLite
- Alpaca API (data integration)
- NumPy (implicit dependency)

---

## 📊 Data Structure

The application expects a SQLite table:

`stock_price_minute`

Fields:
- datetime
- open
- high
- low
- close
- volume
- stock_id

---

## ⚙️ How It Works

1. Load configuration from `config.py`
2. Connect to SQLite database
3. Fetch all available stock IDs
4. Load minute-level price data per stock
5. Run Backtrader engine
6. Execute ORB strategy simulation
7. Output performance per stock

---

## 🧪 Backtesting Process

- Initial capital: **$100,000**
- Position sizing: **95% allocation per trade**
- Runs per stock individually
- Optional parameter optimization available (commented in code)

---

