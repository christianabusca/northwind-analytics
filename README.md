# 🚀 Northwind Analytics Odyssey

> *From SQL Novice to Data Storyteller: Your Journey Through E-Commerce Intelligence*

[![SQL](https://img.shields.io/badge/SQL-Analytics-blue?style=for-the-badge&logo=postgresql)](https://www.postgresql.org/)
[![Learning Path](https://img.shields.io/badge/Learning-Progressive-green?style=for-the-badge)](https://github.com)
[![Difficulty](https://img.shields.io/badge/Level-Beginner%20to%20Advanced-orange?style=for-the-badge)](https://github.com)

---

## 🎯 What is This?

Welcome to **Northwind Analytics Odyssey** – a carefully crafted, progressive SQL learning journey using the classic Northwind e-commerce database. This isn't just another SQL tutorial; it's a story-driven path that transforms you from writing basic queries to building executive-level analytics dashboards.

Think of it as your **data analysis bootcamp** where every query teaches you something new, and every section builds on the last like chapters in a compelling book.

---

## 🗺️ The Journey Ahead

### **Act I: Data Discovery** 🔍
*Learn to navigate and understand your data landscape*

- **Chapter 1:** Exploring the Territory – Basic SELECT, filtering, sorting
- **Chapter 2:** Finding Patterns – LIKE, wildcards, NULL handling
- **Chapter 3:** Counting What Matters – Aggregations and simple analytics

**Skills Unlocked:** `SELECT`, `WHERE`, `ORDER BY`, `LIKE`, `COUNT()`, `SUM()`, `AVG()`

---

### **Act II: The Art of Grouping** 📊
*Master the power of summarization and categorization*

- **Chapter 4:** Grouping by Category – GROUP BY fundamentals
- **Chapter 5:** Filtering the Aggregates – HAVING clause mastery
- **Chapter 6:** Multi-dimensional Analysis – Complex groupings

**Skills Unlocked:** `GROUP BY`, `HAVING`, Multi-level aggregations, Business metrics

---

### **Act III: Connecting the Dots** 🔗
*Weave together relationships across your data universe*

- **Chapter 7:** Simple Connections – Two-table JOINs
- **Chapter 8:** The Grand Tapestry – Multi-table JOINs
- **Chapter 9:** Finding the Gaps – LEFT JOINs and missing data

**Skills Unlocked:** `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, Table relationships, Data integrity

---

### **Act IV: Business Intelligence** 💼
*Answer real-world business questions with data*

- **Chapter 10:** Revenue Detective – Sales and revenue analysis
- **Chapter 11:** Product Performance – Rankings and trends
- **Chapter 12:** Customer Intelligence – Segmentation and insights
- **Chapter 13:** Time Traveler – Temporal analysis and forecasting

**Skills Unlocked:** Window functions, `LAG()`, `LEAD()`, `ROW_NUMBER()`, `NTILE()`, CTEs

---

### **Act V: Master Analytics** 🎓
*Tackle complex problems like a seasoned data professional*

- **Chapter 14:** Executive Dashboards – KPIs and metrics
- **Chapter 15:** Data Quality Guardian – Validation queries
- **Chapter 16:** Strategic Insights – Retention, affinity, seasonality

**Skills Unlocked:** Complex CTEs, Subqueries, Set operations, Advanced window functions

---

### **Act VI: The Final Showcase** 🏆
*Build a complete analytics solution*

Your capstone project: A comprehensive executive sales dashboard that synthesizes everything you've learned into a production-ready analytical tool.

---

## 🎓 Learning Philosophy

### **Progressive Complexity**
Each task introduces exactly **one or two new concepts** while reinforcing previous skills. No cognitive overload!

### **Real Business Context**
Every query solves an actual business problem. You're not just learning syntax; you're learning to think like an analyst.

### **Fail-Safe Design**
Tasks are ordered so that if you get stuck, you can still complete earlier sections and build confidence.

### **Hands-On Practice**
No passive reading – every concept comes with practical tasks you execute yourself.

---

## 📁 Repository Structure

```
northwind-analytics-odyssey/
│
├── 01-data-discovery/
│   ├── explore-tables.sql
│   ├── filter-and-sort.sql
│   └── pattern-matching.sql
│
├── 02-aggregation-grouping/
│   ├── basic-aggregations.sql
│   ├── group-by-fundamentals.sql
│   └── filtering-grouped-data.sql
│
├── 03-joins/
│   ├── simple-joins.sql
│   ├── multi-table-joins.sql
│   └── left-joins.sql
│
├── 04-business-analytics/
│   ├── revenue-analysis.sql
│   ├── product-performance.sql
│   ├── customer-insights.sql
│   └── time-based-analysis.sql
│
├── 05-advanced-challenges/
│   ├── executive-dashboards.sql
│   ├── data-quality-checks.sql
│   └── complex-business-questions.sql
│
├── 06-final-project/
│   └── executive-sales-dashboard.sql
│
├── data/
│   └── northwind-erd.png
│
└── README.md (you are here!)
```

---

## 🚦 Getting Started

### **Prerequisites**
- Basic understanding of databases (what a table is, what a row/column is)
- PostgreSQL installed (version 12+)
- Docker (optional, for containerized setup)
- Curiosity and determination! 🔥

### **Recommended Tools**
- **pgAdmin** – Visual PostgreSQL administration
- **DBeaver** – Universal database tool
- **VS Code with SQLTools extension** – Lightweight SQL IDE
- **TablePlus** – Modern database GUI (macOS/Windows)

### **Database Setup**

This project uses the **Northwind database for PostgreSQL** originally from [pthom/northwind_psql](https://github.com/pthom/northwind_psql).

#### **Option 1: Docker Setup (Recommended)** 🐳

```bash
# Clone the base Northwind database repository
git clone https://github.com/pthom/northwind_psql.git
cd northwind_psql

# Start PostgreSQL with Northwind data
docker-compose up -d

# Verify the database is running
docker ps
```

**Connection Details:**
- Host: `localhost`
- Port: `5432`
- Database: `northwind`
- User: `postgres`
- Password: `postgres`

#### **Option 2: Manual PostgreSQL Setup**

```bash
# 1. Create the database
psql -U postgres -c "CREATE DATABASE northwind;"

# 2. Import the Northwind schema and data
psql -U postgres -d northwind -f northwind.sql

# 3. Verify the import
psql -U postgres -d northwind -c "SELECT COUNT(*) FROM products;"
```

### **Your First Steps**

1. **Clone this analytics repository**
   ```bash
   git clone https://github.com/yourusername/northwind-analytics-odyssey.git
   cd northwind-analytics-odyssey
   ```

2. **Set up the Northwind database** (see options above)

3. **Test your connection**
   ```sql
   -- Run this query to verify everything works
   SELECT 
       COUNT(*) as total_products,
       AVG(unit_price) as avg_price
   FROM products;
   ```
   Expected: ~77 products with average price around $28

4. **Start with Section 1, Task 1.1**
   - Open `01-data-discovery/explore-tables.sql`
   - Read the task descriptions
   - Write your queries
   - Run them and observe the results

5. **Track your progress**
   - Check off completed tasks in this README
   - Commit your solutions to your forked repo
   - Celebrate small wins! 🎉

---

## 💡 Learning Tips

| Tip | Why It Matters |
|-----|----------------|
| **Test on small data first** | Use `LIMIT 10` while developing – catch errors faster |
| **Comment your code** | Future you will thank present you |
| **Format for readability** | Indentation and line breaks = clarity |
| **Check for duplicates** | Use `COUNT(*)` after JOINs to verify correctness |
| **Use EXPLAIN** | Add `EXPLAIN ANALYZE` to understand query performance |
| **Break down complex queries** | Build CTEs step-by-step, test each part |

---

## 🎯 Success Metrics

You'll know you're progressing when you can:

- ✅ Write queries without constantly checking syntax references
- ✅ Explain what a query does in plain English to a non-technical person
- ✅ Debug queries by systematically testing each component
- ✅ Optimize slow queries using indexes and query restructuring
- ✅ Translate business questions into SQL logic automatically

---

## 🤝 Contributing

Found a better way to explain a concept? Have a creative task idea? **Contributions are welcome!**

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-task`)
3. Commit your changes (`git commit -m 'Add an amazing new task'`)
4. Push to the branch (`git push origin feature/amazing-task`)
5. Open a Pull Request

---

## 📜 License

This project is licensed under the MIT License – see the LICENSE file for details.

---

## 🙏 Acknowledgments

- The **Northwind Database** – A timeless teaching tool
- The SQL community for decades of shared knowledge
- Every learner who's ever struggled with JOINs and lived to tell the tale

---

## 📬 Questions or Stuck?

- Open an issue in this repository
- Tag it with `help-wanted` or `question`
- The community is here to help you succeed!

---

<div align="center">

**Ready to begin your odyssey?**

⭐ **Star this repo** to bookmark your journey

🍴 **Fork it** to make it your own

🚀 **Start with Task 1.1** and let the adventure begin!

---

*"Data is the new oil, but SQL is the refinery."*

</div>
