# Maven Market Sales Analysis (1998)

An interactive Power BI dashboard built using Power BI & Excel to analyze 1998 sales data for Maven Market, a multinational grocery retailer operating across the U.S., Canada, and Mexico.

---

## 💡 Key Analytics Features
- Identified and ranked top 30 product brands by total transactions  
- Built clean data models with proper relationships  
- Created custom DAX measures and calculated columns  
- KPI cards comparing monthly profit & returns (Current vs Previous Month)  
- Regional sales analysis using map visuals  
- Revenue vs target tracking using gauge charts  
- Report-level filter applied for 1998 data only  
- Interactive slicers, drill-throughs, and bookmarks for storytelling  

---

## 🧩 Data Model Overview
Star schema design used for optimized analysis:

Fact Tables:
- Sales
- Returns

Dimension Tables:
- Products
- Customers
- Stores
- Calendar

Relationships:
- Sales[ProductID] → Products[ProductID]
- Sales[StoreID] → Stores[StoreID]
- Sales[Date] → Calendar[Date]
- Returns linked to Sales via Transaction ID

---

## 📐 Key DAX Measures
```DAX
Total Sales :=
SUM ( Sales[Sales_Amount] )

Total Profit :=
SUM ( Sales[Profit] )

Profit Margin % :=
DIVIDE ( [Total Profit], [Total Sales] )

Monthly Profit Change :=
[Current Month Profit] - [Previous Month Profit]

Return Rate % :=
DIVIDE ( [Total Returns], [Total Transactions] )

---

## 📌 Business Insights:
1. Portland crossed 1,000 sales in December — strong year-end performance
2. High Top product returns in Mexico doubled (4 → 8), with a 1.2% return rate
3. Strongest overall profit margin (63.55%) by Plato product in 1998

---

## 🔧 Tools Used:
Power BI (DAX, KPI Cards, Report Filters, Slicers, Bookmarks, Drill-throughs), Excel(Data cleaning)
