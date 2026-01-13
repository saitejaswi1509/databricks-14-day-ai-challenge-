## 🚀 Day 05 – Delta Lake Advanced | Databricks 14-Day AI Challenge

This notebook is part of the Databricks 14-Day AI Challenge (Phase 2) and focuses on advanced Delta Lake concepts that are essential for building reliable, scalable, and production-ready data pipelines.

The objective of Day 5 was to move beyond basic Delta Lake usage and gain a deep understanding of how Delta handles incremental data changes, historical tracking, performance optimization, and storage management, all through hands-on implementation.

**📚 Topics Covered**
**⏳ Delta Lake Time Travel (Version History)**

* Understanding how Delta Lake maintains a transaction log

* Querying previous versions of a table

* Auditing and validating historical data changes

**🔁 MERGE Operations (Upserts)**

* Performing incremental updates using MERGE

* Handling updates and inserts in a single operation

* Using a business key (Transaction_ID) for idempotent processing

**⚡ OPTIMIZE & ZORDER**

* Understanding the small-file problem in Delta tables

* File compaction using OPTIMIZE

* Improving query performance with ZORDER for data skipping

**🧹 VACUUM for Cleanup**

* Managing old and unused data files

* Understanding retention periods

* Balancing storage cleanup and time travel safety

**🛠️ Hands-On Tasks Performed**
**📥 Dataset Loading & Delta Table Creation**

Loaded an existing e-commerce transactions dataset. Converted the dataset into a managed Delta table. Enabled ACID transactions, schema enforcement, and versioning

**🔄 Incremental Data Processing**

Created an incremental batch simulating real-world data ingestion

Included:

Existing Transaction_IDs → UPDATE

New Transaction_IDs → INSERT

**🔀 Incremental MERGE (Upserts)**

Applied MERGE to update existing records and insert new ones. Ensured that No duplicate data and Reliable incremental pipeline behavior

**🕒 Time Travel Analysis**

Explored Delta table version history. Identified the version where MERGE occurred.Queried records before and after the update to validate changes

**⚡ Performance Optimization**

Compacted multiple small files into fewer optimized files. Applied ZORDER on Transaction_ID to improve query performance

**🧹 Storage Cleanup**

Executed VACUUM to remove obsolete files. Retained recent versions to preserve time travel functionality

**🎯 Key Learning Outcomes**

**Through this notebook, I learned:**

* How Delta Lake supports reliable incremental data pipelines

* How time travel enables auditing, debugging, and rollback

* Why MERGE is critical for real-world data engineering workflows

* How OPTIMIZE and ZORDER significantly improve query performance

* How VACUUM manages storage without immediately deleting historical versions

* The importance of retention policies in production environments

**🧰 Tools & Technologies Used**

🟣 Databricks Community Edition

🔺 Delta Lake

🔥 Apache Spark (PySpark)

🧮 Spark SQL

**📌 Summary**

This notebook represents Day 5 progress in my Databricks learning journey, where I implemented advanced Delta Lake features including incremental MERGE, time travel validation, performance optimization, and storage cleanup. These concepts form the foundation for building production-grade data lakes and lakehouse architectures.
