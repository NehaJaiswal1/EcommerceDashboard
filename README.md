# 📊 E-commerce Sales Dashboard (Power BI)

This project is an interactive **E-commerce Sales Dashboard** built using **Power BI**. It provides insights into sales trends, profitability, and customer behavior to support data-driven decisions in an online retail business environment.

---

## 🔍 Project Overview

The dashboard helps visualize:

* Total sales, orders, and profit
* Monthly trends in revenue
* Product-level performance by category and sub-category
* Regional sales and profit comparison
* Top-selling products

---

## 🛠️ Tools & Technologies

* **Power BI** for data visualization
* **DAX (Data Analysis Expressions)** for custom calculations
* **Power Query** for data cleaning and transformation

---

## 📈 Key Features

* Summary KPIs (Sales, Profit, Orders)
* Interactive filters (Region, Category, Customer Segment)
* Time series visualizations
* Product-wise sales leaderboard
* Dynamic slicers for drill-down

---

## 🛂 Data Processing Steps

* Cleaned and removed duplicates/nulls
* Standardized formats and categories
* Built star schema using relationships
* Created calculated columns and measures with DAX

---

## 🗁 File Structure

* `E-commerceSalesDashboard.pbix` — Main Power BI report
* `README.md` — Project documentation

---

## 📌 Use Cases

* Sales and profit trend analysis
* Product strategy and inventory decisions
* Regional marketing insights
* Executive business reporting

---

## 🔶 DAX Measures & Logic

This dashboard includes several custom DAX measures:

### ✅ Total Sales

```dax
Total Sales = SUM(Orders[Sales])
```

> Calculates total revenue from all orders.

### ✅ Total Profit

```dax
Total Profit = SUM(Orders[Profit])
```

> Total earnings after cost of goods sold.

### ✅ Total Orders

```dax
Total Orders = COUNTROWS(Orders)
```

> Number of orders placed.

### ✅ Average Order Value (AOV)

```dax
Average Order Value = [Total Sales] / [Total Orders]
```

> Average revenue per order.

### ✅ Profit Margin %

```dax
Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)
```

> Percentage of revenue that is profit.

### ✅ Sales Trend (Month-to-Date)

```dax
Sales Trend = CALCULATE([Total Sales], DATESMTD('Calendar'[Date]))
```

> Month-to-date trend for sales.

### ✅ Product Rank by Sales

```dax
Product Rank = RANKX(ALL('Products'[Product Name]), [Total Sales], , DESC)
```

> Ranks products based on total sales.

### ✅ YOY Sales Growth

```dax
YOY Sales Growth =
VAR CurrentYear = [Total Sales]
VAR LastYear = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Calendar'[Date]))
RETURN DIVIDE(CurrentYear - LastYear, LastYear)
```

> Year-over-year growth comparison.

---

## 🤝 About Me

I’m a data analyst with a background in software development, now focused on creating business insights using Power BI, SQL, Python, and Excel.

---

## 📩 Demo Link

[Have ideas or feedback? Open an issue or reach out—I'd love to connect!](https://github.com/NehaJaiswal1/EcommerceDashboard/blob/main/Ecommerce-Dashbord.png)

