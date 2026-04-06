# Factor-Based Monte Carlo VaR for European Banking Portfolio

**Bachelor Thesis Project**  
**Author**: Huy Nguyen (Student ID: 2107056)  
**Institution**: HAN University of Applied Sciences, Arnhem  
**Supervisor**: Meike Botterweg  
**Date**: April 2026

## Overview

This repository contains the complete implementation, data processing, visualizations, and reproducibility materials for my bachelor's thesis:

> **"To what extent does a rolling factor-based Monte Carlo VaR model with a 99% confidence level provide accurate risk estimates under the Basel Traffic Light backtesting framework for a portfolio of five European banks (Banco Santander, UniCredit, BNP, ING Group ,Deutsche Bank), and how does the portfolio respond to historical and hypothetical stress testing?"**

The project replicates and extends the **risk factor-based Monte Carlo VaR** model introduced by Cheng (2025), applying it to a portfolio of five major European banks:

- Banco Santander (**SAN.MC**)
- UniCredit (**UCG.MI**)
- BNP Paribas (**BNP.PA**)
- ING Group (**INGA.AS**)
- Deutsche Bank (**DBK.DE**)

**Portfolio weights**: [0.30, 0.25, 0.20, 0.15, 0.10]

The study evaluates three models at the **99% confidence level**:
- Rolling Factor-Based Monte Carlo VaR (normal market conditions)
- Historical Stressed VaR (using 2022 Russia–Ukraine war data)
- Hypothetical Stressed VaR (using simulated volatility)

All models are backtested from **February 2025 to February 2026** using the Basel III traffic-light framework.

## Key Results

- **Rolling Factor MC VaR**: Average 99% loss estimate = **3.73%** (range: 2.62% – 4.26%)  
  → **5 violations** → **Yellow zone** (Basel III)

- **Historical SVaR**: **5.13%** (1.38× rolling VaR), 2 violations

- **Hypothetical SVaR**: **6.67%** (1.79× rolling VaR), 1 violation

The rolling model demonstrates moderate-to-good performance and outperforms many Monte Carlo VaR studies reviewed in the literature for financial-sector portfolios. However, all models show limitations in capturing extreme tail events due to the multivariate normal distribution assumption.

## Repository Contents

- **`Thesis - Monte Carlo VaR.ipynb`** – Main analysis notebook (data download, factor regression & selection, rolling VaR, historical & hypothetical SVaR, backtesting, and visualizations)
- **`Reproducibility audit.ipynb`** – Full audit of Cheng (2025) original code
- **`README.md`** – Documentation on models built and results summary

- This study is based on Cheng (2025) and the models built are based on their code. The Github link to original work: https://github.com/Chengyueminga/MarketRisk_VaR
- Cheng, Y. (2025). Monte Carlo-based VaR estimation and backtesting under Basel III. Risks, 13(8), 146. https://www.mdpi.com/2227-9091/13/8/146 

## How to Reproduce

1. Clone the repository:
   ```bash
   git clone https://github.com/HuyNguyen2601/MonteCarloVaR.git
   cd MonteCarloVaR

2. Install required packages:Bash
   ```bash
   pip install pandas numpy matplotlib yfinance statsmodels jupyter
   
3. Launch Jupyter Notebook:Bash
   ```bash
   jupyter notebook

4. Open and run Thesis - Monte Carlo VaR.ipynb

## Contact
Huy Nguyen
Student number: 2107056
Email: HH.Nguyen3@student.han.nl
