### 📊 Day 9 – SQL Analytics & Dashboards | Databricks 14-Day AI Challenge | Phase 3: Advanced Analytics

Day9 focused on using SQL for advanced analytics and converting query results into business-ready dashboards using Databricks SQL.

📘 **All about my learnings:**

**🔹 SQL Warehouses**

- Learned how Databricks SQL Warehouses act as dedicated compute for running analytical SQL queries.

- Understood how serverless SQL warehouses enable fast, scalable, and BI-friendly analytics.

**🔹 Complex Analytical Queries**

- Used CTEs (WITH clauses) to structure complex logic clearly.

- Applied window functions such as moving averages and percentile-based ranking.

- Performed category-level and customer-level aggregations for business insights.

**🔹 Dashboard Creation**

- Built dashboards using Databricks SQL Dashboards (new UI).

- Learned how datasets, visual tiles, and layouts work together.

- Designed dashboards focused on clarity and decision-making.

**🔹 Visualizations & Filters**

- Created line charts, bar charts, tables, and pie charts.

- Understood when to use tables vs charts for multi-metric analysis.

- Explored dashboard filters and scheduling concepts (implemented later).

**🛠️ Tasks & Hands-On Implementation:**

**1️⃣ Create SQL Warehouse**

- Used the Serverless Starter SQL Warehouse available in Databricks Free Edition.

- Started and reused the warehouse for all analytical queries and dashboard tiles.

**2️⃣ Write Analytical Queries**

🔹 Revenue Trend with 7-Day Moving Average

- Aggregated daily revenue.

- Used a window function to calculate a rolling 7-day moving average.

- Helped smooth daily fluctuations and identify trends.

Concepts used:
CTE, SUM(), AVG() OVER, ROWS BETWEEN

**🔹 Top Product Categories by Revenue**

- Grouped transactions by product category.

- Calculated total revenue per category.

- Ranked categories to identify top-performing segments.

Business insight:
Which product categories contribute the most revenue.

**🔹 Category Performance Summary (Funnel-Style Table)**

- Calculated: Total purchases, Unique customers , Total revenue per category

- Used a table visualization to compare multiple KPIs together.

- Why table..? : Multiple metrics are easier to compare side-by-side than in a single chart.

**🔹 Customer Segmentation (VIP / Loyal / Regular)**

- Aggregated customer purchase frequency and total spend.

- Used NTILE window function to create percentile-based customer tiers.

- Ensured a balanced and realistic distribution of customers.

- Customer tiers logic:

Top spenders → VIP

Mid spenders → Loyal

Lower spenders → Regular

**3️⃣ Build SQL Analytics Dashboard**

- Created Day 9 – SQL Analytics Dashboard with the following visuals:

📈 Revenue Trend with 7-Day Moving Average (Line Chart)

📊 Top Categories by Revenue (Bar Chart)

📋 Category Performance Summary (Table)

🥧 Customer Distribution by Tier (Pie Chart)

- Dashboard layout was designed for: Trend analysis,  Category comparison and Customer segmentation insights

<img width="3570" height="1914" alt="image" src="https://github.com/user-attachments/assets/3878c1b9-1b23-4f9f-895f-43fbf244aab6" />

**4️⃣ Filters & Schedule Refresh**

- Learned how dashboard filters can be applied across datasets (date, category, country).

- Understood scheduled refresh for production dashboards.

- Filters and scheduling explored conceptually (kept minimal for clarity at this stage).

**🎯 Key Takeaways**

- SQL is not just for querying data, but for analytics and storytelling.

- Window functions are powerful tools for trend analysis and segmentation.

- Dashboards bridge the gap between raw data and business decisions.

- Clean design and correct visualization choices matter as much as the query logic.
