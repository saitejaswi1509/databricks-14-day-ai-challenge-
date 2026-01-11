📘 Day 3 – PySpark Transformations Deep Dive
Databricks 14-Day AI Challenge 🚀

This notebook is part of Day 3 of the Databricks 14-Day AI Challenge, where the focus is on building strong fundamentals in PySpark transformations through hands-on practice.

The notebook demonstrates how PySpark is used in real-world data engineering workflows to process, transform, and enrich large-scale datasets using distributed computing.

An e-commerce transactions dataset is used throughout this notebook to apply concepts such as UDFs, window functions, aggregations, rankings, and joins.

📚 Learnings
🔹 PySpark vs Pandas

<img width="1559" height="821" alt="image" src="https://github.com/user-attachments/assets/f4980186-2158-45ad-a2bd-cb0b13b595a9" />

Pandas operates on a single machine and is best suited for small to medium-sized datasets.

PySpark enables distributed processing across clusters, making it ideal for large-scale data.

PySpark uses lazy execution, allowing Spark to optimize transformations before executing them, improving performance and scalability.

🔹 Joins in PySpark 

Joins are a core concept in data engineering and are used to combine transactional data with aggregated or derived insights.

Why joins are important:

Enable feature enrichment by merging aggregated data back into raw event-level data.

Help model real-world relationships between datasets.

Commonly used in analytics pipelines and ML feature engineering.

Join types overview:

Inner Join – Returns only matching records from both datasets.

Left Join – Retains all records from the primary dataset (used in this notebook).

Right Join – Retains all records from the secondary dataset.

Outer Join – Retains all records from both datasets with nulls for missing matches.

🔹 Window Functions (Running Totals & Rankings)

Window functions allow calculations across related rows without reducing the number of rows, which makes them extremely powerful for analytics.

Used to compute running totals per user while preserving transaction-level detail.

Used to rank product categories by total revenue.

Widely applied in time-based analytics, customer behavior analysis, and ranking problems.

🔹 User-Defined Functions (UDFs)

User-Defined Functions (UDFs) allow custom logic to be applied when built-in Spark functions are not sufficient.

Used in this notebook to convert numerical Age values into meaningful age group categories.

Enable feature engineering directly within PySpark pipelines.

Should be used judiciously, as built-in Spark functions are more optimized than UDFs.

🛠️ Tasks Performed
✅ 1. Load Full E-commerce Dataset

Loaded a cleaned e-commerce transactions dataset into Databricks.

Inspected sample records to understand available attributes.

✅ 2. Create Derived Features using UDFs

Implemented a User-Defined Function to classify users into age groups:

young, middle_aged, senior, old

Added a new derived column age_group to enhance analytical usability.

✅ 3. Calculate Running Totals using Window Functions

Applied window functions to calculate cumulative purchase amounts per user.

Used a composite user identity (User_Name, Country, Age) to avoid incorrect aggregations.

Preserved transaction-level granularity while generating cumulative insights.

✅ 4. Rank Product Categories by Revenue

Aggregated transaction-level data to compute total revenue per product category.

Ranked product categories based on total revenue using window ranking functions.

Identified top-performing product categories across the dataset.

✅ 5. Perform Complex Joins for Data Enrichment

Joined aggregated product-level rankings back to the transaction-level dataset.

Used a LEFT JOIN to ensure all transactions were preserved.

Enriched each transaction with:

Product-level total revenue

Product revenue rank

📌 Key Takeaways

PySpark enables scalable data processing beyond single-machine limitations.

Window functions are powerful for cumulative metrics and ranking-based analysis.

Joins allow seamless enrichment of transactional data with derived features.

This notebook reflects real-world data engineering and analytics patterns.
