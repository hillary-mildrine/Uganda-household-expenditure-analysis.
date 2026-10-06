# Multi-Variable Econometric Modeling & Data Validation Pipeline (1990–2020)

## Project Overview
This repository features an end-to-end data analytics and econometric modeling project utilizing 30 years of macroeconomic time-series data extracted from the World Bank’s World Development Indicators (WDI). The project constructs an Ordinary Least Squares (OLS) framework to isolate structural determinants of aggregate consumer demand, simulating how fiscal volatility impacts household expenditure.

## Technical Tech Stack & Methodology
* **Tools Used:** Stata, Microsoft Excel
* **Data Ingestion & ETL:** Processed and standardized raw, multi-variable global macroeconomic indicator sheets; executed data cleaning, variable isolation, and missing-variable handling.
* **Feature Engineering:** Implemented data-transformation protocols, utilizing mathematical differencing to resolve non-stationarity across variables.

## Statistical Auditing & Diagnostic Pipeline
To guarantee absolute model stability and eliminate spurious regression risks for decision-making, I built a rigid validation pipeline executing advanced diagnostic checks:
* **Stationarity Assurance:** Verified all variables via Augmented Dickey-Fuller (ADF) unit-root testing to ensure integration at first difference.
* **Multicollinearity Diagnostic:** Executed Variance Inflation Factor (VIF) checks confirming structural stability with an acceptable Mean VIF of 3.86.
* **Error Term Auditing:** Conducted Breusch-Godfrey LM testing confirming zero serial correlation (p-value = 0.7727) and audited for homoscedasticity (p-value = 0.9534).
* **Distribution Verification:** Applied residual normality checks using standard sktest protocols (p-value = 0.4055).

## Enterprise & Strategic Value
* **Predictive Accuracy:** Achieved an **R-squared of 0.6784**, demonstrating that the engineered model successfully accounts for 67.8% of historical consumption variances.
* **Actionable Insights:** Quantified the statistical impact of public debt expansion and gross domestic savings shifts, providing a scalable quantitative framework useful for international fiscal planning, asset allocation, and market risk assessment.

## Files in this Repository
* `cleaned_macro_data.xlsx` - Cleaned macroeconomic time-series indicators used for modeling.
* `analysis.do` - Raw Stata command script containing the full OLS and diagnostic pipeline syntax.
* `academic_report.pdf` - Full Academic Research Report containing the methodology, data tables, and comprehensive economic literature review.
