# 📊 Product Sales Dashboard - Power BI

This dashboard provides a detailed analysis of product sales performance using data sourced from two CSV files: `Orders.csv` and `Details.csv`. Built using Power BI, the dashboard allows users to explore sales, profit, quantity, and customer behavior through interactive visuals.

---

## 📁 Data Model Overview

The data model consists of **two primary tables**:

### 🔹 1. `Details` Table
Contains detailed information about each product in the order.

| Column Name    | Description                                |
|----------------|--------------------------------------------|
| `Order ID`     | Unique identifier for the order (used as FK)|
| `Amount`       | Total sales amount for the product          |
| `Profit`       | Profit made on that item                    |
| `Quantity`     | Number of units sold                        |
| `AOV`          | Average Order Value                         |
| `Category`     | Product category (e.g., Furniture, Electronics) |
| `Sub-Category` | More specific classification (e.g., Chairs) |
| `PaymentMode`  | Payment method used (e.g., COD, UPI)        |

---

### 🔹 2. `Orders` Table
Contains higher-level information related to customer and location for each order.

| Column Name     | Description                                  |
|------------------|----------------------------------------------|
| `Order ID`       | Unique order identifier (Primary Key)        |
| `CustomerName`   | Name of the customer                         |
| `City`           | City where the order was placed              |
| `State`          | State of the customer                        |
| `Order Date`     | Date when the order was placed               |

> Includes a **Date Hierarchy**: Year, Quarter, Month, Day for time-based filtering and grouping.

---

## 🔗 Relationship Between Tables

- `Orders[Order ID]` ⟶ `Details[Order ID]` (One-to-Many)

This relationship allows filtering order-level data using product-level details and vice versa.

---

## 🎯 Dashboard Objectives

- Track KPIs like Sales, Quantity, Profit, AOV
- Analyze profit trends across months
- Understand customer behavior by state and city
- Identify top products and sub-categories
- Segment payment method usage
- Enable filtering by Quarter and other dimensions

---

## 📌 Key KPIs

| KPI               | Description                                  | Value        |
|-------------------|----------------------------------------------|--------------|
| **Sum of Amount** | Total revenue across all sales               | ₹438K        |
| **Sum of Quantity**| Total units sold                            | 5615 units   |
| **Sum of Profit** | Overall profit from product sales            | ₹37K         |
| **Sum of AOV**    | Average order value across transactions      | ₹121K        |

---

## 📊 Visual Components

- **Profit by Month** (Bar Chart)
- **Sales by State** (Horizontal Bar)
- **Sales by Customer Name** (Bar Chart)
- **Profit by Sub-Category** (Bar Chart)
- **Quantity by Category** (Donut Chart)
- **Quantity by Payment Mode** (Donut Chart)

---

## 🛠 Tools Used

- Power BI Desktop
- CSV Data Sources
- DAX Calculations for KPIs
- Date Hierarchy for time-based analytics

---
## 📈 Example Insights

- COD is the most used payment method (44%)
- Clothing accounts for 63% of product quantity sold
- Printers bring the highest profit among sub-categories
- May and December have negative profit trends
