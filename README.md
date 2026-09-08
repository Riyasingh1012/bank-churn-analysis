# Bank Customer Churn Analysis

## Overview
This project analyzes customer churn for a bank using a real-world dataset of 10,000 customers, identifying key drivers of churn across geography, age, product usage, and account engagement. The goal is to answer: **who is leaving, and why** — and translate that into actionable retention recommendations.

## Tools Used
- **Python** — pandas, numpy, matplotlib, seaborn
- **SQLite** — data loading and querying via `sqlite3`
- **Jupyter Notebook**

## Key Findings
- **Overall churn rate: 20.4%**
- **Germany** churns at nearly double the rate of France/Spain, despite having fewer customers — driven by significantly higher average account balances in that segment
- The **46-60 age group** has the highest churn risk, with churn notably higher among women within that bracket
- Customers with **3-4 products** churn dramatically more than those with 1-2 — a non-linear pattern that isn't visible in a standard correlation analysis
- **Inactive members** churn at roughly 2x the rate of active members — the most actionable lever for retention

## Recommendations
1. Offer tailored retirement-planning products and dedicated relationship management for the 46-60 age segment
2. Audit interest rates, fees, and account terms for high-product customers, who have the most incentive to switch banks
3. Launch a targeted re-engagement campaign (fee waivers, personalized offers) for inactive members

## Files
- `Bank_Churn_Analysis.ipynb` — full analysis notebook
- `Churn_Modelling.csv` — dataset (source: Kaggle)



## 🤖 Machine Learning Model

### Random Forest Classifier - Churn Prediction

**Performance Metrics:**
- **Accuracy: 85.85%** ✅
- **Precision: 74.55%**
- **Recall: 42.49%**
- **F1-Score: 0.5413**

### Top 5 Churn Drivers:
1. **Age** (24.83%)
2. **EstimatedSalary** (16.73%)
3. **CreditScore** (16.18%)
4. **Balance** (14.88%)
5. **NumOfProducts** (13.12%)

### Model Details:
- **Algorithm:** Scikit-learn Random Forest
- **Trees:** 100
- **Training Samples:** 8,000
- **Testing Samples:** 2,000
- **Features:** 8 numeric features

### Key Insights:
This model identifies at-risk customers with 85.85% accuracy, enabling targeted retention strategies based on customer demographics and financial behavior.
