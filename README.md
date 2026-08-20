# Customer Shopping Behavior Analysis

An end-to-end data analytics project focused on understanding customer purchasing behavior, product performance, revenue patterns, subscription behavior, and customer segmentation using **Python, SQL, MySQL, and Power BI**.

---

## 📌 Overview

Understanding customer behavior is essential for businesses to improve customer retention, optimize product offerings, design effective promotional strategies, and increase revenue.

However, raw transactional data often contains valuable information that is difficult to interpret directly. This project transforms customer shopping data into meaningful business insights through a structured analytics workflow.

The project covers the complete data analytics lifecycle:

**Data Cleaning → Data Transformation → Database Integration → SQL Analysis → Business Intelligence Dashboard**

---

## 🎯 Problem Statement

Businesses generate large volumes of customer transaction data, but without proper analysis, it is difficult to identify important patterns in **customer spending, product performance, discounts, subscriptions, purchasing frequency, and customer loyalty**.

This project aims to analyze customer shopping behavior and answer key business questions such as:

* Which customer segments contribute the most revenue?
* Which products have the highest ratings and purchase frequency?
* Do subscribed customers spend more than non-subscribers?
* Which products have the highest discount usage?
* How can customers be categorized based on their purchasing history?
* Are repeat customers more likely to subscribe?
* Which age groups contribute the most revenue?
* How does shipping type relate to customer spending?

The objective is to convert raw customer transaction data into **actionable insights that can support data-driven business decisions**.

---

## 🎯 Objectives

* Perform data cleaning and preprocessing using Python.
* Handle missing values and transform raw attributes into analysis-ready features.
* Store and manage the processed data using MySQL.
* Perform exploratory and business-oriented analysis using SQL.
* Apply advanced SQL concepts such as **CTEs, subqueries, CASE statements, and window functions**.
* Segment customers based on previous purchasing behavior.
* Analyze revenue, product performance, discounts, subscriptions, and customer demographics.
* Develop an interactive Power BI dashboard for business reporting.

---

## 🗂️ Dataset

The project uses the **Customer Shopping Behavior** dataset containing customer-level purchase information.

### Key Attributes

| Attribute              | Description                    |
| ---------------------- | ------------------------------ |
| Customer ID            | Unique customer identifier     |
| Age                    | Customer age                   |
| Gender                 | Customer gender                |
| Item Purchased         | Product purchased              |
| Category               | Product category               |
| Purchase Amount        | Amount spent                   |
| Location               | Customer location              |
| Size                   | Product size                   |
| Color                  | Product color                  |
| Season                 | Purchase season                |
| Review Rating          | Customer review rating         |
| Subscription Status    | Customer subscription status   |
| Shipping Type          | Selected shipping method       |
| Discount Applied       | Whether a discount was applied |
| Promo Code Used        | Whether a promo code was used  |
| Previous Purchases     | Number of previous purchases   |
| Payment Method         | Payment method used            |
| Frequency of Purchases | Customer purchase frequency    |

---

## 🛠️ Tech Stack

| Technology           | Purpose                                 |
| -------------------- | --------------------------------------- |
| **Python**           | Data cleaning and transformation        |
| **Pandas**           | Data manipulation and preprocessing     |
| **NumPy**            | Numerical operations                    |
| **Jupyter Notebook** | Analysis environment                    |
| **MySQL**            | Database management                     |
| **SQL**              | Business analysis                       |
| **SQLAlchemy**       | Python–MySQL connectivity               |
| **MySQL Connector**  | Database connection                     |
| **Power BI**         | Interactive dashboard and visualization |
| **Git & GitHub**     | Version control and project management  |

---

# 🔄 Project Workflow

### 1. Data Collection

The raw customer shopping dataset is imported into Python using Pandas.

### 2. Data Cleaning

The dataset is examined for:

* Missing values
* Incorrect data types
* Inconsistent column names
* Data quality issues

Missing values are handled using appropriate statistical techniques, including category-level median imputation for review ratings.

### 3. Data Transformation

Additional analytical features are created, including **age groups** and transformed purchase-frequency values.

Customers are categorized into different age groups using quantile-based segmentation.

### 4. Database Integration

The processed dataset is loaded into a MySQL database:

```text
Database: customer_behaviour
Table: customer
```

### 5. SQL Analysis

SQL is used to answer business questions involving:

* Revenue
* Customer segmentation
* Product performance
* Discounts
* Subscription behavior
* Shipping preferences
* Customer loyalty

### 6. Power BI Dashboard

The processed data is visualized through an interactive Power BI dashboard to make the analysis easier to interpret and communicate.

---

# 📊 SQL Business Analysis

The project includes several business-oriented SQL analyses.

### Revenue Analysis

Revenue is analyzed across customer demographics such as gender and age group.

### Customer Spending Analysis

Customers who used discounts but still spent at or above the average purchase amount are identified.

### Product Performance

Products are ranked based on their average review ratings and purchase frequency.

### Subscription Analysis

Subscriber and non-subscriber groups are compared based on:

* Customer count
* Average purchase amount
* Total revenue

### Discount Analysis

The percentage of purchases involving discounts is calculated for individual products.

### Customer Segmentation

Customers are categorized as:

* **New** — 1 previous purchase
* **Returning** — 2–10 previous purchases
* **Loyal** — More than 10 previous purchases

### Product Ranking

The `ROW_NUMBER()` window function is used with `PARTITION BY` to identify the top three products within each category.

### Repeat Customer Analysis

Customers with more than five previous purchases are analyzed to understand their subscription behavior.

These analyses are implemented in the project's SQL file.

---

# 📈 Power BI Dashboard

The Power BI dashboard provides an interactive view of customer shopping behavior.

### Dashboard Analysis Includes

* Customer overview
* Revenue analysis
* Product performance
* Category performance
* Subscription analysis
* Age-group analysis
* Customer purchasing behavior
* Discount analysis

### Interactive Filters

The dashboard allows users to explore the data based on dimensions such as:

* Gender
* Category
* Age Group
* Subscription Status
* Payment Method

The dashboard is designed to convert analytical results into an easily understandable business-reporting format.

---

# 🔍 Key Business Questions

The project addresses the following questions:

1. What is the total revenue generated by each gender?
2. Which customers used discounts while spending above the average purchase amount?
3. Which five products have the highest average review ratings?
4. How does average spending differ between Standard and Express shipping?
5. Do subscribed customers spend more than non-subscribers?
6. Which products have the highest percentage of discounted purchases?
7. How many customers fall into New, Returning, and Loyal segments?
8. What are the top three products within each category?
9. Are repeat buyers more likely to subscribe?
10. Which age group contributes the most revenue?

These questions are directly represented in the SQL analysis included in the project.

---

# 📁 Project Structure

```text
Customer-Shopping-Behavior-Analysis/
│
├── customer_shopping_behavior.csv
├── Customer shopping behavior Analysis.ipynb
├── customer behavior analysis.sql
├── Customer Behavior analysis.pbix
└── README.md
```

### Files

**`customer_shopping_behavior.csv`**
Raw customer shopping dataset.

**`Customer shopping behavior Analysis.ipynb`**
Python notebook containing data cleaning, transformation, and analysis.

**`customer behavior analysis.sql`**
MySQL database queries used for business analysis.

**`Customer Behavior analysis.pbix`**
Power BI dashboard containing interactive visualizations.

---

# 🚀 Getting Started

## Prerequisites

Make sure the following are installed:

* Python 3.x
* Jupyter Notebook
* MySQL
* MySQL Workbench
* Power BI Desktop

---

## 1. Clone the Repository

```bash
git clone <repository-url>
cd Customer-Shopping-Behavior-Analysis
```

## 2. Install Python Dependencies

```bash
pip install pandas numpy sqlalchemy mysql-connector-python jupyter
```

## 3. Run the Jupyter Notebook

Open:

```text
Customer shopping behavior Analysis.ipynb
```

Run the notebook sequentially to perform data cleaning and transformation.

## 4. Configure MySQL

Create the database:

```sql
CREATE DATABASE customer_behaviour;

USE customer_behaviour;
```

Update your MySQL connection credentials in the notebook and load the processed dataset into the `customer` table.

## 5. Execute SQL Analysis

Open:

```text
customer behavior analysis.sql
```

Run the queries using MySQL Workbench.

## 6. Open the Power BI Dashboard

Open:

```text
Customer Behavior analysis.pbix
```

Refresh the data connection if required and explore the dashboard using the available filters.

---

# 📌 Skills Demonstrated

### Data Analytics

* Data Cleaning
* Data Preprocessing
* Exploratory Data Analysis
* Feature Engineering
* Business Analysis

### Python

* Pandas
* NumPy
* Data Transformation
* Missing Value Handling

### SQL

* Aggregate Functions
* Subqueries
* CTEs
* CASE Statements
* Window Functions
* `ROW_NUMBER()`
* `PARTITION BY`
* Data Aggregation

### Business Intelligence

* Power BI
* Dashboard Development
* Interactive Filtering
* KPI Analysis
* Data Visualization

---


# 👨‍💻 Author

**Avni Gupta**

Data Analytics & Machine Learning Enthusiast

**Technical Skills:**
Python • Pandas • NumPy • SQL • MySQL • Power BI • Data Analysis • Data Visualization • Machine Learning

---
