### 📘 Day 6 — Medallion Architecture | Phase 2: Data Engineering | Databricks 14 Days AI Challenge

This notebook is part of **Phase 2 (Data Engineering)** of the **Databricks 14 Days AI Challenge**, where the focus is on building real-world, production-style data pipelines using the **Medallion Architecture** on Databricks.

**🎯 What I Learned Today**
**🥉🥈🥇 Medallion Architecture**

* Understood the Bronze → Silver → Gold layered architecture pattern used in modern data engineering.

* Learned how separating raw, cleaned, and aggregated data improves reliability, scalability, and maintainability.

* Gained clarity on the responsibility of each layer instead of mixing transformations.

**✅ Best Practices for Each Layer**

- **Bronze:** Store raw data as-is with ingestion metadata, no business logic.

- **Silver:** Clean, standardize, validate, and prepare trusted data for reuse.

- **Gold:** Create business-ready aggregates optimized for analytics and dashboards.

**🔁 Incremental Processing Patterns**

* Learned why reprocessing full data every time is inefficient.

* Understood how incremental logic, idempotent pipelines, and upsert-friendly design make pipelines production-ready.

**🛠️ Hands-On Tasks Completed**
**1️⃣ Designed a 3-Layer Architecture**

* Created separate schemas for **Bronze, Silver, and Gold** layers.

* Structured the pipeline to clearly reflect industry-standard Medallion Architecture.

**2️⃣ Built the Bronze Layer (Raw Ingestion)**

* Ingested source transaction data into the Bronze layer.

* Preserved data exactly as received from the source.

* Added ingestion metadata (ingestion timestamp, source name) for traceability.

* Ensured Bronze acts as a raw, replayable source of truth.

**3️⃣ Performed Bronze Validation / Data Profiling**

* Checked row counts, uniqueness of transaction IDs, and basic null/invalid checks.

* Used Bronze only for observing and understanding data quality, not for fixing issues.

* Clearly separated data profiling (Bronze) from data cleaning (Silver).

**4️⃣ Built the Silver Layer (Cleaned & Trusted Data)**

* Applied data quality rules such as valid purchase amount checks.

* Standardized string columns to ensure consistency.

* Added reusable derived columns (year and month) to support downstream analytics.

* Ensured deduplication safety to make pipelines idempotent.

* Created a trusted, reusable dataset that Gold can safely depend on.

**5️⃣ Built the Gold Layer (Business Aggregates)**

Created business-ready aggregated tables from Silver data.

Built KPIs such as:

- Daily revenue metrics

- Revenue by product category

- Revenue by country

Optimized Gold tables for direct consumption by BI tools and analytics queries if needed.

**🧠 Key Takeaways**
* **Bronze** = raw truth (observe, don’t modify)

* **Silver** = trusted data (clean once, reuse everywhere)

* **Gold** = business answers (aggregated, optimized, dashboard-ready)

* Clear separation of layers makes pipelines easier to debug, scale, and explain in interviews.

**📌 Outcome:**
By the end of Day 6, I successfully built an end-to-end **Medallion Architecture pipeline** that mirrors how data engineering pipelines are designed in real-world Databricks environments.
