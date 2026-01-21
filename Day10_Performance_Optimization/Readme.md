### 📘 Day 10 – Performance Optimization | Databricks 14-Day AI Challenge

Day 10 focused on performance optimization techniques in Databricks.

- The goal was to understand how Spark executes queries, identify performance bottlenecks, and apply best practices to optimize large analytical workloads using Delta Lake features.

- This notebook demonstrates how performance improvements are designed, applied, and validated, rather than just relying on query runtime alone.

**📚 What I Learned**

**🔍 Query Execution Plans**

Learned how Spark converts SQL queries into physical execution plans using EXPLAIN FORMATTED.
This helps identify expensive operations such as full table scans, shuffles, and inefficient filters.

**📂 Partitioning Strategies**

Partitioning splits large tables into logical segments (for example, by date).
This enables partition pruning, significantly reducing the amount of data scanned during filtered queries.

**🧱 OPTIMIZE & ZORDER**

OPTIMIZE compacts small files into fewer large files to improve read efficiency.
ZORDER physically clusters related data to enable data skipping for frequently filtered columns.

**⚡ Caching Techniques**

Caching stores frequently accessed data in memory to reduce repeated disk I/O.
This is especially useful for iterative analysis and repeated queries in analytics workflows.

**🛠️ Hands-On Tasks Completed**

**1️⃣ Analyze Query Plans**

Used EXPLAIN FORMATTED to understand scans, filters, and execution stages

**2️⃣ Partition Large Tables**

Created a partitioned Delta table on Transaction_Date to enable partition pruning

**3️⃣ Apply ZORDER**

Applied OPTIMIZE with ZORDER on frequently filtered columns such as user and category

**4️⃣ Benchmark Improvements**

- Compared query runtimes before and after optimization

- Evaluated performance impact while accounting for dataset size and execution behavior

**📊 Summary**

- Partitioning improved performance for date-based queries through partition pruning

- ZORDER did not significantly reduce runtime on a small dataset, which is expected behavior

- Performance optimizations show clear benefits at scale, even if improvements are subtle on smaller datasets

- Understanding execution plans is critical for building scalable, production-ready data pipelines

**🎯 Key Takeaway**

Performance optimization is not just about faster queries today, but about designing data models that scale efficiently as data volume grows.
