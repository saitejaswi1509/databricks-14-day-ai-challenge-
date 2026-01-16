### 📘 Day 8 – Unity Catalog & Data Governance  
**Databricks 14-Day AI Challenge**

## 📌 Overview
This notebook focuses on **Unity Catalog governance concepts** in Databricks, demonstrating how enterprise data platforms organize, secure, and share data using centralized governance mechanisms.

The goal of this exercise was to move beyond data processing and understand **real-world data security, access control, and governed data sharing**.

---

## 🧠 Concepts Covered
- Unity Catalog fundamentals
- Catalog → Schema → Table hierarchy
- Managed Delta tables
- Access control using GRANT / REVOKE
- Controlled data access using Views

---

## 🏗️ Architecture Implemented
The notebook follows a **Medallion Architecture** approach:

- **Bronze** – Raw event-level data  
- **Silver** – Cleaned and structured data  
- **Gold** – Business-ready, analytics-friendly data  

All layers are registered and governed using **Unity Catalog**.

---

## 🛠️ Hands-on Tasks Completed

### 1️⃣ Catalog & Schema Setup
- Created a catalog named `ecommerce`
- Created schemas:
  - `bronze`
  - `silver`
  - `gold`
- Established a clear hierarchical structure for governance

---

### 2️⃣ Delta Table Registration
- Created managed Delta tables:
  - `bronze.events`
  - `silver.events`
  - `gold.products`
- Verified data using SQL queries
- Ensured tables are centrally governed under Unity Catalog

---

### 3️⃣ Access Control (GRANT)
- Inspected existing permissions using `SHOW GRANTS`
- Granted **SELECT-only access** on `gold.products`
- Validated permissions using Unity Catalog metadata

This step demonstrates how data access is controlled at the table level to prevent unauthorized modifications.

---

### 4️⃣ Controlled Data Access Using Views
- Created a view `gold.top_products`
- Applied:
  - Column-level restriction (excluded sensitive columns)
  - Row-level filtering (`purchases > 10`)
- Granted SELECT access on the **view instead of the base table**

This reflects a **real-world best practice** for secure data sharing with business users.

---

## 🔐 Key Learnings
- Unity Catalog enables centralized data governance across teams
- Clear data hierarchy improves scalability and manageability
- GRANT/REVOKE ensures secure and controlled access
- Views are preferred over tables for safe data consumption
- Governance is as critical as data transformation in production systems

---

## ✅ Conclusion
This exercise highlights how **enterprise-grade data governance** is implemented in Databricks using Unity Catalog.  
It reinforces that effective data engineering is not just about building pipelines—but about ensuring **security, trust, and controlled access** to data.

---
