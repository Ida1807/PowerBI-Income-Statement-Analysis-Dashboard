#  Power BI Income Statement Analysis Dashboard
#  Project Overview
This project presents a financial analysis dashboard built in Power BI for Global Trading Group, a multinational trading and distribution company. The dashboard evaluates company performance using a structured Income Statement (P&L) built directly in Power BI using matrix visuals and DAX measures to replicate a real-world financial reporting format. A star schema data model was implemented, with a central General Ledger fact table containing transactional data and supporting dimension tables such as Date, Chart of Accounts, and Territory. This structure enables efficient filtering, scalable analysis, and dynamic insights into revenue, costs, and profitability.

#  Key Business Metrics
The dashboard tracks core financial performance indicators, including:
- Sales Revenue
- Gross Profit
- EBITDA (Earnings Before Interest, Taxes, Depreciation, and Amortisation)
- Net Profit
- Profitability Margins (Gross, EBITDA, Net)
- Cost-to-Sales Ratios
These metrics provide insight into both top-line growth and operational efficiency.

#  Multi-Dimensional Analysis
Users can analyse performance across:
- 📅 Time (Year, Quarter, Month)
- 🌍 Country (e.g., USA, UK, Germany, etc.)
This enables:
Cross-country comparison, trend analysis over multiple years and identification of high-performing countries

#  DAX Measures & Calculations
DAX was used extensively to create dynamic and reusable measures.
🔹 Some Core Measures Include
- TotalSales = CALCULATE([TotalTransactions],'Dim_Chart of Accounts'[SubClass] = "Sales")
- Cost of Sales = CALCULATE([TotalTransactions],'Dim_Chart of Accounts'[SubClass] = "Cost of Sales")
- Gross Profit = CALCULATE([TotalTransactions], 'Dim_Chart of Accounts'[Class] = "Trading account")
- Net Profit = CALCULATE([TotalTransactions],'Dim_Chart of Accounts'[Report]= "Profit and Loss")

🔹Profitability Ratios
- GrossProfit Margin = [Gross Profit]/[TotalSales]
- NetProfit Margin = [Net Profit]/[TotalSales]
- 
🔹Time Intelligence Measures
- SalesYTD = TOTALYTD([TotalSales],Dim_Calendar[Date])
- SalesQTD = TOTALQTD([TotalSales],Dim_Calendar[Date])
- SalesPYTD = CALCULATE([TotalSales],SAMEPERIODLASTYEAR(Dim_Calendar[Date]))
- SalesMTD = TOTALMTD([TotalSales], Dim_Calendar[Date])
- YTDGrowth % = DIVIDE([SalesYTD]-[SalesPYTD], [SalesPYTD])
These measures enable dynamic comparison between current and previous periods, supporting trend analysis and performance evaluation.

# Dashboard Features
The report consists of multiple interactive pages:
- Executive Summary – High-level KPIs and insights
- Sales Analysis – Revenue trends over time
- P&L Statement – Structured income statement built in Power BI
- Cross-Country Analysis – Regional comparison
- Performance Analysis – Ratios, YTD vs PYTD, cost analysis

# Visualisation Techniques
- KPI Cards
- Line Charts (trend analysis)
- Bar Charts (comparisons)
- Matrix Visual (Income Statement)
- Slicers (Country, Year filters)

# Tools & Technologies
- Power BI
- DAX (Data Analysis Expressions)
- Power Query (Data Transformation)
- Data Modelling (Star Schema)
- Financial Analysis (Income Statement & KPI Development)
  
