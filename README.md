# Financial News Summarization & Sentiment Analysis 

## Overview
This project automates the collection, summarization, and sentiment analysis of financial news articles from **Yahoo Finance RSS feeds**. It extracts key insights using **NLP models**, providing a concise view of market sentiment across various assets, including **stocks, cryptocurrencies, indices, and forex**.

## Features
- **Multi-asset coverage**: SPY, AAPL, GOOGL, TSLA, BTC-USD, ETH-USD, AMZN, MSFT, DJI, IXIC, CRYPTO, FOREX.
- **Automated article fetching** from **Yahoo Finance RSS feeds**.
- **Text extraction** using `newspaper3k`.
- **Summarization** using `facebook/bart-large-cnn`.
- **Sentiment analysis** using `FinBERT`.
- **Multi-threaded processing** (`ThreadPoolExecutor`) for faster execution.
- **Exports results** to `financial_news_summary.csv`.

## Technical Specifications
- **Programming Language**: Python
- **Data Sources**: Yahoo Finance RSS Feeds
- **Machine Learning Models**:
  - **Summarization**: `facebook/bart-large-cnn`
  - **Sentiment Analysis**: `yiyanghkust/finbert-tone`
- **Libraries Used**:
  - `transformers` (NLP models)
  - `newspaper3k` (article extraction)
  - `beautifulsoup4` (HTML parsing)
  - `feedparser` (RSS feed handling)
  - `concurrent.futures.ThreadPoolExecutor` (parallel processing)
  - `pandas` (data handling)
  - `requests` (HTTP requests)
  - `torch` (PyTorch backend for NLP)

## Installation
**Clone the repository**
   ```bash
   git clone https://github.com/rupamdusane/Finance-News-Sentiment-and-Summarization.git
   cd Finance-News-Sentiment-and-Summarization
   ```

## How It Works
1. **Fetches Articles**: The script retrieves financial news articles from **Yahoo Finance RSS feeds** for multiple assets.
2. **Extracts Text**: Uses `newspaper3k` to scrape the full article content.
3. **Summarizes Content**: The `facebook/bart-large-cnn` model condenses the article into a short summary.
4. **Performs Sentiment Analysis**: The `FinBERT` model classifies the sentiment as **Positive, Neutral, or Negative**.
5. **Saves Output**: The processed data is stored in `financial_news_summary.csv` with the following fields:
   - **Ticker** (e.g., AAPL, BTC-USD)
   - **Title** (Article headline)
   - **Publication Date**
   - **Summary** (Generated text)
   - **Sentiment** (Positive, Neutral, Negative)
   - **URL** (Original article link)

## Future Enhancements
- **Real-time news monitoring** instead of batch processing.
- **Advanced visualization dashboards** for sentiment trends.
- **Integration with stock price movements** for correlation analysis.

## Contributing
This is a personal project, but feedback and suggestions are always welcome!  
If you'd like to contribute, feel free to fork the repository.
