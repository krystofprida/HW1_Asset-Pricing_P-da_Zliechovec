# JEM092 – Homework 1: Financial Data & Portfolio Analysis

**Authors:** Kryštof Přída, Daniel Zliechovec  
**Course:** JEM092 Asset Pricing (SS 2025/2026), Charles University (FSV UK)  
**Language:** R  

---

## 📌 Project Overview
This repository contains our solution for Homework 1 in R. The project focuses on scraping and processing financial market data, Markowitz portfolio optimization, and stock index construction over the 2015–2024 period.

All code, data pipelines, and visual outputs are documented in `HW_1_DanielZliechovec_KrystofPrida.ipynb`.

---

## 📂 Project Tasks

### 1. Task 1 – Data Collection & Scraping
* Downloaded daily adjusted close prices and trading volume for 250 assigned tickers via Yahoo Finance.
* Scraped Market Capitalization and Book Value per Share from Macrotrends using `httr` and `rvest`.
* Cleaned and validated the panel dataset for the 2010–2026 period.

### 2. Task 2 – Markowitz Portfolio Optimization
* Analyzed 20 assigned stocks split into two portfolios (A & B) across 119 monthly return observations (2015–2024).
* Estimated expected returns and the variance-covariance structure.
* Solved for the **Global Minimum Variance Portfolio (GMVP)** and generated **Efficient Frontiers** using `PortfolioAnalytics` and `ROI`.
* Plotted the risk-return profiles and identified key frontier-driving assets.

### 3. Task 3 – Stock Index Construction
* Built and compared three custom index weighting schemes for the 20 stocks:
  1. **Price-Weighted Index** (adjusted for price levels / splits)
  2. **Equally-Weighted Index** ($1/N$ allocation)
  3. **Market-Cap-Weighted Index** (value-weighted)
* Visualized and evaluated the cumulative performance across the three methodologies.

---

## ⚙️ Requirements & How to Run

### Required R Packages
```r
install.packages(c(
  "PerformanceAnalytics",
  "PortfolioAnalytics",
  "ROI",
  "ROI.plugin.quadprog",
  "ROI.plugin.glpk",
  "xts",
  "zoo",
  "quantmod",
  "rvest",
  "httr",
  "tidyverse"
))
