# 📈 Magic Formula Value Investing

This project implements **Joel Greenblatt’s Magic Formula**, a systematic approach to value investing introduced in *The Little Book That Still Beats the Market*.  

The formula is designed to help investors find **good companies at cheap prices** by ranking stocks on two simple measures: **Earnings Yield** and **Return on Capital**.

---

## 🧠 The Magic Formula

The strategy uses two key metrics:

1. **Earnings Yield (EY)** – a measure of cheapness  
   \[
   EY = \frac{EBIT}{Enterprise\ Value}
   \]  
   - **EBIT** = Earnings Before Interest and Taxes (operating profit)  
   - **Enterprise Value (EV)** = Market Cap + Debt − Cash  
   - Higher EY → cheaper stock relative to its earnings power  

2. **Return on Capital (ROC)** – a measure of quality  
   \[
   ROC = \frac{EBIT}{Net\ Fixed\ Assets + Working\ Capital}
   \]  
   - Shows how efficiently a company generates profits from the capital it uses  
   - Higher ROC → stronger business  

**Ranking:**  
- Rank all stocks by EY (highest = rank 1)  
- Rank all stocks by ROC (highest = rank 1)  
- Add the two ranks → lower combined score = better investment  

---

## 📊 What the Code Does

1. **Fetches Data**  
   - Uses `yfinance` to download financial data for a list of large US and Indian stocks.  
   - Pulls information such as EBIT, Market Cap, Debt, Cash, PPE, and Cash Flow.  

2. **Computes Metrics**  
   - Calculates EBIT, Enterprise Value, Earnings Yield, Return on Capital.  
   - Also computes supporting ratios like Free Cash Flow Yield, Book-to-Market, and Dividend Yield.  

3. **Ranks Stocks**  
   - Ranks each stock separately on EY and ROC.  
   - Combines ranks into a **Magic Formula Score**.  
   - Sorts stocks so the top-ranked are both **cheap and high-quality**.  

4. **Outputs Results**  
   - Produces a ranked table of stocks with their fina
