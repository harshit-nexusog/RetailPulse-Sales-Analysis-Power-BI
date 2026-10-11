# 📊 RetailPulse Sales Analysis | Power BI

## 📌 Project Overview

RetailPulse Sales Analysis is a Business Intelligence and Data Analytics project developed using Microsoft Power BI. The project focuses on analyzing retail sales data, creating interactive dashboards, and generating meaningful business insights through data visualization and DAX calculations.

This project covers Power BI Practicals 7, 8, and 9, including data transformation, data modeling, dashboard development, and advanced time intelligence.

## 🎯 Project Objectives

* Import and transform retail sales data using Power Query.
* Clean and prepare data for analysis.
* Create relationships between Sales, Product, and Store tables.
* Develop DAX measures for sales performance analysis.
* Build interactive dashboards and visualizations.
* Analyze monthly sales trends and year-over-year growth.
* Calculate year-to-date sales and regional sales contributions.

## 🛠️ Tools & Technologies

* **Microsoft Power BI Desktop** — Data visualization and dashboard development
* **Power Query** — Data cleaning and transformation
* **DAX (Data Analysis Expressions)** — Calculations and business metrics
* **Microsoft Excel** — Dataset storage and data source

## 📂 Dataset Description

The project uses a synthetic RetailPulse retail sales dataset containing three tables:

| Table   | Description                                                                   |
| ------- | ----------------------------------------------------------------------------- |
| Sales   | Order IDs, sales dates, product IDs, store IDs, quantities, and sales amounts |
| Product | Product IDs, product names, categories, and unit prices                       |
| Store   | Store IDs, store names, regions, and cities                                   |

**Dataset Statistics:**

* 1,800 sales records
* 12 products
* 8 stores
* 4 regions: North, South, East, and West
* Sales data covering January 2024 to December 2025

## 📚 Practicals Covered

### Practical 7: Data Import & Transformation

* Imported Excel data into Power BI.
* Used Power Query Editor to prepare the dataset.
* Set appropriate data types.
* Checked for blank and duplicate rows.
* Created a conditional column named `Sale Size`.
* Classified sales of $1,000 or more as Large and other sales as Standard.

### Practical 8: Data Modeling, DAX & Dashboard

* Created relationships between Sales, Product, and Store tables.
* Developed DAX measures for Total Sales, Total Quantity, and Average Order Value.
* Created a calculated column for Sales per Unit.
* Built interactive cards, bar charts, and monthly sales trend charts.
* Added a Region slicer for interactive filtering.
* Published the report to a Power BI workspace.

### Practical 9: Time Intelligence & Advanced DAX

* Created and configured a Date table.
* Developed Year, Month Number, and Month Name columns.
* Calculated Year-to-Date (YTD) sales.
* Compared current sales with the previous year's sales.
* Calculated Year-over-Year (YoY) growth.
* Analyzed regional contributions using `CALCULATE` and `ALL`.
* Used Performance Analyzer to examine visual performance.

## 📈 Key Performance Indicators

| Metric                      |      Result |
| --------------------------- | ----------: |
| Total Sales                 | $812,474.31 |
| Total Quantity Sold         |       5,414 |
| Average Order Value         |     $451.37 |
| Highest-Selling Category    | Electronics |
| Highest-Contributing Region |       South |
| Electronics Sales           | $524,579.39 |

## 📊 Visualizations Created

The project includes a variety of Power BI visualizations, such as:

* Sales by Product Category
* Sales by Region
* Monthly Sales Trends
* 2024 vs. 2025 Sales Comparison
* Sales Share by Category and Region
* Stacked and Clustered Column Charts
* Donut and Pie Charts
* Top 10 Products by Sales
* Sales by Store
* Region vs. Category Sales Matrix
* Quantity vs. Sales Analysis
* Order Amount Distribution
* Large vs. Standard Sales
* Sales by Day and Quarter
* Sales YTD Analysis
* YoY Growth Analysis
* Waterfall Chart
* KPI Gauge
* Region Share Percentage

## 🧮 Important DAX Measures

### 1. Total Sales

```DAX
Total Sales = SUM(Sales[Sales Amount])
```

### 2. Total Quantity

```DAX
Total Quantity = SUM(Sales[Quantity])
```

### 3. Average Order Value

```DAX
Average Order Value =
DIVIDE(
    [Total Sales],
    DISTINCTCOUNT(Sales[OrderID])
)
```

### 4. Sales Year-to-Date

```DAX
Sales YTD =
TOTALYTD(
    [Total Sales],
    'Date'[Date]
)
```

### 5. Sales Last Year

```DAX
Sales LY =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR('Date'[Date])
)
```

### 6. Year-over-Year Growth

```DAX
YoY Growth % =
VAR Curr = [Total Sales]
VAR Prev = [Sales LY]
RETURN
    DIVIDE(Curr - Prev, Prev)
```

### 7. Region Share Percentage

```DAX
Region Share % =
DIVIDE(
    [Total Sales],
    CALCULATE(
        [Total Sales],
        ALL(Store[Region])
    )
)
```

## 💡 Key Business Insights

* Electronics is the largest sales category, contributing approximately 64.6% of total sales.
* South is the highest-contributing region, accounting for approximately 28.4% of total sales.
* East contributes approximately 26.8%, followed by North at 26.7%.
* West contributes approximately 18.1% of total sales.
* Year-over-year analysis highlights monthly fluctuations in sales performance.
* The Region slicer enables users to explore sales performance across different regions.

## 📁 Project Files

The repository may contain the following files:

* `RetailPulse_Sales.xlsx` — Source dataset
* `RetailPulse_Analysis.pbix` — Power BI project file
* `RetailPulse_All_Graphs.pdf` — Collection of Power BI visualizations
* `PowerBI_Practical_7_to_9_Harshit.pdf` — Practical documentation

*Upload only the files you intend to share. The Power BI `.pbix` file should be included if you have saved it and want others to explore the report.*

## 🚀 Learning Outcomes

Through this project, I gained practical experience in:

* Data cleaning and transformation
* Data modeling and table relationships
* DAX measures and calculated columns
* Interactive dashboard creation
* Time intelligence calculations
* Sales performance analysis
* Business insights and data storytelling

## 👨‍💻 Author

**Harshit Kumar Srivastava**

Business Analytics | Power BI | Data Analytics

---

⭐ If you find this project useful, consider giving the repository a star!
