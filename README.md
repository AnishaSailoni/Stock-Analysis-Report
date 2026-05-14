 📈 Stock Market Intelligence Dashboard

An interactive Power BI dashboard designed to analyze stock market performance by tracking close price trends, moving averages, volatility, returns, and investment recommendations across multiple companies.


1. Short Description / Purpose

The Stock Market Intelligence Dashboard is a dynamic Power BI report built to analyze and compare stock performance of major companies.
It helps identify price trends, 30-day returns, moving average signals, and volatility risk to support better investment decisions.


2. Tech Stack

The dashboard was built using the following tools and technologies:

* 📊 Power BI Desktop – Used for designing and developing the complete interactive dashboard report.
* 📂 Power Query – Used for data cleaning, transformation, and formatting the stock dataset.
* 🧠 DAX (Data Analysis Expressions) – Used to create calculated measures such as Moving Averages (MA20, MA50), Volatility, 30-Day Return, and Recommendations.
* 🐍 Python – Used to generate the dataset using live stock data from Yahoo Finance.
* 🌐 yFinance Library – Used for extracting 1-year daily stock market data.
* 📝 Data Modeling – Structured the dataset for proper filtering, slicers, and analysis.
* 📁 File Format – `.pbix` (Power BI report file), `.csv` (dataset), and `.png` (dashboard screenshots).


3. Data Source

Dataset Name: Stock Market Dataset (Custom Generated)
Source Type: Yahoo Finance (Live Data Extracted via Python)

This dataset was not downloaded from any ready-made dataset source.
It was created manually using Python by extracting stock market data using the yFinance API.

The dataset contains daily stock market information including:

* Date
* Open Price
* High Price
* Low Price
* Close Price
* Adjusted Close
* Volume
* Stock Symbol


📌 Dataset Creation Code (Python)

python
import yfinance as yf
import pandas as pd

stocks = ["AAPL", "MSFT", "TSLA", "GOOG", "AMZN"]

data = yf.download(stocks, period="1y", interval="1d")
data = data.reset_index()

data.to_csv("stock_data.csv", index=False)


 4. Features / Highlights

 ✅ Business Problem

Investors and analysts deal with large amounts of stock market data daily.
Without visualization, it becomes difficult to answer important questions like:

* Which stock is giving the best return in the last 30 days?
* Which company has the highest volatility (risk)?
* Is the stock price following a bullish or bearish trend?
* How do multiple companies compare in terms of risk vs return?
* Which stock is recommended for investment based on analysis?


🎯 Goal of the Dashboard

The goal of this dashboard is to provide an interactive platform that helps stakeholders:

* Track stock performance over time
* Identify strong-performing stocks based on return
* Analyze volatility risk for each stock
* Compare companies using moving average indicators
* Generate investment signals such as BUY and STRONG BUY


5. Walkthrough of Key Dashboard Pages & Visuals

📌 Page 1: Stock Market Intelligence Dashboard (Overview)

Key Elements:

* KPI Cards

  * Close Price
  * Volatility
  * 30-Day Return
  * MA50

* Line Chart (MA20, Close Price, MA50 by Date)

  * Shows stock price movement along with moving average signals.

* Bar Chart (30D Return by Stock)

  * Helps identify the best-performing stock in the last 30 days.

* Slicers

  * Company selection
  * Date range filter

* Table

  * Displays Close Price, Return, Volatility and Recommendation for each stock.


📌 Page 2: Trend Analysis Dashboard

Key Elements:

* Trend Insight Card

  * Shows overall market trend like Bullish / Bearish

* Line Chart (Sum of Close by Date and Stock)

  * Displays stock price trend comparison across all companies.

* Bar Chart (Price vs MA by Date)

  * Helps identify whether the price is above or below the moving average.


📌 Page 3: Risk & Volatility Analysis

Key Elements:

* Scatter Plot (30D Return vs Volatility)

  * Shows the relationship between risk and return.
  * Helps identify which stock provides good return at lower risk.

* Bar Chart (Volatility by Stock)

  * Compares volatility levels of all companies.

* Slicers

  * Company selection
  * Date range filter

---

📌 Page 4: Company Performance Comparison

Key Elements:

* Line Chart (Close Price by Date and Stock)

  * Compares stock performance over time.

* Table (Company Metrics Summary)

  * Shows Close Price, Return, Volatility, and Investment Recommendation.

* Slicers

  * Company filter
  * Date filter


6. Business Impact & Insights

📌 Key Insights from the Dashboard:

* Stocks with higher volatility show higher risk but may provide higher returns.
* Moving averages (MA20 & MA50) help identify bullish/bearish signals.
* Comparison charts make it easy to identify the strongest-performing company.
* Risk vs Return scatter plot helps investors choose the best balance between safety and growth.

Business Benefits:

* 📈 Investment Strategy: Helps identify stocks with strong performance signals.
* ⚠️ Risk Monitoring: Volatility analysis supports better risk management.
* 📊 Trend Tracking: Helps understand long-term and short-term price movements.
* 🔍 Company Comparison: Supports decision-making by comparing multiple companies in one dashboard.


7. Screenshots / Demos

📌 Dashboard Preview


* Stock Market Intelligence Dashboard (Overview)
* Trend Analysis Dashboard
* Risk & Volatility Analysis
* Company Performance Comparison


8. Author

Author Name: Anisha Sailoni
Tool Used: Microsoft Power BI
Dataset Generated Using: Python (yFinance)


 9. How to Use the Dashboard


1. Download the `.pbix` file from this repository.
2. Open it using Power BI Desktop.
3. Use the Company slicer to filter stock-wise insights.
4. Use the Date slicer to analyze performance within a selected time range.
5. Observe KPI cards, charts, and tables for return, volatility, and recommendations.


If you want, I can also prepare a **perfect GitHub folder structure** for this project (dataset + screenshots + pbix + python file).
