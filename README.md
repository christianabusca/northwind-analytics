# 📊 Northwind E-Commerce Analytics

> SQL-based sales analytics dashboard built on the Northwind PostgreSQL database

[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![SQL](https://img.shields.io/badge/SQL-Analytics-blue?style=flat-square)](https://github.com)

---

## 📖 About

Personal analytics project exploring e-commerce data patterns using SQL. Built on the [Northwind PostgreSQL database](https://github.com/pthom/northwind_psql) with queries progressing from basic exploration to advanced business intelligence.

---

## 🗂️ Project Structure

### **Section 1: Data Exploration**
Understanding the data foundation
- Explore individual tables (products, orders, customers)
- Filter and sort operations
- Pattern matching with LIKE and wildcards

### **Section 2: Aggregation & Grouping**
Summarizing data to find patterns
- Basic aggregations (AVG, SUM, COUNT)
- GROUP BY fundamentals
- Filtering grouped data with HAVING

### **Section 3: JOINs**
Connecting related data across tables
- Two-table joins (products + categories, orders + customers)
- Multi-table joins (4+ tables)
- LEFT JOINs to find missing data

### **Section 4: Business Analytics**
Answering real business questions
- **Revenue Analysis**: Order totals, monthly trends, top customers
- **Product Performance**: Rankings, best sellers, category contributions
- **Customer Insights**: Segmentation, lifetime value, retention rates
- **Time-Based Analysis**: Running totals, moving averages, growth rates

### **Section 5: Advanced Queries**
Complex analytical challenges
- **Executive Dashboards**: Multi-metric KPI queries
- **Data Quality Checks**: Validation and error detection
- **Complex Business Questions**: Retention rates, basket affinity, seasonality

### **Section 6: Reporting**
Production-ready output formatting
- Pivot tables and cross-tabs
- Number formatting and NULL handling
- Summary reports with subtotals (ROLLUP, CUBE)

### **Final Project: Executive Sales Dashboard**
Comprehensive dashboard including:
- KPI summary (revenue, orders, AOV, YoY growth)
- Top performers (products, customers, employees)
- Trend analysis (monthly revenue, moving averages)
- Geographic breakdown
- Inventory alerts

---

## 🚀 Setup

**Database:** [pthom/northwind_psql](https://github.com/pthom/northwind_psql)

```bash
# Clone and start the database
git clone https://github.com/pthom/northwind_psql.git
cd northwind_psql
docker-compose up -d

# Connection: localhost:5432, database: northwind, user/pass: postgres
```

---

## 📊 Key Analytics Areas

### Revenue Analysis
- Total revenue calculations: `quantity × unit_price × (1 - discount)`
- Monthly/yearly revenue trends
- Top revenue-generating orders and customers
- Category-level performance

### Product Performance
- Product rankings by quantity sold and revenue
- ABC classification (Pareto analysis)
- Inventory turnover rates
- Best sellers per category

### Customer Intelligence
- Customer segmentation (High/Medium/Low value)
- Lifetime value calculations
- Retention and cohort analysis
- Average order value per customer

### Time-Series Analysis
- Running totals by date
- Month-over-month growth rates
- 3-month moving averages
- Seasonal trend detection

### Geographic Insights
- Revenue by country/region
- Market penetration metrics
- Regional performance comparison

---

## 🛠️ SQL Techniques Used

**Fundamentals**
- SELECT, WHERE, ORDER BY, LIMIT
- Filtering (comparison operators, IN, BETWEEN, LIKE)
- Date functions and arithmetic

**Aggregations**
- COUNT(), SUM(), AVG(), MIN(), MAX()
- GROUP BY with multiple dimensions
- HAVING for post-aggregation filtering

**JOINs**
- INNER JOIN for related data
- LEFT JOIN for missing data detection
- Multi-table joins (4+ tables)
- Table aliases

**Advanced SQL**
- Window functions (ROW_NUMBER, RANK, NTILE, LAG, LEAD)
- Common Table Expressions (CTEs)
- CASE statements for segmentation
- PARTITION BY for grouped calculations
- Subqueries and nested queries

**Reporting**
- CROSSTAB for pivot tables
- ROLLUP and CUBE for subtotals
- ROUND() and formatting functions
- COALESCE() for NULL handling

---

## 💡 Query Development Tips

- **Test incrementally**: Use `LIMIT 10` while developing
- **Comment your code**: Use `--` for clarity
- **Format for readability**: Indentation and line breaks
- **Verify joins**: Use `COUNT(*)` to check for duplicates
- **Analyze performance**: Add `EXPLAIN ANALYZE` before queries

---

## 📝 License

MIT License

---

## 🙏 Credits

Database: [pthom/northwind_psql](https://github.com/pthom/northwind_psql)
