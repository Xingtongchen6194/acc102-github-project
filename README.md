# BatteryCompare: Global Battery Leaders Stock Analysis

## 1. Problem & User

**Problem**: Many beginner investors do not know how to compare stocks in a simple and practical way. They often look at price changes only, without considering risk or risk-adjusted returns.

**Target User**: Beginner investors interested in the electric vehicle battery sector, students learning financial data analysis, and general users who want a simple comparison of battery stock performance.

## 2. Data

- **Source**: East Money Information Co., Ltd.
- **Access Date**: 23 April 2026
- **Time Period**: 1 April 2024 - 1 April 2025 (one full year)
- **Stocks Analyzed**: CATL (300750), BYD (002594), EVE Energy (300014)
- **Key Fields**: Date, Closing Price (used for analysis)

## 3. Methods

1. **Data Acquisition**: Downloaded historical stock data from East Money's public API
2. **Data Cleaning**: Removed missing values using `dropna()`
3. **Daily Returns Calculation**: `(Today's Price - Yesterday's Price) / Yesterday's Price`
4. **Annualized Return**: Mean daily return × 252 trading days
5. **Annualized Volatility**: Standard deviation of daily returns × √252
6. **Sharpe Ratio**: (Return - Risk-Free Rate) / Volatility (risk-free rate = 2%)
7. **Maximum Drawdown**: Largest peak-to-trough decline
8. **Composite Scoring**: Weighted ranking (Return 30%, Volatility 20%, Sharpe 30%, Drawdown 20%)

## 4. Key Findings

| Metric | BYD | CATL | EVE Energy |
|--------|-----|------|------------|
| Annual Return | **66.14%** | 39.10% | 33.48% |
| Annual Volatility | **36.97%** | 45.25% | 58.40% |
| Sharpe Ratio | **1.73** | 0.82 | 0.54 |
| Max Drawdown | **-18.98%** | -23.66% | -28.81% |

**Conclusion**: BYD outperformed in all metrics, offering the highest return with the lowest risk. BYD's Sharpe Ratio of 1.73 indicates exceptional risk-adjusted performance.

## 5. How to Run

### Prerequisites
- Python 3.8 or higher
- Jupyter Notebook or JupyterLab

### Steps
1. Clone this repository:
   ```bash
   git clone https://github.com/Xingtongchen6194/acc102-github-project.git
   ```
2. Navigate to the project folder:
   ```bash
   cd acc102-github-project
   ```
3. Install required packages:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```
4. Open `Battery_Stock_Analysis.ipynb` in Jupyter Notebook
5. Run all cells (Kernel → Restart & Run All)

## 6. Product Link / Demo

- **GitHub Repository**: https://github.com/Xingtongchen6194/acc102-github-project
- **Demo Video**: (coming soon)

## 7. Limitations & Next Steps

### Current Limitations
- Only one year of historical data
- Only three stocks analyzed
- Price-only analysis (no fundamental metrics)
- External factors not considered (raw material prices, government policies)
- Simplified risk-free rate assumption (2%)

### Next Steps / Future Improvements
- Add more battery stocks (LG Energy Solution, Samsung SDI, Panasonic)
- Include fundamental analysis (P/E ratio, revenue growth, profit margins)
- Add technical indicators (moving averages, RSI)
- Build an interactive dashboard using Streamlit
- Extend time period to multiple years

## Repository Structure

```
acc102-github-project/
├── Battery_Stock_Analysis.ipynb   # Main analysis notebook
├── 300750.csv                     # CATL raw data
├── 002594.csv                     # BYD raw data
├── 300014.csv                     # EVE Energy raw data
└── README.md                      # Project documentation
```

## Author

ACC102 Mini Assignment - Track 2 GitHub Data Analysis Project  
Xi'an Jiaotong-Liverpool University

## AI Disclosure

- **Tool**: ChatGPT (GPT-4)
- **Access Date**: 23 April 2026
- **Purpose**: Code debugging, README documentation, financial metrics guidance

## Disclaimer

This project is for educational purposes only. Past performance does not guarantee future results. This does not constitute financial advice.
```
