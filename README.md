# 📊 Risk Modeling Project (Group Assignment – MSc Quantitative Finance)

This repository presents a comprehensive risk modeling project developed as part of the UCD MSc Quantitative Finance curriculum. The project involved constructing and analyzing Value at Risk (VaR) and Expected Shortfall (ES) measures across equity, interest rate, and combined portfolios using both historical and parametric methods.

## 🎯 Project Objective

The goal was to build three distinct portfolios (Equity Risk, Interest Rate Risk, and Combined Risk) and apply various risk estimation techniques to:

- Estimate Value at Risk (VaR) and Expected Shortfall (ES)
- Compare and validate risk models using backtesting
- Evaluate performance using Sharpe Ratios and scenario analysis
- Incorporate stress testing and portfolio diversification insights

## 👨‍💻 My Contribution

I actively contributed to and independently managed the following components:

- 📈 **Equity Risk Portfolio**: Constructed a diversified portfolio of equities, calculated log returns, and estimated risk using:
  - Historical Simulation
  - Parametric Normal and t-distribution methods
  - Exponentially Weighted Moving Average (EWMA)

- 💸 **Interest Rate Risk Portfolio**: Developed a bond portfolio and computed interest rate VaR using duration and convexity adjustments.

- 🔗 **Combined Portfolio**: Integrated equity and interest rate portfolios, implemented variance-covariance matrix adjustments, and tested diversification benefits.

I also helped in presenting results and interpreting model behavior under normal and stress market conditions.

## 📅 Data Used

We used **daily market data** from **01 January 2019 to 27 March 2024** for:

- **Equities**: Stock prices from global exchanges
- **Bonds**: Government bond yield and price data
- **Risk-Free Rate**: Used for Sharpe Ratio and discounting
- Sources: Yahoo Finance and public data repositories
- Processed in Excel with manual cleaning for corporate actions (e.g., dividends, splits)

### Data Transformations:
- Daily **log returns** computed from closing prices
- Applied **EWMA (λ = 0.94)** for volatility smoothing
- Rolling window used for VaR/ES estimation

## 🧪 Methodology

Risk estimation techniques applied:

- **Historical Simulation (HS)**
- **Parametric VaR** (Normal and Student's t)
- **Expected Shortfall (ES)** at 95% and 99% confidence levels
- **EWMA volatility weighting**
- **Backtesting** using Kupiec’s test
- **Stress Testing** via hypothetical extreme scenarios
- **Sharpe Ratio** and Performance Metrics

## 📊 Key Results

- The **equity portfolio** had the highest volatility and exhibited left-tail risk under both HS and parametric VaR.
- The **interest rate portfolio** showed relatively lower risk, but stress tests revealed convexity-led tail exposures.
- The **combined portfolio** benefited from diversification, with reduced VaR and higher Sharpe ratios.
- Backtesting confirmed the robustness of the t-distribution model compared to normal VaR in capturing fat-tailed risks.

## 🛠️ Tools & Technologies

- **Microsoft Excel** for modeling, charts, and data transformation
- **PowerPoint** for risk report and presentation
- **Python/Power BI (Planned future extension)** for dynamic dashboards and real-time VaR

