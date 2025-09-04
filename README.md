# Value-Investing-using-GreenBlat-Formula

# 📈 Magic Formula Value Investing (Greenblatt Strategy)

This repository implements **Joel Greenblatt’s Magic Formula** for value investing, adapted to work with both **US** and **Indian** stocks using live financial data from [Yahoo Finance](https://finance.yahoo.com) via the [`yfinance`](https://github.com/ranaroussi/yfinance) Python library.

---

## 🧠 What is the Magic Formula?

The Magic Formula was introduced by Joel Greenblatt in *The Little Book That Still Beats the Market*.  
It systematically ranks companies to find **“good businesses at bargain prices”** using two metrics:

1. **Earnings Yield (EY)** – how cheap the stock is  
   \[
   EY = \frac{EBIT}{Enterprise\ Value}
   \]

2. **Return on Capital (ROC)** – how good the business is  
   \[
   ROC = \frac{EBIT}{Net\ Fixed\ Assets + Working\ Capital}
   \]

Stocks are ranked on both, and the combined rank gives the **Magic Formula Rank**.

---

## 📊 Features

- Works with both **Indian (.NS)** and **US** stocks.
- Uses only `yfinance` (no fragile HTML scraping).
- Computes:
  - EBIT
  - Enterprise Value (TEV)
  - Earnings Yield (EY)
  - Return on Capital (ROC)
  - Free Cash Flow Yield
  - Book-to-Market
  - Dividend Yield
- Ranks stocks by the Magic Formula.
- Outputs a ranked DataFrame and saves results to CSV.

---

## 🛠️ Installation

Clone the repo:

```bash
git clone https://github.com/your-username/magic-formula-value-investing.git
cd magic-formula-value-investing
