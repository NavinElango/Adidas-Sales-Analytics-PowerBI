# 📊 Adidas US Sales Analytics — Power BI Dashboard

> **Interactive Power BI dashboard analyzing Adidas US sales data (2020–2021) across regions, retailers, products, and sales channels — built with DAX, Power Query, and advanced data visualizations.**

---

## 🔗 Portfolio Links
- 📄 **[View Full Dashboard (PDF)](./Nav.pdf)**
- 👤 **[LinkedIn](https://www.linkedin.com/in/navin-elango)**
- 🎓 **[Student Spending Analytics Project](https://github.com/NavinElango/Student-Spending-Analytics-PowerBI)**

---

## 📌 Project Overview

This project analyzes Adidas US sales data from **2020 and 2021**, sourced from Kaggle. The goal was to uncover meaningful insights about regional performance, retailer effectiveness, product category trends, and pricing strategy — and communicate those findings through clear, interactive Power BI dashboards.

The project demonstrates end-to-end Power BI development including data preparation in Power Query, calculated column creation using DAX, advanced visualization design, and data storytelling with written insights for each business question.

---

## 📂 Dataset

| Field | Description |
|-------|-------------|
| Sales ID | Unique numeric identifier (Index column added) |
| Retailer | Name of the retailer (West Gear, Foot Locker, Sports Direct, Kohl's, Walmart, Amazon) |
| Retailer ID | Unique identifier for each retailer |
| Invoice Date | Date of the sales transaction |
| Region | Geographic region (West, Northeast, South, Southeast, Midwest) |
| State | State where the transaction occurred |
| City | City where the transaction occurred |
| Product | Description of the product sold |
| Price per Unit | Cost of one unit of the product |
| Units Sold | Number of units sold during the transaction |
| Operating Margin | Profit margin (Operating Profit / Total Sales) |
| Sales Method | In-store, Online, or Outlet |
| Operating Profit | Calculated column (Operating Margin × Total Sales) |
| Product Category | Men or Women — classified using DAX SWITCH function |
| Total Sales | Calculated column (Units Sold × Price Per Unit) |

**Dataset source:** Kaggle | **Period:** 2020–2021 | **Records:** US retail transactions

---

## 🛠️ Data Preparation (Power Query)

**Step 1 — Removed Non-Data Rows & Promoted Headers**
Removed irrelevant rows that loaded from the Excel spreadsheet and promoted the first row to become column headers.

**Step 2 — Removed Redundant Columns & Added Index**
Removed the pre-calculated Total Sales column (to recalculate via DAX) and added an Index column renamed as "Sales ID" to serve as the primary key.

**Step 3 — Changed Data Types**
Corrected data types for all fields — for example, changed Invoice Date from text format (ABC123) to proper DATE type to enable time-intelligence calculations.

**Step 4 — Standardized Values**
Cleaned and standardized field values to ensure consistency across all reporting outputs.

---

## 📐 DAX Measures & Calculated Columns

Key calculations built using DAX:

| Calculation | Type | Formula Logic |
|-------------|------|--------------|
| Total Sales | Calculated Column | Units Sold × Price Per Unit |
| Operating Profit | Calculated Column | Operating Margin × Total Sales |
| Product Category | Calculated Column | SWITCH function classifying Men/Women products |
| Highest Region Sale | Measure | MAX of Total Sales by Region |
| Highest Retailer Sale | Measure | MAX of Total Sales by Retailer |
| Year-over-Year Comparison | Measure | Time-intelligence comparison 2020 vs 2021 |

---

## ❓ Business Questions Answered (5 Questions)

### Question 1 — Regional Sales Division
**"What is the division of sales between different regions across years?"**
- Visualization type: Nominal Comparison + Part to Whole
- Visuals: Clustered Bar Chart, Donut Chart, Map Visual
- **Key Insight:** The West region generates 30.32% of total sales ($36.44M), with California alone contributing over $8M in revenue — driven by large population, high per capita income, and fashion-conscious culture.

---

### Question 2 — Retailer Performance by Region
**"What is the total sales compared by different retailer and then drilled by region?"**
- Visualization type: Nominal Comparison + Part to Whole
- Visuals: Bar Chart, Drill Down Donut Pro (custom visual)
- **Key Insight:** West Gear accounts for nearly 27% of Adidas' total revenue ($32.4M), with 58% of its contribution originating from the West region — underscoring strong regional brand alignment.

---

### Question 3 — Year-over-Year Sales Comparison
**"Did Adidas surpass the total sales of year 2020 in year 2021?"**
- Visualization type: Deviation + Time Series
- Visuals: Gauge Chart, Line/Bar Combo Chart, Waterfall Chart
- **Key Insight:** Sales in 2021 saw a remarkable 400% surge compared to 2020 ($24M → $96M), driven by post-pandemic recovery, return to fitness activities, and easing of lockdown restrictions.

---

### Question 4 — Men vs Women Product Performance
**"What is the total sales and units sold comparison between men and women products?"**
- Visualization type: Nominal Comparison + Part to Whole
- Visuals: Horizontal Bar Charts, Donut Chart
- **Key Insight:** Men's products account for 53.91% of total sales ($64.78M) versus 46.09% for Women's ($55.39M) — an 8% gap suggesting near gender parity, with opportunity to grow Women's segment through targeted marketing.

---

### Question 5 — Price per Unit Correlation Analysis
**"How do total sales, units sold, and number of sales transactions correlate with price per unit?"**
- Visualization type: Correlation
- Visuals: Three Scatter Plot Charts
- **Key Insight:** A notable concentration of data points falls within the $40–$60 price range — suggesting this is the optimal pricing sweet spot for Adidas products. High-priced and low-priced items contribute relatively less, driven by perceived quality and value-for-money considerations.

---

## 📈 Visualizations Used

- Clustered Bar Charts
- Donut Charts
- Drill Down Donut Pro (Custom Visual)
- Scatter Plot / Correlation Charts
- Gauge Chart
- Map Visual (Bing Maps)
- KPI Cards
- Line and Bar Combo Chart
- Cross-filtering Slicers (Year, Region, Sales Method)

---

## 💡 Key Findings Summary

| Metric | Value |
|--------|-------|
| Total Sales (2020–2021) | $120,166,650 |
| Highest Region | West — $36.44M (30.32%) |
| Top Retailer | West Gear — $32.4M (26.97%) |
| YoY Growth | 400% surge (2020→2021) |
| Top Sales Method | In-store |
| Men vs Women Split | 53.91% vs 46.09% |
| Optimal Price Range | $40–$60 per unit |

---

## 🧰 Tools & Technologies

| Tool | Usage |
|------|-------|
| Power BI Desktop | Dashboard development |
| Power Query (M) | Data cleaning and transformation |
| DAX | Calculated columns, measures, and KPIs |
| Drill Down Donut Pro | Custom visualization for drill-through analysis |
| Kaggle | Data source |
| GitHub | Portfolio hosting |

---

## 👤 About Me

**Navin Elango** — Power BI Developer and Data Analyst based in Dallas, TX

- 🎓 MS in Business Analytics, University of Delaware (GPA 3.8)
- 🏆 Microsoft Certified: Azure Fundamentals (AZ-900) — July 2026
- 💼 2.5+ years of full-time BI and analytics experience
- 🔧 Skills: Power BI, DAX, Power Query, SQL, Python, Tableau, Excel
- 🌐 [LinkedIn](https://www.linkedin.com/in/navin-elango)
- 📧 msnavin2000@gmail.com
- 📍 Dallas, TX | Authorized to work in the U.S. (OPT) — No sponsorship required

---

*Built with ❤️ using Power BI Desktop | Data source: Kaggle*
