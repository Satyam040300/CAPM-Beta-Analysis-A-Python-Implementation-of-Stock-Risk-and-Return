# Capital Asset Pricing Model (CAPM) - Stock Analysis

This project implements the **Capital Asset Pricing Model (CAPM)** to analyze stock returns and estimate **Beta**, which measures the volatility of a stock relative to the market. The project compares high-beta and low-beta stocks by performing a **linear regression** between stock returns and market returns, and then applies the CAPM formula to estimate expected returns.

## Project Overview

- **Objective**: Calculate Beta for stocks and apply the **CAPM formula** to estimate the expected return for the stock.
- **Stocks Analyzed**: Apple (AAPL), Tesla (TSLA), Coca-Cola (KO), Procter & Gamble (PG), and others.
- **Market Benchmark**: S&P 500 Index (Ticker: `^GSPC`).
- **Tools Used**: 
  - **Python** 
  - **yfinance** for downloading historical stock and market data.
  - **statsmodels** for performing linear regression.
  - **matplotlib** and **seaborn** for visualization.

## How It Works

1. **Data Download**: The script downloads historical data for a stock (e.g., Apple) and the S&P 500 index from Yahoo Finance.
2. **Return Calculation**: Daily stock and market returns are calculated based on adjusted closing prices.
3. **Regression**: A linear regression is performed to calculate **Beta** (the stock's sensitivity to market returns).
4. **CAPM**: Using the CAPM formula, the expected return for the stock is calculated:
   
   \[
   E(R) = R_f + beta * (R_m - R_f)
   \]

   Where:
   - \( R_f ) is the risk-free rate (e.g., 4% for 10-year U.S. Treasury).
   - \( beta ) is the Beta value from the regression.
   - \( R_m ) is the average market return.

5. **High-Beta vs Low-Beta Stocks**: The script compares **high-beta** and **low-beta** stocks using the same methodology.
6. **Visualization**: A scatter plot is generated to visualize the risk-return trade-off for the analyzed stocks.

## Usage
Run the Python script

The script will display the following outputs:

Beta value for the stock.
Expected Return using the CAPM formula.
A scatter plot comparing stock returns and market returns.
Results for high-beta and low-beta stocks will be printed in the console.

## Example Output

**Beta:** 1.2105

**Expected Return using CAPM:** 10.72%

**High-Beta Stocks:**

**AAPL Beta:** 1.2105

**TSLA Beta:** 1.4897

**GOOGL Beta:** 1.1056

**Low-Beta Stocks:**

**KO Beta:** 0.4864

**PG Beta:** 0.3718

**JNJ Beta:** 0.6552

The generated plot will show the relationship between Market Return and Stock Return for the selected stock, along with a red regression line indicating the calculated Beta.

## Acknowledgments

yfinance for providing easy access to financial data.

statsmodels for linear regression modeling.

Matplotlib and Seaborn for data visualization.



