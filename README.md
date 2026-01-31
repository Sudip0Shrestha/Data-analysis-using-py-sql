# 🛒 E-commerce Data Analysis using Python & MySQL

This project demonstrates an **end-to-end data analytics workflow** using **Python, Pandas, MySQL, and SQL (advanced queries + window functions)** on a real-world e-commerce dataset.

The goal of this project is to:

* Import raw CSV data into a relational database
* Perform business-focused SQL analysis
* Visualize insights using Python
* Answer real-world analytical questions (sales, growth, retention, customer behavior)

---

## 📂 Dataset Overview

The project uses multiple CSV files representing an e-commerce platform:

| File Name         | Description                        |
| ----------------- | ---------------------------------- |
| `customers.csv`   | Customer information & location    |
| `orders.csv`      | Order lifecycle & timestamps       |
| `order_items.csv` | Products included in each order    |
| `products.csv`    | Product details & categories       |
| `payments.csv`    | Payment type, value & installments |
| `sellers.csv`     | Seller information                 |
| `geolocation.csv` | Customer geolocation data          |

---

## 🛠️ Tech Stack

* **Python** 🐍
* **Pandas** (Data processing)
* **MySQL** (Relational database)
* **SQL** (Joins, CTEs, Window Functions)
* **Matplotlib & Seaborn** (Data Visualization)
* **NumPy** (Correlation analysis)

---

## ⚙️ Data Ingestion Pipeline

✔ Automatically reads CSV files using Pandas
✔ Cleans column names for SQL compatibility
✔ Detects data types dynamically
✔ Creates MySQL tables programmatically
✔ Inserts data safely handling NULL values

```python
CREATE TABLE IF NOT EXISTS table_name (...)
INSERT INTO table_name VALUES (...)
```

This ensures the database schema is built **directly from the data**.

---

## 📊 Business Questions Answered

### 🔹 Customer & Orders

* List all **unique customer cities**
* Count **total orders placed in 2017**
* Customers distribution **by state**
* **Top 3 customers per year** by total spend

### 🔹 Sales & Revenue

* Total sales **per product category**
* Percentage contribution of each category to total revenue
* **Year-over-Year (YoY) growth rate** of sales
* **Cumulative monthly revenue** across years

### 🔹 Payments & Behavior

* Percentage of orders paid using **installments**
* **Moving average of order value** per customer
* **Retention rate** (repeat purchase within 6 months)

### 🔹 Advanced Analytics

* Correlation between **product price** and **purchase frequency**
* Seller-wise revenue ranking using `DENSE_RANK()`

---

## 🧠 SQL Concepts Used

* `JOIN` (INNER JOIN)
* `GROUP BY`, `ORDER BY`
* `CTE (WITH clause)`
* `WINDOW FUNCTIONS`

  * `AVG() OVER()`
  * `SUM() OVER()`
  * `LAG()`
  * `DENSE_RANK()`
* Date functions (`YEAR()`, `MONTH()`, `DATE_ADD()`)

---

## 📈 Visualizations

* Bar charts for:

  * Customers by state
  * Monthly orders
  * Top sellers by revenue
* Labels and formatting for clear storytelling

---

## 📌 Key Insights

* Most revenue comes from **Bed, Bath & Furniture categories**
* Installment payments dominate (~99.9%)
* Weak negative correlation between price and purchase frequency
* Significant YoY growth from 2016 → 2017
* Customer retention within 6 months is **very low**, indicating churn

---

## ▶️ How to Run

1. Install dependencies

```bash
pip install pandas mysql-connector-python matplotlib seaborn numpy
```

2. Create MySQL database

```sql
CREATE DATABASE ecommerce;
```

3. Update MySQL credentials in the script

4. Run the Python script to:

* Load CSVs into MySQL
* Execute SQL queries
* Generate visualizations

---

## 🚀 Future Improvements

* Add indexes & primary/foreign keys
* Improve retention query logic
* Build a dashboard (Power BI / Tableau)
* Automate with Airflow
* Optimize insert performance (bulk inserts)

---

## 👨‍💻 Author

**Sudip Shrestha**
Bachelor's in CSIT | Aspiring Data Scientist
Python • SQL • Machine Learning

---

⭐ If you found this project useful, give it a **star** on GitHub!
