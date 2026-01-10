Day 02 – Apache Spark Fundamentals in Databricks

This notebook is part of the Databricks 14-Day AI Challenge, focused on building a strong understanding of Apache Spark fundamentals and how Spark operates within the Databricks platform through hands-on practice.

The objective of Day 2 was to understand how Spark works internally, explore core Spark abstractions, and apply fundamental DataFrame operations on a real-world e-commerce dataset.

What I learned today: 
Spark architecture (Driver,Executors and DAG (Directed Acyclic Graph))
Differences between DataFrames and RDDs
Lazy evaluation in Apache Spark
Using Databricks notebook magic commands: %python, %sql and %fs

Loading data into Spark DataFrames
Basic DataFrame operations: select() filter() groupBy() orderBy()

Hands-on Tasks Performed

Uploaded a sample e-commerce transactions CSV dataset (Kaggle) into Databricks using Data Ingestion.
Read the dataset into a Spark DataFrame using PySpark
Explored schema and displayed data in tabular format

Performed core DataFrame transformations and aggregations like:

Selecting specific columns

Filtering records based on conditions

Grouping and aggregating data


Key Learning Outcomes

Through this notebook, I learned:

How Spark’s driver–executor architecture enables distributed data processing

Why DataFrames are preferred over RDDs for analytics and data engineering

How lazy evaluation allows Spark to optimize execution plans

How Databricks notebooks support a seamless PySpark + SQL workflow

How to apply basic Spark transformations on real-world datasets

This exercise strengthened my understanding of Spark internals while reinforcing how Databricks simplifies large-scale data processing.

Tools & Technologies

Databricks Community Edition

Apache Spark (PySpark)

Spark SQL

📌 This notebook represents Day 2 progress in my Databricks learning journey, guided by Indian Data Club, Codebasics, and Databricks.
