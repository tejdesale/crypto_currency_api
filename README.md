![Crypto Price Tracker](https://your-image-host.com/crypto-banner.jpg)

# Crypto Price Tracker & Email Reporter 📈📧

A Python script that fetches real-time cryptocurrency market data from the CoinGecko API, saves it to a CSV file, identifies the top gainers and losers of the day, and emails a daily report — designed to run automatically every morning at 8 AM.

## Features

- Fetches live market data for the top 250 cryptocurrencies by market cap
- Tracks price, market cap, 24h price change, 24h high/low, all-time high (ATH), and all-time low (ATL)
- Saves the full dataset to a timestamped CSV file
- Identifies the top 10 gainers and top 10 losers over the last 24 hours
- Sends an automated email report with the CSV attached
- Can be scheduled to run daily at a set time using the schedule library

## How It Works

1. Sends a request to the CoinGecko markets endpoint for 250 coins
2. Cleans the response into a Pandas DataFrame with the relevant columns
3. Adds a timestamp column and saves the data to a CSV file
4. Filters the top 10 positive and top 10 negative movers by 24h price change
5. Composes an email with a summary in the body and the full CSV attached
6. Sends the email via Gmail's SMTP server
7. Optionally runs on a schedule, once a day at a fixed time

## Requirements

- Python 3.9+
- Dependencies: requests, pandas, schedule

## Setup

1. Clone the repository to your machine.
2. Install the required dependencies listed above.
3. Configure your email credentials as environment variables rather than hardcoding them in the script (see Security Note below). You'll need a Gmail App Password rather than your regular account password.
4. Run the script to fetch data and send the report immediately, or enable the built-in scheduler to have it run automatically every day at 8 AM.


## Project Structure

- crypto_tracker.py — Main script
- requirements.txt — Python dependencies
- README.md — This file


## Disclaimer

This project is for educational and informational purposes only. It is not financial advice. Cryptocurrency markets are highly volatile — always do your own research before making investment decisions.
