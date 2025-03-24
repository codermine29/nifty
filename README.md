# MS Capital Developer Assessment – Cash Allocation Model

## Overview
This project builds a data-driven model to recommend optimal cash allocation in equity portfolios using Indian market liquidity indicators.

## Setup Instructions
1. Run all cells in the provided Google Colab notebook.
2. Required packages: `pandas`, `yfinance`, `matplotlib`, `requests`, `beautifulsoup4`
3. Output files:
   - `nifty50_raw.csv`
   - `repo_rate_data.csv`
   - `cash_allocation_output.csv`

## Data Sources
- Nifty 50: Yahoo Finance (`yfinance`)
- Repo Rate: Mocked RBI data (can be replaced with scraped data)
- VIX & Midcap data: Excluded due to source restrictions

## Key Features
- 30-day rolling volatility from Nifty 50 returns
- Interest rate feature from repo rate
- Liquidity scoring using weighted sum

## Cash Allocation Model
- Inputs: Volatility & Repo Rate (normalized)
- Scoring: 60% volatility, 40% repo rate
- Risk profiles: low/medium/high
- Output: Cash % between 0.1 – 1.0

## How to Run
1. Run notebook cells
2. Adjust `risk_setting = 'low' | 'medium' | 'high'`
3. View output plot and download final CSVs
