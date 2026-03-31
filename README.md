# Buffett-style-stock-screening-using-ROIC-and-Treasury-yield-spread
# Buffett-Style Equity Screening using ROIC and Treasury Yield

## 1. Project Motivation

After studying Warren Buffett’s investment philosophy, I became interested in how he evaluates investment opportunities relative to risk-free returns (e.g., U.S. Treasury bonds).

Buffett emphasizes:
- Return on Invested Capital (ROIC) → business quality
- Comparing expected return vs Treasury yield → opportunity cost

This project aims to translate that philosophy into a data-driven system.

---

## 2. Objective

To identify “Buffett-style attractive companies” by combining:

1. **ROIC Trend**
   - Measures business quality and capital efficiency over time
   - Focus on persistence and growth, not just a single value

2. **Earnings Yield vs Treasury Yield**
   - Earnings Yield = 1 / P/E
   - Compared against 10-Year U.S. Treasury yield
   - Measures whether a stock offers better returns than a risk-free asset

---

## 3. Key Research Question

> Do companies with strong and persistent ROIC, combined with a high yield spread over Treasuries, produce superior long-term performance?

---

## 4. Methodology

### Step 1: Data Collection
- Stock price & P/E → yfinance
- Treasury yield (10Y) → FRED API
- ROIC → financial datasets (to be determined)

---

### Step 2: Feature Engineering

#### (1) ROIC Quality
- 5–10 year average ROIC
- ROIC trend (increasing / stable / declining)
- ROIC volatility

#### (2) Yield Spread
- Earnings Yield = 1 / P/E
- Spread = Earnings Yield – 10Y Treasury Yield

---

### Step 3: Classification Model

Companies will be categorized into:

| Category | Description |
|----------|------------|
| High ROIC + Cheap | Strong business + undervalued (ideal) |
| High ROIC + Expensive | Strong business but priced high |
| Low ROIC + Cheap | Potential value trap |
| Low ROIC + Expensive | Avoid |

---

### Step 4: Backtesting (Optional Extension)
- Evaluate whether “High ROIC + Cheap” group outperforms the market

---

## 5. Tech Stack

- Python
- pandas / numpy
- matplotlib / seaborn
- yfinance (market data)
- FRED API (macro data)

---

## 6. Project Structure
```
project-root/
│
├── data/
├── notebooks/
├── src/
│   ├── data_loader.py
│   ├── feature_engineering.py
│   ├── strategy.py
│   └── visualization.py
│
├── README.md
└── requirements.txt
```
---

## 7. Current Progress

- [ ] Set up data pipeline
- [ ] Download stock data (yfinance)
- [ ] Download treasury data (FRED)
- [ ] Define ROIC calculation/source
- [ ] Compute yield spread
- [ ] Build classification logic
- [ ] Visualization
- [ ] Backtest strategy

---

## 8. Future Improvements

- Incorporate growth rate (reinvestment)
- Add free cash flow yield
- Improve ROIC calculation accuracy
- Use rolling window analysis
- Portfolio optimization

---

## 9. Disclaimer

This project is for educational purposes only and does not constitute financial advice
