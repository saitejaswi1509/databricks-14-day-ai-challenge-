# 📘 Day 12 | MLflow Basics | Databricks 14-Day AI Challenge

This notebook focuses on understanding the **fundamentals of MLflow** by tracking machine learning experiments in a structured and reproducible way. 

The objective of Day 12 was to learn how to log experiments, models, and metrics, and compare multiple model runs using MLflow UI.

---

## 🎯 Objective
- Learn how MLflow helps manage the machine learning lifecycle
- Track experiments instead of relying on scattered notebook outputs
- Compare multiple model runs objectively

---

## 📘 What I Learned

### 🔹 MLflow Components
- **Tracking**: Records parameters, metrics, and artifacts for each run  
- **Models**: Provides a standard way to save and load trained models  
- **Registry**: Manages model versions and lifecycle stages (conceptual)  
- **MLflow UI**: Visual interface to explore and compare experiments  

---

### 🔹 Experiment Tracking
- Difference between **Experiment** and **Run**
- How each model training attempt is stored as a run
- Importance of logging parameters and metrics for reproducibility

---

### 🔹 Model Logging
- Logging trained models as MLflow artifacts
- Associating models with their parameters and metrics
- Making experiments easier to reproduce and audit

---

### 🔹 MLflow UI
- Viewing all runs under an experiment
- Comparing multiple runs side by side
- Analyzing performance differences using metrics

---

## 🛠️ Hands-On Tasks

### 1️⃣ Train Simple Regression Model
- Prepared features and target variable from transactional data
- Trained a baseline **Linear Regression** model

### 2️⃣ Log Parameters, Metrics, and Model
- Logged model details and feature set
- Logged evaluation metric (R² score)
- Saved trained model using MLflow

### 3️⃣ Train Second Model with Additional Feature
- Added an extra feature (`is_weekend`)
- Trained a second regression model
- Logged as a separate MLflow run

### 4️⃣ Compare Runs in MLflow UI
- Opened MLflow UI
- Compared multiple runs side by side
- Analyzed how feature changes impacted model performance
- Identified the better-performing run using metrics

<img width="1789" height="1028" alt="Screenshot 2026-01-21 at 6 44 25 PM" src="https://github.com/user-attachments/assets/8b0acba9-2d41-4aba-89c1-9057b8c93ebb" />


---

## ✅ Key Takeaways
- MLflow helps track ML experiments systematically
- Multiple model runs can be compared objectively
- Experiment tracking improves clarity and reproducibility
- MLflow is essential for real-world ML and MLOps workflows

---

📌 *Note: The focus of this notebook is on MLflow fundamentals and experiment tracking rather than model accuracy or optimization.*

---

## 🚀 Challenge Progress
This notebook is part of the **Databricks 14-Day AI Challenge**, aimed at building strong foundations in data engineering, analytics, and machine learning on Databricks.

