# 📊 Risk Modelling of Equity, Bond, and Mixed Portfolios

## Overview

This project, part of the "Portfolio and Risk Management" module at UCD, investigates the **Value at Risk (VaR)** and **Expected Shortfall (ES)** of three investment strategies. The aim is to assess the robustness of risk models under various market conditions using both **parametric** and **non-parametric** techniques.

We model and compare:
- A portfolio comprising S&P 500 equities
- A bond portfolio comprising government and corporate bond ETFs
- A mixed portfolio combining 60% bonds and 40% equities

Our analysis supports **risk management decision-making** through the use of statistical backtesting, spectral risk measures, and sensitivity testing.

---

## 🧾 Objective

To evaluate how well-capitalised financial institutions are against market shocks by identifying which VaR/ES methodology best captures market risk across different portfolio structures.

---

## 📂 Data

- **Source**: Yahoo Finance and Kenneth French's Data Library
- **Period**: January 1, 2019 – March 27, 2024 (5 years)
- **Assets**:
  - **Equity Portfolio**: Top stock by market cap from each of the 11 GICS sectors (e.g., XOM, META, JPM)
  - **Bond Portfolio**: ETFs like BND, AGG, LQD, GOVT representing U.S. government and corporate bonds
  - **Combined Portfolio**: 60% bonds, 40% equities
- **Data Frequency**: Daily adjusted closing prices

---

## 🧠 Methodology

### 📐 Parametric Methods
- **Normal Distribution VaR**
- **Student’s t-Distribution VaR**
- **Cornish-Fisher Expansion**: Adjusts for skewness and kurtosis

### 📊 Non-Parametric Methods
- **Historical Simulation (HS)**
- **Volatility-Weighted HS (EWMA model)**

### 🧮 Alternative Method
- **Spectral Risk Measures** (Cotter & Dowd 2006): Used with a risk aversion coefficient (λ = 550)

### ✅ Backtesting & Sensitivity Analysis
- **Lopez Test** and **Binomial Exceedance Test** performed on rolling windows of 550 days
- Stress-tested different VaR techniques against changing asset weights and lambda decay factors

---

## 📈 Key Results

| Portfolio Type        | Best Performing VaR Method     | QPS Score |
|-----------------------|-------------------------------|-----------|
| Equity                | Normal Linear VaR              | 0.014     |
| Bonds                 | Normal Linear VaR              | 0.007     |
| Equity + Bonds (60/40)| Normal Linear VaR              | 0.014     |

- **Historical and Student’s t-distributions** were close contenders but showed slightly higher exceedance frequencies.
- **Sensitivity analysis** confirmed that asset allocation and lambda decay values significantly impact VaR estimations.

---

## 🧪 Visuals & Insights
- All backtesting and rolling-window simulations were visualized.
- EWMA decay factor λ = 0.85 showed higher responsiveness to recent volatility, enhancing VaR precision.
- Spectral risk measures (with 5000 slices) were explored for deeper tail risk insights.

---

## 🧑‍💻 My Contributions (Pranjal Kharbanda)

- **Data Sourcing**: Collected daily financial data for all portfolios via Yahoo Finance and Kenneth French Library.
- **Portfolio Allocation**: Helped structure the equity and bond portfolios by applying tangency weights using Python.
- **Editing**: Contributed to final report editing, ensuring accuracy and clarity of financial methodology.
- **Learnings**:
  - Gained experience in **portfolio-level VaR modelling**
  - Understood **rolling-window backtesting** and **QPS scoring**
  - Developed insight into **asset allocation effects** on risk models
  - Practiced advanced **Python-based data analytics** and applied **finance theory** into practical risk assessment

---

## 📚 Literature Foundation

Key models and approaches were drawn from:
- John Hull (2012), Kevin Dowd (2005)
- Acerbi & Tasche (2002) for Cornish-Fisher and ES
- Cotter & Dowd (2006/07) for Spectral Risk
- Lopez (1998) for empirical backtesting frameworks

---

## 💡 Conclusion

The study recommends the **Normal Linear VaR model** as the most robust and industry-relevant choice for all three portfolios. Backtesting and sensitivity testing validate its lower exceedance rates and consistent performance under different market scenarios.

---

## 📎 Files Included

- `Risk_Modelling(Group-25).xlsx`: Full model and calculations
- `PR_Assignment Risk Modelling.pdf`: Full write-up


---

## 📌 Keywords

`VaR`, `Expected Shortfall`, `Spectral Risk`, `Portfolio Management`, `Backtesting`, `EWMA`, `Cornish-Fisher`, `QPS`, `Financial Risk Modelling`, `UCD MSc Quantitative Finance`
