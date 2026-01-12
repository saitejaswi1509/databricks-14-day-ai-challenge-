### 📘 Day 4 | Delta Lake Introduction | Databricks 14-Day AI Challenge

On Day 4, I focused on understanding Delta Lake fundamentals and applying them hands-on using PySpark and SQL. 
This notebook covers how Delta Lake improves reliability, data quality, and consistency in real-world data pipelines.

📚 What I Learned

What is Delta Lake?
Delta Lake is an open-source storage layer that adds reliability, versioning, and ACID guarantees on top of data lakes.

ACID Transactions
Learned how Delta Lake ensures atomicity, consistency, isolation, and durability for concurrent reads and writes.

Schema Enforcement
Understood how Delta Lake prevents incompatible schema writes, ensuring data quality and protecting tables from corrupt data.

Delta vs Parquet
Compared Delta Lake and Parquet to understand why Delta is preferred for production pipelines (ACID, time travel, schema control).

🛠️ Hands-On Tasks Completed

1️⃣ Convert Source Data to Delta Format

Loaded existing e-commerce transaction data from the Databricks catalog

Converted the data into a managed Delta table using PySpark

2️⃣ Create Delta Tables (PySpark & SQL)

Created a Delta table using PySpark (saveAsTable)

Created another Delta table using SQL (CREATE TABLE USING DELTA AS SELECT)

3️⃣ Test Schema Enforcement

Attempted to insert data with an incompatible schema

Verified that Delta Lake blocked the write, confirming schema enforcement works as expected

4️⃣ Handle Duplicate Inserts

Identified duplicate records using a business key

Removed duplicates using dropDuplicates()

Overwrote the Delta table with clean data

Verified duplicates were removed using SQL aggregation checks

✅ Key Takeaways

Delta Lake adds production-grade reliability to data lakes

Schema enforcement prevents bad data from entering tables

Duplicate handling can be managed cleanly before inserts

Delta tables work seamlessly with both PySpark and SQL
