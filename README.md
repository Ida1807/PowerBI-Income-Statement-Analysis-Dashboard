# 📊 Power BI Income Statement Analysis Dashboard
# 📌 Project Overview
This project presents a financial analysis dashboard developed in Power BI to evaluate company performance using a structured Income Statement (Profit and Loss – P&L) built directly within Power BI. The income statement was designed using Power BI visuals (matrix and measures) to replicate a real-world financial reporting format, allowing dynamic analysis of revenue, costs, and profitability. A star schema data model was implemented, consisting of a central fact table ( General Ledger which contains transactions) and supporting dimension tables (Date, Chart of Accounts, Territory), ensuring efficient filtering and scalable analysis.

# 📈 Key Business Metrics
The dashboard tracks core financial performance indicators, including:
- Sales Revenue
- Gross Profit
- EBITDA (Earnings Before Interest, Taxes, Depreciation, and Amortisation)
- Net Profit
- Profitability Margins (Gross, EBITDA, Net)
- Cost-to-Sales Ratios
These metrics provide insight into both top-line growth and operational efficiency.

# 🌍 Multi-Dimensional Analysis
Users can analyse performance across:
- 📅 Time (Year, Quarter, Month)
- 🌍 Country (e.g., USA, UK, Germany, etc.)
This enables:
Cross-country comparison, trend analysis over multiple years and identification of high-performing countries

# 🧮 DAX Measures & Calculations
DAX was used extensively to create dynamic and reusable measures.
🔹 Core Measures
- SalesTotal = CALCULATE([Total_FTP],'Dim_Chart of Accounts'[SubClass] = "Sales")
- 
