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

## 👨‍💻 My Role (Pranjal Kharbanda)

I contributed to the **design, modeling, and evaluation** of all three portfolios. This included hands-on implementation, data preparation, and performance analysis.

### ✅ Equity Portfolio
- Collected and cleaned equity data from Yahoo Finance
- Implemented Tangency Portfolio weight selection using Sharpe Ratios in Python
- Calculated log returns, VaR, and ES using multiple methods (Normal, Historical, t-distribution)
- Backtested rolling-window exceedances and validated findings using QPS scores

### ✅ Interest Rate Portfolio
- Selected bond ETFs and validated fixed income data consistency
- Developed volatility-weighted Historical VaR using the **EWMA** method (λ = 0.94)
- Performed risk decomposition using bond duration, convexity, and spectral risk measures

### ✅ Combined Portfolio
- Integrated equity and bond return streams
- Computed multi-asset portfolio VaR using correlation-adjusted Normal and t-distributions
- Analyzed diversification benefits and performed backtesting using **Lopez Test**

---

### 📘 Additional Responsibilities & Learnings

- **Data Sourcing**: Extracted daily price and yield data from Yahoo Finance and Kenneth French's database
- **Model Deployment**: Worked with Excel and Python to apply parametric and non-parametric models across rolling 550-day windows
- **Documentation & Presentation**: Contributed to the structure and clarity of the final report and slide deck

#### 📚 What I Learned
- Developed applied skills in **portfolio-level VaR modelling**
- Practiced **rolling-window backtesting** and performance validation using **QPS scoring**
- Gained deeper insight into how **asset allocation** affects sensitivity and stability of risk estimates
- Strengthened my ability to connect **finance theory with data-driven analytics**, particularly around capital preservation and institutional risk control

---

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
