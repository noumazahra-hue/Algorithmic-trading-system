<div align="center">
  <img src="https://via.placeholder.com/1200x400/0a0a0f/c8a96e?text=Algorithmic+Trading+Signal+System" 
       alt="Trading System Banner" width="100%"/>
  
  <h1>Algorithmic Trading Signal System</h1>
  
  <p>
    <strong>Personal Project • 2026</strong><br>
    Author: Zahra Nouma<br>
  </p>

  <p>
    <a href="https://github.com/noumazahra-hue">
      <img src="https://img.shields.io/badge/GitHub-Profile-blue?style=flat&logo=github" alt="GitHub">
    </a>
    <img src="https://img.shields.io/badge/Python-3.10%2B-blue?style=flat&logo=python" alt="Python">
    <img src="https://img.shields.io/badge/Automation-Daily-success?style=flat" alt="Automation">
    <img src="https://img.shields.io/badge/Assets-6%20Monitored-orange?style=flat" alt="Assets">
    <img src="https://img.shields.io/badge/Signals-BUY%20%7C%20SELL%20%7C%20HOLD-red?style=flat" alt="Signals">
  </p>
</div>

---

## Abstract

A fully automated algorithmic trading signal system** that monitors 6 major financial assets daily including US equities and cryptocurrency. The system fetches live market data, computes technical indicators (RSI, Momentum, Moving Averages), generates BUY/SELL/HOLD signals based on rule-based logic, and delivers a professional HTML email report automatically every day — with zero manual intervention.

## Key features:
- Real-time data fetching via Yahoo Finance API
- RSI-based overbought/oversold signal detection
- Momentum analysis for trend confirmation
- MA50/MA200 crossover for uptrend filtering
- Automated daily email report with color-coded signals
- JSON logging for signal history tracking

## Monitored Assets

| Ticker   | Asset                  | Type       |
|----------|------------------------|------------|
| AAPL     | Apple Inc.             | Equity     |
| MSFT     | Microsoft Corp.        | Equity     |
| AMZN     | Amazon.com Inc.        | Equity     |
| NVDA     | NVIDIA Corp.           | Equity     |
| META     | Meta Platforms Inc.    | Equity     |
| BTC-USD  | Bitcoin                | Crypto     |

## Signal Logic

| Condition                  | Signal  |
|----------------------------|---------|
| RSI > 70                   | 🔴 SELL |
| RSI < 30 + Uptrend = True  | 🟢 BUY  |
| Everything in between      | 🟡 HOLD |

> The system uses MA50 > MA200 as an uptrend confirmation filter before generating BUY signals, reducing false positives in bearish market conditions.
> 
## Sample Output (2026-04-20)

| Asset    | Signal | Price      | RSI  | Momentum |
|----------|--------|------------|------|----------|
| AAPL     | 🔴 SELL | $272.57   | 75.0 | 9.9%     |
| MSFT     | 🔴 SELL | $419.87   | 80.8 | 9.9%     |
| AMZN     | 🔴 SELL | $247.54   | 77.9 | 20.5%    |
| NVDA     | 🔴 SELL | $199.66   | 76.7 | 15.6%    |
| META     | 🔴 SELL | $673.38   | 71.4 | 13.4%    |
| BTC-USD  | 🟡 HOLD | $75,855   | 62.5 | 11.2%    |

## Repository Structure

algorithmic-trading-system/
├── requirements.txt         # Python dependencies
├── README.md               
├── samples/
│   └── daily_alerts.json    # Sample signal output
└── screenshots/
    └── email_report.png     # Sample HTML email report

## Key Results

 ✅ **100% automated** runs daily with zero manual intervention
 ✅ **Real-time data** live prices from Yahoo Finance API
 ✅ **6 assets monitored**  equities + crypto
 ✅ **3 technical indicators**  RSI, Momentum, MA50/MA200
 ✅ **Professional email report**  HTML formatted, color-coded signals
 ✅ **Signal history** JSON logging for every daily run

## Implementation Details

 **Language:** Python 3.10+
 **Data Source:** Yahoo Finance (yfinance)
 **Indicators:** RSI (14-period), Momentum (20-period), MA50, MA200
 **Automation:** Google Colab / Scheduler
 **Email:** SMTP with HTML template
 **Storage:** JSON daily logs


## Technical Indicators Explained

**RSI (Relative Strength Index)**
Measures the speed and magnitude of price changes. Values above 70 indicate overbought conditions (SELL), below 30 indicate oversold conditions (BUY).

**Momentum**
Measures the percentage price change over 20 trading days. High momentum (>10%) signals an overextended move — used to confirm SELL signals.

**MA50 / MA200 (Moving Averages)**
When MA50 > MA200, the asset is in a long-term uptrend. This acts as a filter — BUY signals are only generated in confirmed uptrends.

## For Recruiters

This project demonstrates:

 **Python automation** : end-to-end pipeline with zero manual steps
 **Financial data engineering** : real-time API integration
 **Technical analysis** : RSI, Momentum, Moving Averages
 **Signal generation logic** : rule-based decision system
 **Email automation** : professional HTML report generation
 **Data logging** : structured JSON output for history tracking
 **Quantitative thinking**  translating market theory into code


## Visual Results

### Daily Email Report
![Email Report](screenshots/email_report.png)
