# Project Overview
This project presents a financial analysis dashboard developed in Power BI to evaluate company performance using a structured Income statement.
The data model was designed using a star schema, consisting of a central fact table which is the Chart of Accounts containing transactional sales data and multiple dimension tables (e.g., date, general ledger, and territory attributes such as country) to enable efficient filtering and analysis.

#📈 Key Metrics
The dashboard includes key financial metrics such as:
Sales Revenue
Gross Profit
EBITDA (Earnings Before Interest, Taxes, Depreciation, and Amortisation)
Net Profit
These metrics provide a comprehensive view of profitability and cost structure.

# 🌍 Multi-Country Analysis
Performance is analysed across multiple countries, enabling:
Cross-country comparison of sales
Profitability analysis
Cost efficiency evaluation

# 🧮 DAX Measures & Calculations
DAX (Data Analysis Expressions) was used extensively to create dynamic measures and KPIs, including:
Total Sales and Average Price calculations
Profitability metrics (Gross Profit, Net Profit, EBITDA)
Ratio analysis (e.g., profit margins, cost-to-sales ratios)
Custom measures using CALCULATE, DIVIDE, and aggregation functions
These measures enable flexible, real-time analysis across different dimensions such as time, region, and product.

# ⏱ Time Intelligence (DAX)
Advanced time intelligence functions in DAX were used to analyse performance over time, including:
Year-to-Date (YTD) – cumulative performance from the start of the year
Month-to-Date (MTD) – performance within the current month
Previous Year-to-Date (PYTD) – same period comparison with the previous year
Year-over-Year (YoY) Growth – percentage change in performance

These calculations were implemented using functions such as:
TOTALYTD()
TOTALMTD()
SAMEPERIODLASTYEAR()
CALCULATE()
This allows users to compare current performance against previous periods and identify trends across multiple years.

# 📊 Visualisation & Insights
Interactive visuals include:
KPI cards
Line charts for trend analysis

Breakdown visuals by country, product, and time
These enable users to:
Track performance trends
Compare results across regions and time periods
Support data-driven decision-making

# 🛠 Tools & Skills Used
Power BI
DAX (Data Analysis Expressions)
Data Modelling (Star Schema)
Power Query (Data Transformation)
Financial Analysis (Income Statement and KPI development)
