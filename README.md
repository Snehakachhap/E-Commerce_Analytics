# E-Commerce Analytics: Business Performance &amp; Customer Insights

An end-to-end **E-Commerce Analytics project** that transforms raw transactional and clickstream data into a structured, decision-oriented business intelligence solution using **Excel, Python, and Power BI**.

The project covers the complete analytics pipeline — from **initial data exploration and audit in Excel**, to **programmatic data cleaning and validation in Python**, followed by **Power BI data modeling, DAX-based analysis, and interactive dashboard development**.

The objective is to ensure that the data is **understood, validated, modeled, and then translated into meaningful business insights**.

---

## 📌 Business Problem

An e-commerce business generates data across customers, products, website sessions, customer events, orders, order items, and reviews.

Individually, these datasets provide only partial information. When combined without proper validation and modeling, it becomes difficult to answer important business questions reliably.

### The core question this project addresses:

> **How can raw e-commerce transaction and clickstream data be audited, cleaned, validated, and modeled to reveal reliable insights into revenue and profitability, product performance, customer value, website engagement, conversion behavior, and customer satisfaction?**

This project addresses the problem through a structured **Excel → Python → Power BI** analytics workflow.

---

# 🎯 Project Objectives

* Audit raw datasets for **missing values, duplicates, key uniqueness, and structural issues**
* Clean and validate the data programmatically using **Python**
* Verify relationships between the seven related datasets
* Prepare clean datasets for business intelligence analysis
* Build a relational **Power BI data model**
* Create business-focused **DAX measures and calculated columns**
* Analyze revenue, orders, profit, and profitability
* Compare business performance **year over year**
* Analyze product and category performance
* Understand customer purchasing behavior and customer value
* Measure website engagement and purchase conversion
* Analyze traffic-source performance
* Evaluate customer reviews and product satisfaction
* Build a five-page interactive Power BI dashboard around a coherent business story

---

# 🔄 Analytics Workflow

```text
Raw E-Commerce Data
        ↓
Data Understanding & Exploration
        ↓
Excel Data Audit
        ↓
Python Data Cleaning & Validation
        ↓
Data Quality & Relationship Checks
        ↓
Cleaned & Validated Data
        ↓
Power BI Data Modeling
        ↓
DAX Measures & Calculated Columns
        ↓
Interactive Dashboard
        ↓
Business Analysis & Insights
```
---

# 📊 Dataset

The project uses an **E-Commerce Transactions & Clickstream** dataset consisting of seven related tables.

## Dataset Tables

| Table         | Description                                                                  | Primary Key   | Foreign Keys               |
| ------------- | ---------------------------------------------------------------------------- | ------------- | -------------------------- |
| `customers`   | Customer profile, demographics, and signup information                       | `customer_id` | —                          |
| `products`    | Product catalog, category, price, cost, and margin information               | `product_id`  | —                          |
| `sessions`    | Website visit/session information and traffic sources                        | `session_id`  | `customer_id`              |
| `events`      | Customer clickstream activity such as page views, add-to-cart, and purchases | `event_id`    | `session_id`, `product_id` |
| `orders`      | Completed order-level transactions                                           | `order_id`    | `customer_id`              |
| `order_items` | Product-level details within each order                                      | —             | `order_id`, `product_id`   |
| `reviews`     | Customer reviews and product ratings                                         | `review_id`   | `order_id`, `product_id`   |

### Dataset Scale

| Table       |    Rows | Columns |
| ----------- | ------: | ------: |
| Customers   |  20,000 |       7 |
| Products    |   1,197 |       6 |
| Sessions    | 120,000 |       6 |
| Events      | 760,958 |      10 |
| Orders      |  33,580 |      10 |
| Order Items |  59,163 |       5 |
| Reviews     |  10,780 |       6 |

**Total:** 7 related tables covering customers, products, transactions, website activity, and customer feedback.

---

# 🧹 1. Excel — Data Audit & Exploration

The project begins with a structured **first-pass audit in Excel** before any programmatic cleaning.

The purpose of this stage was to understand the raw data and identify potential quality issues before using it for analysis.

### Audit Checks

* Row and column counts
* Blank-value checks
* Duplicate checks
* Primary-key identification
* Foreign-key identification
* Data structure inspection
* Pivot-based exploration
* Initial validation of important business fields

Excel provided the initial understanding of the datasets and established a baseline for comparison with the Python validation results.

---

# ⚙️ 2. Python — Data Cleaning & Validation

Python was used in **Google Colab** with **Pandas and NumPy** to perform reproducible data cleaning and validation.

### Data Processing

The Python workflow included:

* Loading all seven Excel datasets
* Inspecting dataset dimensions
* Reviewing column names and schemas
* Checking and standardizing data types
* Generating missing-value summaries
* Detecting duplicate rows
* Converting date/time fields to `datetime`
* Converting nullable numerical fields to appropriate types
* Standardizing discount-related fields
* Removing exact duplicate rows from `order_items`
* Rechecking data quality after cleaning
* Validating key uniqueness
* Testing candidate composite keys
* Checking foreign-key integrity
* Generating a final data-quality summary
* Exporting cleaned datasets for Power BI

---

# 📈 3. Power BI — Data Modeling & Dashboarding

After cleaning and validation, the prepared datasets were imported into **Power BI**.

The Power BI stage focused on:

* Relational data modeling
* Table relationships
* Date-table creation
* DAX measures
* Calculated columns
* Time intelligence
* Customer segmentation
* KPI development
* Interactive visualizations
* Business-focused dashboard design
  
---

# 📊 Dashboard Pages

The final Power BI report contains **five analytical pages**, structured to tell a progressive business story.

---

## 1️⃣ Executive Overview - Business Performance

<img width="971" height="552" alt="image" src="https://github.com/user-attachments/assets/8fce32da-adad-4368-a979-d688562ac619" />

### KPIs

* Total Revenue
* Revenue Growth %
* Total Orders
* Order Growth %
* Average Order Value
* Total Profit
* Profit Margin %

### Analysis

* Revenue Performance — Current Year vs Previous Year
* Profit Performance — Current Year vs Previous Year
* Order Distribution by Product Category
* Revenue & Profit by Product Category

### Business Focus

Delivers a high-level view of revenue, profitability, order performance, and category contribution to support overall **business performance assessment**.

---

## 2️⃣ Product & Category Performance

<img width="970" height="547" alt="image" src="https://github.com/user-attachments/assets/b3bf1bc3-465a-4134-870f-fce123970d5e" />

### KPIs

* Total Products
* Products Sold
* Total Units Sold
* Average Product Rating

### Analysis

* Average Product Rating by Category
* Revenue & Profit by Product Category
* Profit Performance by Category — Current Year vs Previous Year
* Units Sold by Category — Current Year vs Previous Year

### Business Focus

Evaluates **product and category contribution**, including sales volume, profitability, and customer ratings.

---

## 3️⃣ Customer Analytics

<img width="970" height="547" alt="image" src="https://github.com/user-attachments/assets/716e902a-d609-4df8-9d22-77f4cd12bc99" />

### KPIs

* Total Customers
* Average Orders per Customer
* Average Customer Revenue
* Top Customer Revenue
* Top Customer Orders
* Repeat Customer Rate

### Analysis

* Revenue & Profit by Country
* Revenue by Customer Age Group
* Top Products by Customer Revenue
* Customer Revenue Distribution

### Business Focus

Examines **customer value, purchasing frequency, geographic contribution, and customer revenue distribution**.

---

## 4️⃣ Conversion Funnel - Marketing & Acquisition Performance

<img width="965" height="545" alt="image" src="https://github.com/user-attachments/assets/89612dd0-77ca-4fc3-84c7-42318ac8b150" />

### KPIs

* Total Sessions
* Total Events
* Average Events per Session
* Add-to-Cart Rate
* Purchase Conversion Rate

### Analysis

* Customer Funnel
* Sessions by Traffic Source
* Conversion Rate by Traffic Source

### Business Focus

Analyzes how customers interact with the website and how effectively engagement translates into purchase activity.

---

## 5️⃣ Customer Reviews & Product Satisfaction

<img width="966" height="545" alt="image" src="https://github.com/user-attachments/assets/87ec8e1a-fde8-4b6e-a738-6454c0193b6f" />

### KPIs

* Total Reviews
* Reviewed Product %
* Average Rating
* 5-Star Review %
* 1–2 Star Review %

### Analysis

* Review Distribution by Rating
* Average Rating by Product Category
* Review Volume by Product Category
* Revenue vs Average Rating by Category

### Business Focus

Connects **customer feedback, product categories, ratings, and revenue performance** to understand product satisfaction.

---

# 🔍 Business Questions Answered

The dashboard is designed to answer questions across five major areas.

### 💰 Business Performance

* Is revenue growing year over year?
* How are orders performing?
* What is the average order value?
* How much profit is being generated?
* What is the overall profit margin?

### 📦 Product Performance

* Which categories generate the most revenue?
* Which categories generate the most profit?
* Which categories have the highest unit sales?
* How has category performance changed year over year?
* Which products contribute most to customer revenue?

### 👥 Customer Behavior

* How much revenue does the average customer generate?
* How frequently do customers place orders?
* What proportion of customers are repeat customers?
* Which countries contribute the most revenue and profit?
* Which age groups contribute the most revenue?
* How is customer revenue distributed?

### 🛒 Engagement & Conversion

* How many sessions and events occur?
* How actively do customers interact with the website?
* What percentage of sessions result in add-to-cart activity?
* What percentage of sessions result in purchases?
* Which traffic sources generate stronger conversion?

### ⭐ Customer Satisfaction

* How are customer ratings distributed?
* Which categories have the highest average ratings?
* Which categories receive the most reviews?
* Does product/category rating appear to relate to revenue performance?

---

# 🛠️ Tools & Technologies

### Data Audit & Exploration

**Microsoft Excel**

* Data auditing
* Initial validation
* PivotTable analysis
* Structural exploration

### Data Cleaning & Validation

**Python**

* Pandas
* NumPy
* Google Colab
* Data cleaning
* Missing-value analysis
* Duplicate detection
* Data-type standardization
* Key validation
* Referential integrity checks

### Business Intelligence

**Microsoft Power BI**

* Data modeling
* Relationships
* DAX
* Calculated columns
* Measures
* Time intelligence
* Customer segmentation
* KPI cards
* Interactive slicers
* Business-focused visualizations

---

# 📚 Key Learning Outcomes

This project provided practical experience in:

* Working with a multi-table relational e-commerce dataset
* Performing structured data auditing before analysis
* Using Excel for initial exploration and validation
* Cleaning and validating data using Python/Pandas
* Distinguishing full-row duplicates from composite-key duplication
* Testing primary-key assumptions rather than blindly accepting them
* Validating foreign-key relationships across multiple tables
* Handling missing values based on data context
* Standardizing date/time and numerical data types
* Preparing clean datasets for Power BI
* Building a relational Power BI data model
* Creating business-focused DAX measures
* Implementing time-intelligence calculations
* Creating customer segmentation logic
* Allocating order-level revenue to line-item level
* Analyzing customer engagement and conversion
* Connecting product performance with customer reviews
* Designing a five-page business intelligence dashboard
* Translating business questions into KPIs and visualizations
* Structuring an end-to-end analytics project for reproducibility

---

# 🚀 Project Outcome

This project demonstrates an **end-to-end E-Commerce Analytics workflow**.

The data moves through:

```text
RAW DATA
   ↓
AUDIT
   ↓
CLEAN
   ↓
VALIDATE
   ↓
MODEL
   ↓
CALCULATE
   ↓
ANALYZE
   ↓
VISUALIZE
```

The final Power BI report brings together:

```text
Revenue & Profit
       +
Product Performance
       +
Customer Insights
       +
Website Engagement & Conversion
       +
Customer Reviews
```

into a centralized analytical solution.

The project demonstrates how raw e-commerce data can be transformed into a **structured, validated, and business-focused analytics solution** — with the complete process documented from initial data audit through final dashboard development.

---
