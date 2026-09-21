# Retail-Sales

## 📌 Project Overview

This project performs an end-to-end analysis of retail sales data using **Python, SQL Server, and Power BI**.
The objective is to understand **sales performance, profitability, customer behavior, regional trends, discount impact, product performance, and shipping efficiency** and convert the findings into actionable business insights.The project follows a complete analytics workflow:

**Raw Data → Data Cleaning → Exploratory Data Analysis → SQL Business Analysis → Power BI Dashboard → Business Insights**

---

## 🎯 Business Objectives

The analysis focuses on answering key business questions such as:

* Which product categories generate the highest sales and profit?
* Which sub-categories and products are causing losses?
* Which regions perform best in terms of sales and profitability?
* How do sales change over time?
* Which products and customers contribute the most revenue?
* Does higher discounting negatively affect profitability?
* What percentage of orders result in a loss?
* How does shipping mode affect order volume and profitability?
* What are the month-over-month sales trends?

---

## 🗂️ Dataset

The project uses the **Superstore retail sales dataset**, containing order-level transaction information.

### Key Data Fields

| Field          | Description                     |
| -------------- | ------------------------------- |
| `Order Date`   | Date when the order was placed  |
| `Ship Date`    | Date when the order was shipped |
| `Category`     | Product category                |
| `Sub-Category` | Product sub-category            |
| `Product Name` | Name of the product             |
| `Sales`        | Revenue generated               |
| `Profit`       | Profit generated                |
| `Discount`     | Discount applied                |
| `Quantity`     | Quantity sold                   |
| `Region`       | Geographic region               |
| `State`        | Customer/order state            |
| `Segment`      | Customer segment                |
| `Ship Mode`    | Shipping method                 |
| `Customer ID`  | Unique customer identifier      |

---

## 🛠️ Tools & Technologies

### 🐍 Python

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

**Used for:**

* Data cleaning
* Data preprocessing
* Exploratory Data Analysis
* Trend analysis
* Visualization
* Identifying relationships between variables

### 🗄️ SQL Server

Used to perform business-oriented analysis using:

* Aggregations
* `GROUP BY`
* `ORDER BY`
* `CASE WHEN`
* `TOP`
* Common Table Expressions (CTEs)
* Window Functions
* `LAG()`
* Date functions
* Profitability analysis
* Customer and product analysis

### 📊 Power BI

Used to create an interactive business intelligence dashboard with:

* KPI cards
* Sales & profit analysis
* Category analysis
* Regional analysis
* Product performance
* Shipping analysis
* Sales trends
* Interactive slicers and filters

---

## 🔄 Project Workflow

### 1️⃣ Data Preparation

The raw Superstore dataset was loaded and prepared for analysis.

Key activities included:

* Checking missing values
* Validating data types
* Identifying inconsistent records
* Preparing date fields
* Preparing the dataset for SQL and Power BI analysis

---

### 2️⃣ Exploratory Data Analysis — Python

Python was used to explore the dataset and identify important patterns.

The analysis focused on:

* Sales distribution
* Profit distribution
* Category performance
* Regional performance
* Product performance
* Customer behavior
* Discount vs. profit relationship
* Time-based sales trends

Visualizations were created using **Matplotlib and Seaborn**.

---

### 3️⃣ SQL Business Analysis

The cleaned dataset was analyzed using SQL Server to answer business questions.

### Key SQL Analysis

#### 📈 Category Performance

Analyzed total sales and profit across product categories.

#### 📦 Product Performance

Identified:

* Top-selling products
* Products generating the highest losses
* Product-level sales and profit contribution

#### 🌎 Regional Analysis

Compared sales and profitability across different regions.

#### 👥 Customer Analysis

Identified high-value customers based on sales and profit contribution.

#### 💰 Discount & Profit Analysis

Investigated the relationship between discount levels and profitability.

#### 🚚 Shipping Analysis

Calculated average shipping time by shipping mode and compared sales and profit performance.

#### 📅 Time-Series Analysis

Analyzed monthly sales trends and calculated month-over-month growth using the `LAG()` window function.

#### ⚠️ Loss Analysis

Calculated the percentage of orders resulting in negative profit.

---

## 📊 Power BI Dashboard

The Power BI dashboard provides an interactive view of overall retail performance.

### Dashboard Features

* 💰 Sales KPIs
* 📈 Profit performance
* 🛍️ Category & sub-category analysis
* 🌎 Regional performance
* 🚚 Shipping mode analysis
* 📅 Sales trend analysis
* 👥 Customer segment analysis
* 🔎 Interactive filtering

### Available Filters

Users can dynamically filter the dashboard by:

* Region
* State
* Category
* Ship Mode
* Customer Segment

---

## 🔍 Key Business Insights

The analysis revealed several important patterns:

### 💰 Profitability

High sales volume does not always translate into high profitability. Certain categories and sub-categories generate substantial revenue while contributing relatively low or negative profit.

### 🏷️ Discount Impact

Higher discount levels are associated with weaker profitability in several product groups, highlighting the importance of reviewing discount strategies.

### 🌎 Regional Performance

Sales and profit vary considerably across regions, helping identify stronger and weaker geographic markets.

### 📦 Product Performance

A small group of products contributes significantly to overall sales, while certain products consistently generate losses.

### 👥 Customer Segments

Customer segments differ in terms of sales contribution and profitability, providing useful information for customer-focused strategies.

### 🚚 Shipping

Different shipping modes show measurable differences in order volume, shipping time, sales, and profitability.

### 📅 Sales Trends

Monthly analysis reveals changes in sales performance over time and helps identify periods of stronger and weaker demand.

---

## 💡 Business Recommendations

Based on the analysis, businesses can consider:

* Reviewing discount strategies for low-margin products.
* Focusing inventory and promotional efforts on profitable product categories.
* Investigating products that consistently generate losses.
* Identifying high-value customers and developing targeted retention strategies.
* Evaluating regional performance to optimize sales investments.
* Monitoring shipping performance and its impact on customer experience and profitability.
* Tracking monthly sales trends to improve demand planning.

---

## 📑 Project Deliverables

| Deliverable           | Description                                 |
| --------------------- | ------------------------------------------- |
| 🐍 Python Notebook    | Data cleaning & exploratory analysis        |
| 🗄️ SQL Script        | Business-question-driven SQL analysis       |
| 📊 Power BI Dashboard | Interactive business intelligence dashboard |
| 📑 Analysis Report    | Detailed project findings                   |
| 🎤 Presentation       | Stakeholder-oriented project presentation   |
| 🖼️ Dashboard Image   | Project preview                             |

---

## 🧠 Skills Demonstrated

**Data Analytics**

* Data Cleaning
* Exploratory Data Analysis
* Business Analysis
* KPI Analysis
* Trend Analysis
* Profitability Analysis

**Technical Skills**

* Python
* Pandas
* NumPy
* SQL Server
* Advanced SQL
* Power BI
* Data Visualization

**Analytical Techniques**

* Aggregation
* Time-Series Analysis
* Customer Analysis
* Product Analysis
* Regional Analysis
* Discount Analysis
* Window Functions
* Month-over-Month Analysis

---

## 📌 Project Takeaway

This project demonstrates how raw retail transaction data can be transformed into **business-ready insights** by combining Python-based analysis, SQL querying, and interactive Power BI visualization.
The focus is not only on reporting what happened, but also on identifying **profitability issues, product and customer opportunities, regional patterns, and operational factors** that can support better business decision-making.

---
## 👩‍💻 Author

**Taniya**

Aspiring **Data Analyst** focused on SQL, Python, Excel, Power BI, and business intelligence.

---

⭐ **If you found this project useful, consider giving the repository a star!**
