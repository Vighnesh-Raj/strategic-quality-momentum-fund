# Strategic Quality-Momentum Fund (SQMF)

This project implements a long-only, value-weighted U.S. equity factor strategy called the **Strategic Quality-Momentum Fund (SQMF)**. The fund selects large-cap stocks each quarter based on three academic and empirically supported signals:

- **Low Volatility** (Ang et al., 2006): Prefer stable return profiles  
- **High Momentum** (Jegadeesh and Titman, 1993): Past 12-to-2-month returns  
- **High Profitability (ROE)** (Novy-Marx, 2013): Strong earnings performance  

The goal is to deliver superior risk-adjusted returns through a disciplined, rules-based strategy, with transparent factor exposures and quarterly rebalancing.

---

## 🧠 Methodology

1. **Universe Screening**: Top 1,000 U.S. stocks by market cap and dollar volume, price > $5  
2. **Factor Rankings**:
   - Volatility: Ascending (lower is better)
   - Momentum (R11): Descending (higher is better)
   - Profitability (ROE): Descending (higher is better)
3. **Score & Selection**: Average rank across 3 signals; select top 100 stocks  
4. **Weighting**: Value-weighted by market cap  
5. **Rebalancing**: Quarterly  

---

## 📈 Performance Highlights (1994–2023)

- **Positive Returns** in 25 of 30 years  
- **30-Year CAGR**: **11.43%** vs. **10.15%** (S&P 500)  
- **Annual Sharpe Ratio**: **0.62** vs. **0.52** (S&P 500)  
- **Volatility**: 16.82% (lower than S&P 500's 18.23%)  
- **Max Drawdown in 2008**: **-39.1%** vs. **-51.0%** (S&P 500)  
- **Cumulative Return**: Grew $10,000 to **$256,964** vs. **$181,945** in S&P 500  
- **3-Year CAGR**: **29.35%**, **5-Year CAGR**: **16.70%**, **10-Year CAGR**: **8.03%**

---

## 📊 Regression Analysis vs Factor Models

| Model       | Alpha (monthly) | Market Beta | SMB (Size) | HML (Value) | Interpretation                          |
|-------------|------------------|-------------|------------|-------------|------------------------------------------|
| CAPM        | 0.27% **         | 0.80        | —          | —           | Positive alpha, moderate market exposure |
| Fama-French 3-Factor | 0.27% **     | 0.84        | -0.27      | -0.09       | Large-cap growth tilt, consistent alpha  |

- **Alpha**: Statistically significant at the 5% level in both models
- **Market Beta**: Less than 1, indicating lower sensitivity to market movements
- **SMB (Size)**: Negative, reflecting a preference for large-cap stocks
- **HML (Value)**: Slightly negative, indicating a tilt away from deep value toward growth/profitability

 

---

## 💼 Top Holdings (as of 2023 Q4)

| Rank | Ticker | Name        | Weight |
|------|--------|-------------|--------|
| 1    | AAPL   | Apple       | 20.69% |
| 2    | MSFT   | Microsoft   | 19.31% |
| 3    | AMZN   | Amazon      | 10.85% |
| 4    | NVDA   | NVIDIA      | 8.45% |
| 5    | META   | Meta        | 5.43% |

---

## ⚠️ Risks & Limitations

- Vulnerable to **momentum crashes** or **regime shifts**  
- Value-weighting can lead to concentration risk (e.g., AAPL/MSFT > 40%)  
- Assumes frictionless execution (no trading costs/slippage)  

---

## 📂 Files

- `Final_Project_VR.ipynb`: Full modeling process and backtest  
- `Final Project.pdf`: Project summary, slides, and results  

---

## 🧠 Author

Vighnesh Raj  
MS Business Analytics, University of Cincinnati  
📧 vighnesh_raj@live.com
