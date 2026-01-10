# 🚀 Day 02 – Apache Spark Fundamentals in Databricks

This notebook is part of the **Databricks 14-Day AI Challenge**, focused on building a strong foundation in **Apache Spark fundamentals** and understanding how Spark operates within the **Databricks platform** through hands-on practice.

The objective of **Day 2** was to understand Spark’s internal architecture, core abstractions, and execution model, while applying fundamental **PySpark DataFrame operations** on a real-world e-commerce dataset.

---

## 📚 Topics Covered

- ⚙️ **Spark Architecture**
  - Driver
  - Executors
  - DAG (Directed Acyclic Graph)
- 📊 **DataFrames vs RDDs**
- ⏳ **Lazy Evaluation in Apache Spark**
- 🧩 **Databricks Notebook Magic Commands**
  - `%python`
  - `%sql`
  - `%fs`
- 📥 Loading data into Spark DataFrames
- 🔍 Basic DataFrame operations:
  - `select()`
  - `filter()`
  - `groupBy()`
  - `orderBy()`

---

## 🛠️ Hands-on Tasks Performed

- 📁 Uploaded a sample **e-commerce transactions CSV dataset** (from Kaggle) into Databricks using **Data Ingestion**
- 📄 Read the dataset into a Spark DataFrame using **PySpark**
- 🧪 Explored the schema and displayed data in tabular format
- 🔄 Performed core DataFrame transformations and aggregations, including:
  - Selecting specific columns
  - Filtering records based on conditions
  - Grouping and aggregating transactional data
  - Ordering results to derive insights

---

## 🎯 Key Learning Outcomes

Through this notebook, I learned:

- How Spark’s **driver–executor architecture** enables distributed data processing
- Why **DataFrames are preferred over RDDs** for analytics and data engineering workloads
- How **lazy evaluation** allows Spark to optimize execution plans efficiently
- How Databricks notebooks enable a **seamless PySpark + SQL workflow**
- How to apply fundamental Spark transformations on **real-world datasets**

This exercise strengthened my understanding of **Spark internals** while reinforcing how **Databricks simplifies large-scale data processing**.

---

## 🧰 Tools & Technologies

- 🟣 Databricks Community Edition  
- 🔥 Apache Spark (PySpark)  
- 🧮 Spark SQL  

---

📌 This notebook represents **Day 2 progress** in my Databricks learning journey, guided by **Indian Data Club**, **Codebasics**, and **Databricks**.
