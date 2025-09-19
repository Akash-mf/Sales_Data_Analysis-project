# Sales Data Analysis Project

## Overview

This project demonstrates a complete **Sales Data Analysis** workflow using **Excel, SQL, Power BI, and storytelling**. It helps visualize sales performance, identify trends, and generate actionable insights for decision-making.

---

## Project Objectives

* Analyze sales data to track business performance.
* Build interactive dashboards with KPIs.
* Generate insights like:

  * *"Sales dropped in Q3 due to reduced marketing spend in APAC region."*
* Practice ETL concepts using SQL and Excel.
* Present data-driven stories using Power BI.

---

## Dataset

The project uses a `sales_dataset.csv` file containing the following columns:

| Column Name   | Description                                         |
| ------------- | --------------------------------------------------- |
| OrderID       | Unique ID for each order                            |
| OrderDate     | Date when the order was placed                      |
| ShipDate      | Date when the order was shipped                     |
| CustomerID    | Unique customer identifier                          |
| CustomerName  | Name of the customer                                |
| Region        | Region of sale (APAC, EMEA, Americas)               |
| Country       | Country name                                        |
| State         | State/province name                                 |
| City          | City name                                           |
| Category      | Product category (Electronics, Furniture, Clothing) |
| SubCategory   | Detailed subcategory of the product                 |
| ProductID     | Unique product identifier                           |
| ProductName   | Product name                                        |
| UnitsSold     | Number of units sold                                |
| UnitPrice     | Selling price per unit                              |
| UnitCost      | Cost price per unit                                 |
| Sales         | Total revenue (UnitsSold \* UnitPrice)              |
| Cost          | Total cost (UnitsSold \* UnitCost)                  |
| Profit        | Total profit (Sales - Cost)                         |
| Discount      | Discount percentage given                           |
| SalesChannel  | Online or Offline                                   |
| PromotionFlag | Indicates if a promotion was applied (Y/N)          |

---

## Tools Used

* **Excel** - Data cleaning and quick analysis.
* **SQL** - Data querying and transformations.
* **Power BI** - Interactive dashboard and storytelling.
* **Python (Optional)** - For generating and pre-processing sample data.

---

## Steps to Follow

### 1. Data Preparation

* Download the `sales_dataset.csv` file.
* Clean the data in Excel or Python:

  * Remove duplicates.
  * Handle missing values.
  * Validate date formats.

### 2. SQL Database Setup

* Create a database named `SalesDB`.
* Import `sales_dataset.csv` into a `Sales` table.
* Run sample SQL queries:

```sql
-- Total Sales by Region
SELECT Region, SUM(Sales) AS TotalSales
FROM Sales
GROUP BY Region
ORDER BY TotalSales DESC;

-- Average Order Value (AOV)
SELECT AVG(Sales) AS AvgOrderValue FROM Sales;
```

### 3. Power BI Dashboard

**Key KPIs to include:**

* Total Sales
* Average Order Value (AOV)
* Total Profit
* Profit Margin

**Visualizations:**

* Sales by Region (Map)
* Sales by Category (Bar Chart)
* Monthly Sales Trend (Line Chart)
* Filter options for:

  * Region
  * Category
  * Time Period

### 4. Insights & Storytelling

Add narrative insights like:

* *"Sales peaked in Q2 due to seasonal promotions."*
* *"EMEA region showed a 15% increase compared to last year."*
* *"Online sales contributed 60% of total revenue."*

---

## Folder Structure

```
Sales-Data-Analysis-Project/
│
├── data/
│   └── sales_dataset.csv
│
├── sql/
│   └── sales_queries.sql
│
├── powerbi/
│   └── SalesDashboard.pbix
│
└── README.md
```

---

## Final Deliverables

* **Cleaned dataset** ready for analysis.
* **SQL scripts** for ETL and querying.
* **Interactive Power BI dashboard**.
* **Business insights report**.

---

## Next Steps

* Add predictive modeling using Python.
* Build automated data pipelines.
* Publish dashboard online using Power BI Service.
