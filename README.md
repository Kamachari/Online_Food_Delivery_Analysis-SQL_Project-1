# 🍕 Online Food Delivery Analysis — SQL Project 1

> A beginner-level SQL analysis project exploring core business metrics of an online food delivery platform — covering orders, revenue, customer behaviour, and restaurant performance.

**Level:** 🟢 Beginner | **Status:** ✅ Complete | **Part:** 1 of 3

---

## 🔗 Demo Link

> _Screenshots of query results are available in the `/Screenshots` folder of this repository._

---

## 📑 Table of Contents

- [Business Understanding](#business-understanding)
- [Data Understanding](#data-understanding)
- [Screenshots](#screenshots)
- [Technologies](#technologies)
- [Setup](#setup)
- [Approach](#approach)
- [Status](#status)
- [Credits](#credits)

---

## 💼 Business Understanding

Online food delivery platforms handle thousands of orders daily across multiple cities and restaurants. To make smart operational and strategic decisions, businesses need to understand where orders are coming from, which items generate the most revenue, and which restaurants are performing well.

**Goal:** This project performs foundational SQL-based exploratory analysis on an online food delivery dataset to answer key business questions around orders, revenue, customers, and restaurant activity.

**Why this project?**
This is the first project in a 3-part SQL portfolio series, designed to build a strong foundation in SQL querying before progressing to advanced analytics and full business systems. It demonstrates proficiency in:
- Writing structured SQL queries for real-world business questions
- Aggregating and summarising transactional data
- Extracting actionable insights from relational datasets

**Challenges faced:**
- Joining multiple related tables (Orders, Customers, Restaurants, Menu Items) to produce meaningful aggregations
- Handling date-based trend analysis using monthly grouping
- Filtering and ranking results to surface the most relevant business insights

---

## 📊 Data Understanding

### Datasets Used
This project uses **5 relational tables** representing a food delivery platform's core data:

| Table | Description |
|---|---|
| `Customers` | Customer details including signup dates and city |
| `Orders` | Transaction records with order date and customer ID |
| `Menu_Items` | List of food items offered by restaurants with pricing |
| `Order_Details` | Line-item breakdown of items ordered per transaction |
| `Restaurants` | Restaurant information including city and menu offerings |

### Dataset Relationships
```
Customers ──< Orders ──< Order_Details >── Menu_Items
                │
            Restaurants
```

### Key Metrics Available
- Total order volume by city and restaurant
- Revenue per food item and per city
- Customer spending patterns
- Monthly order trends over time

**Future enhancements:**
- Add delivery time analysis once delivery agent data is available *(covered in Project 3)*
- Incorporate customer segmentation based on spending tiers *(covered in Project 2)*
- Build a Power BI / Excel dashboard on top of these queries

---

## 📸 Screenshots

> Query result screenshots are available in the `/Screenshots` folder.

---

## 🛠️ Technologies

| Tool | Purpose |
|---|---|
| **MySQL 8.x** | Relational database engine for data storage and querying |
| **VS Code** | Primary development IDE |
| **SQLTools Extension** | MySQL connection and query execution within VS Code |
| **SQLTools MySQL/MariaDB Driver** | VS Code driver to connect to MySQL server |
| **MySQL Workbench** | Backend MySQL server (connected via SQLTools) |
| **Git & GitHub** | Version control and project showcase |

---

## ⚙️ Setup

### Prerequisites
- MySQL Server installed and running (port 3306)
- VS Code installed
- SQLTools extension installed in VS Code
- SQLTools MySQL/MariaDB Driver installed

### Step 1 — Clone the Repository
```bash
git clone https://github.com/BuragapalliKamachari/online-food-delivery-sql-project-1.git
cd online-food-delivery-sql-project-1
```

### Step 2 — Configure SQLTools in VS Code
1. Open VS Code → Click the **SQLTools icon** in the Activity Bar
2. Select **Add New Connection** → Choose **MySQL**
3. Enter connection details:
   - Host: `localhost`
   - Port: `3306`
   - Username: `root`
   - Password: _(your MySQL root password)_
4. Click **Test Connection** → **Save**

### Step 3 — Run SQL Scripts in Order
Open each file from the `Sql_Queries/` folder and execute using `Ctrl+E+E`:

```
1. Database_Creation.sql     ← Create the project database
2. Table_Creation.sql        ← Create all 5 tables
3. Data_Insertion.sql        ← Load sample data
4. Analysis_Queries.sql      ← Run all 10 business queries
```

---

## 🔍 Approach

This project follows the **Data Analysis Lifecycle**: Define → Collect → Clean → Analyse → Report.

### Phase 1 — Database & Table Setup
- Created a dedicated MySQL database for the project
- Defined all 5 tables with appropriate data types and relationships
- Loaded the dataset into MySQL via CSV import or INSERT statements

### Phase 2 — Exploratory Analysis (10 Queries)

| # | Business Question | SQL Technique |
|---|---|---|
| 1 | Total orders per city | `GROUP BY`, `COUNT` |
| 2 | Revenue generated by each food item | `JOIN`, `SUM` |
| 3 | Top 5 spending customers | `ORDER BY`, `LIMIT` |
| 4 | Restaurant-wise order count | `GROUP BY`, `COUNT` |
| 5 | Average order value by city | `AVG`, `GROUP BY` |
| 6 | Monthly order trends | `MONTH()`, `GROUP BY` |
| 7 | Top 3 cities by revenue | `SUM`, `ORDER BY`, `LIMIT` |
| 8 | Number of unique customers per city | `COUNT(DISTINCT)` |
| 9 | Most frequently ordered items | `COUNT`, `ORDER BY DESC` |
| 10 | Restaurants with low order count (<30) | `HAVING`, `COUNT` |

### Phase 3 — Insights & Reporting
- Results exported and documented
- Screenshots captured for each key query result
- Insights summarised for progression into Project 2

---

## 📌 Status

```
✅ Complete — Sept 2025
```
This is **Part 1 of 3** in the Online Food Delivery SQL Portfolio Series:
- ✅ Project 1 — Beginner Analysis ← You are here
- ✅ Project 2 — Advanced Analytics
- 🔄 Project 3 — Business Analytics System (In Progress)

---

## 🙏 Credits

| Contributor | Role |
|---|---|
| **Buragapalli Kamachari** | Project Author — SQL Development & Analysis |
| **MySQL Documentation** | Reference for SQL functions and syntax |
| **SQLTools by Matheus Teixeira** | VS Code MySQL integration extension |
| **GitHub** | Repository hosting and portfolio showcase |

---

*Online Food Delivery SQL Project 1 of 3 | Buragapalli Kamachari | Sept 2025*
