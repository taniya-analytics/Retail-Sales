# 📊 Retail Sales Analysis | Python • SQL • Power BI

> **An end-to-end retail analytics project focused on uncovering sales trends, profitability drivers, loss-making products, discount impact, customer value, regional performance, and shipping efficiency.**

---

## 🎯 Project Overview

Retail businesses generate large volumes of transaction data, but revenue alone does not tell the complete story.

This project analyzes **9,994 retail order lines** covering approximately **5,000 unique orders and 793 customers** from **2014–2017** to understand:

- Where the business generates the most revenue and profit
- Which products and sub-categories are destroying profitability
- How discounts affect profit
- Which regions are performing well or underperforming
- Which customers generate the highest sales
- How shipping modes affect delivery time and profitability
- What seasonal sales patterns exist
- Where management should focus to improve profitability

The project follows a complete analytics workflow:

**Raw Data → Python Cleaning & EDA → SQL Business Analysis → Power BI Dashboard → Business Insights & Recommendations**

---

# 📌 Business Problem

The business generates consistent revenue but experiences significant differences in profitability across products, regions, customers, and discount levels.

Management needs a data-driven view of:

> **Where are we making money, where are we losing money, and why?**

The analysis was designed to support decisions around:

- Pricing
- Discount strategy
- Product profitability
- Regional performance
- Customer retention
- Shipping operations
- Inventory and seasonal planning

---

# 📂 Dataset

**Dataset:** Superstore Retail Sales Dataset

**Period:** 2014–2017  
**Order Lines:** 9,994  
**Unique Orders:** ~5,000  
**Customers:** 793  
**Categories:** 3  
**Regions:** 4

### Key Data Fields

| Area | Columns |
|---|---|
| Order | Order ID, Order Date, Ship Date, Ship Mode |
| Customer | Customer ID, Customer Name, Segment |
| Geography | Region, State, City |
| Product | Product ID, Product Name, Category, Sub-Category |
| Metrics | Sales, Profit, Discount, Quantity |

---

# 🛠️ Tech Stack

### Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

**Used for:**
- Data loading
- Data quality checks
- Missing-value analysis
- Duplicate detection
- Data-type correction
- Feature engineering
- Exploratory Data Analysis

### SQL Server

**Used for:**
- Business-question analysis
- Aggregations
- GROUP BY
- CASE statements
- CTEs
- Window functions
- LAG()
- Date calculations
- Profitability analysis
- Customer and product analysis

### Power BI

**Used for:**
- KPI development
- Interactive dashboard
- Sales & profit visualization
- Category analysis
- Regional analysis
- Product performance
- Shipping analysis
- Time-series analysis
- Interactive filtering

---

# 🔄 Analytics Workflow

```text
                RAW SUPERSTORE DATA
                        │
                        ▼
              ┌──────────────────┐
              │ Python / Pandas  │
              │ Data Cleaning    │
              │ Data Validation  │
              │ Feature Creation │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │   SQL Server     │
              │ Business Queries │
              │ KPI Analysis     │
              │ Trend Analysis   │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │     Power BI     │
              │ Interactive      │
              │ Dashboard        │
              └────────┬─────────┘
                       │
                       ▼
              BUSINESS INSIGHTS
                       │
                       ▼
            ACTIONABLE RECOMMENDATIONS
```

---

# 🧹 1. Data Cleaning & Preparation

The dataset was first prepared using Python and Pandas.

### Data quality checks

- Checked dataset structure and dimensions
- Reviewed data types
- Checked missing values
- Checked duplicate records
- Standardized column names
- Converted date columns into proper datetime format
- Reviewed categorical variables
- Investigated negative-profit transactions

### Feature Engineering

Created additional analytical fields:

```python
df['order_year'] = df['order_date'].dt.year
df['order_month'] = df['order_date'].dt.month
df['shipping_days'] = (
    df['ship_date'] - df['order_date']
).dt.days
```

These features enabled time-series, shipping, and profitability analysis.

---

# 🔎 2. Exploratory Data Analysis

Python EDA was performed to understand the structure and behavior of the dataset.

### Areas analyzed

- Sales distribution
- Profit distribution
- Discount patterns
- Category performance
- Regional performance
- Negative-profit transactions
- Sales trends
- Shipping duration
- Customer behavior
- Product performance

The dataset contained:

- **No missing values**
- **No duplicate rows**

---

# 🧮 3. SQL Business Analysis

SQL Server was used to answer **12 business questions**.

### Key Business Questions

| # | Business Question |
|---|---|
| 01 | What are total sales and profit by category? |
| 02 | Which sub-category generates the most loss? |
| 03 | Which regions have the strongest sales and profit performance? |
| 04 | What does the monthly sales trend look like? |
| 05 | What are the top 10 best-selling products? |
| 06 | Which products generate the highest losses? |
| 07 | What is the relationship between discount and profit? |
| 08 | Who are the top customers by sales? |
| 09 | What is the average shipping time by ship mode? |
| 10 | What percentage of order lines result in a loss? |
| 11 | What is the month-over-month sales growth? |
| 12 | How does ship mode affect sales and profit? |

### SQL Techniques Demonstrated

```text
GROUP BY
ORDER BY
CASE WHEN
CTEs
Aggregate Functions
JOIN / Relational Analysis
Date Functions
DATEDIFF()
LAG()
Window Functions
Percentage Calculations
```

---

# 📊 4. Key Business Findings

## 💰 Overall Performance

| KPI | Result |
|---|---:|
| Total Sales | **₹2.30M** |
| Total Profit | **₹286K** |
| Profit Margin | **12.47%** |
| Order Lines | **9,994** |
| Unique Orders | **~5K** |
| Customers | **793** |
| Loss-Making Order Lines | **18.72%** |

### 🔥 Key Finding

Approximately **1 in every 5 order lines generates a loss**, making profitability management a major business priority.

---

## 🏆 Technology Is the Strongest Category

Technology generated the highest overall performance:

| Category | Sales | Profit |
|---|---:|---:|
| Office Supplies | ₹719K | ₹122K |
| Furniture | ₹742K | ₹18K |
| **Technology** | **₹836K** | **₹145K** |

Technology also had the **lowest average discount at 13.23%** and the **highest average profit per order at ₹78.75**.

### Business Implication

Technology appears to provide a stronger combination of **revenue generation and profitability**, making it a strong candidate for continued inventory and marketing investment.

---

# ⚠️ Furniture Is the Major Profitability Concern

Furniture generated approximately **₹742K in sales**, but only **₹18K in profit**.

Its average discount was the highest:

**17.39%**

The biggest problem areas were:

- Tables → **-₹17,725 profit**
- Bookcases → **-₹3,473 profit**
- Supplies → **-₹1,189 profit**

### Business Implication

High sales do not necessarily mean healthy business performance.

Furniture requires deeper investigation into **pricing, discounting, product costs, and product-level margins**.

---

# 🌎 Regional Performance

| Region | Sales | Profit |
|---|---:|---:|
| **West** | ₹725K | **₹108K** |
| East | ₹679K | ₹92K |
| South | ₹392K | ₹47K |
| **Central** | ₹501K | **₹40K** |

### Key Insight

The **West region leads in profitability**, while the **Central region generates the lowest profit despite having moderate sales**.

### Recommendation

Investigate Central-region:

- Discount levels
- Product mix
- Shipping costs
- Operating costs
- Loss-making sub-categories

---

# 📅 Seasonal Sales Pattern

Sales increased substantially over the four-year period:

| Year | Sales |
|---|---:|
| 2014 | ₹411K |
| 2015 | ₹469K |
| 2016 | ₹608K |
| 2017 | ₹733K |

Sales consistently peak around **November and December**.

The highest monthly sales recorded were approximately:

**November 2017 → ₹118K**

### Business Implication

The business should prepare inventory, staffing, and promotional capacity ahead of the year-end demand surge.

---

# 🚚 Shipping Analysis

Average shipping duration:

| Ship Mode | Avg. Shipping Days |
|---|---:|
| Same Day | 0 |
| First Class | 2 |
| Second Class | 3 |
| Standard Class | 5 |

**Standard Class** is the dominant shipping mode, accounting for approximately **59% of sales**.

Interestingly, **First Class has the highest average profit per order (~₹31.84)**.

---

# 👥 Customer Analysis

The analysis identified the top customers by sales.

One notable finding:

> **Sean Miller generated approximately ₹25K in sales but was loss-making overall with approximately -₹1,981 profit.**

### Business Implication

High-value customers should not be evaluated using revenue alone.

Customer profitability should also consider:

- Discounting
- Product mix
- Order profitability
- Fulfillment costs

---

# 📈 Power BI Dashboard

The project includes an interactive **Superstore Sales Dashboard** built in Power BI.

### Dashboard Features

- Total Sales KPI
- Total Orders KPI
- Total Customers KPI
- Sales by Category
- Monthly Sales Trend
- Sales by Region
- Top Products by Sales
- Profit by Sub-Category
- Sales by Ship Mode
- Region filter
- State filter
- Category filter
- Ship Mode filter
- Segment filter
- Reset Filters button
- Key Insights section

### Dashboard Preview

![Superstore Sales Dashboard](superstore%20sales%20dashboard.png)

---

# 💡 Business Recommendations

### 1. Review Furniture Discount Strategy

Furniture has the highest average discount and significantly lower profitability.

**Action:** Review discount limits for Tables and Bookcases and evaluate product-level margins before applying large discounts.

---

### 2. Investigate Major Loss-Making Products

Products such as:

- Cubify CubeX 3D Printers
- Large conference tables
- Selected printers and office equipment

generate significant losses.

**Action:** Review their pricing, cost structure, discount levels, and demand before continuing aggressive sales.

---

### 3. Continue Investing in Technology

Technology generates the strongest combination of sales and profitability.

**Action:** Prioritize high-performing technology products for inventory planning and marketing campaigns.

---

### 4. Improve Central Region Profitability

Central generates significantly less profit compared with West and East.

**Action:** Analyze regional product mix, discounts, shipping costs, and operational expenses.

---

### 5. Prepare for Year-End Demand

November and December consistently show strong sales.

**Action:** Increase inventory availability and operational capacity before the seasonal peak.

---

### 6. Evaluate Customer Profitability

High-revenue customers can still be unprofitable.

**Action:** Segment customers based on **both sales and profit**, rather than revenue alone.

---

# 📁 Project Structure

```text
Retail-Sales-Analysis/
│
├── 📓 Retail_sales_Exploratory Data Analysis.ipynb
│
├── 🗄️ RetailSales_Analysis.sql
│
├── 📊 Superstore sales Dashboard.pbix
│
├── 🖼️ superstore sales dashboard.png
│
├── 📑 Retail_Sales_Analysis_Report.pdf
│
├── 📽️ Retail_sales+presentation.pptx
│
├── 📋 Problem_Statement_Retail_Sales_Analysis.pdf
│
├── 📊 sample_superstore.xlsm
│
└── 📄 LICENSE
```

---

# 🚀 How to Explore the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Retail-Sales-Analysis.git
cd Retail-Sales-Analysis
```

### 2. Explore the Python Analysis

Open:

```text
Retail_sales_Exploratory Data Analysis.ipynb
```

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn openpyxl
```

Run the notebook to reproduce the data preparation and exploratory analysis.

---

### 3. Run the SQL Analysis

Open:

```text
RetailSales_Analysis.sql
```

Create the database in SQL Server and load the dataset into the required table.

The SQL script contains the business questions and analytical queries used in the project.

---

### 4. Open the Power BI Dashboard

Open:

```text
Superstore sales Dashboard.pbix
```

using **Power BI Desktop**.

Use the slicers to interactively explore performance across:

- Region
- State
- Category
- Ship Mode
- Segment

---

# 📑 Project Deliverables

| Deliverable | Purpose |
|---|---|
| Python Notebook | Data cleaning & EDA |
| SQL Script | Business analysis |
| Power BI Dashboard | Interactive visualization |
| PDF Report | Detailed analysis & findings |
| Presentation | Stakeholder-friendly summary |
| Dataset | Source data for analysis |

---

# 🎯 Skills Demonstrated

### Technical Skills

`Python` `Pandas` `NumPy` `SQL Server` `Advanced SQL` `Power BI` `DAX` `Data Cleaning` `EDA` `Data Visualization` `KPI Analysis` `Feature Engineering` `Business Intelligence`

### Analytical Skills

`Business Problem Solving`  
`Trend Analysis`  
`Profitability Analysis`  
`Customer Analysis`  
`Product Analysis`  
`Regional Analysis`  
`Discount Analysis`  
`Time-Series Analysis`  
`Root Cause Analysis`  
`Data-Driven Recommendations`

---

# 🧠 What This Project Demonstrates

This project goes beyond simply creating charts.

It demonstrates the ability to:

**1. Clean and validate raw business data**

↓  

**2. Explore data and identify patterns**

↓  

**3. Translate business problems into SQL questions**

↓  

**4. Perform KPI and profitability analysis**

↓  

**5. Build an interactive BI dashboard**

↓  

**6. Convert analytical findings into business recommendations**

---

# 📌 Final Takeaway

The analysis shows that **revenue alone is not enough to measure business performance**.

Technology demonstrates strong sales and profitability with relatively low discounting, while Furniture generates substantial revenue but significantly weaker profit due to high discounting and loss-making sub-categories.

The project ultimately provides a data-driven framework for improving:

**Profitability → Pricing → Discount Strategy → Regional Performance → Customer Value → Operational Planning**

---

## 👤 Author

**Taniya**

Aspiring Data Analyst | SQL | Python | Power BI | Excel

Focused on transforming raw business data into **actionable insights and data-driven decisions**.

---

⭐ **If you found this project useful, consider giving the repository a star!**
