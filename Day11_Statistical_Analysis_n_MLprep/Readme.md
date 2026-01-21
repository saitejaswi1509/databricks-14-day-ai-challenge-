### 📘 Day 11 — Statistical Analysis & ML Prep | Databricks 14-Day AI Challenge

Day 11 focused on building a strong foundation for ML by understanding the dataset statistically, validating assumptions through weekday vs weekend analysis, checking correlations, and creating simple ML-ready features.

**📚 What I Learned**
**📊 Descriptive Statistics**

How to summarize numeric columns using key statistical measures (count, mean, std, quartiles) and validate data quality (null checks) before deeper analysis.

**🧪 Hypothesis Testing (Weekday vs Weekend)**

How to frame a business question as a hypothesis and validate it by comparing group-level metrics (weekday vs weekend behavior).

**🧬 A/B Test Design**

How experiments are designed using control vs variant groups, selecting the right metric, and avoiding bias through randomization and sufficient sample size.

**🔧 Feature Engineering**

How to convert raw transaction columns into meaningful, ML-ready features using time-based and behavior-based signals (without overengineering).

**🛠️ Hands-On Implementation**

**1) Load the transactions table**

- Loaded default.ecommerce_transactions into a Spark DataFrame

- Displayed sample rows to validate data availability and column structure

- Output: Quick preview of transactions for sanity check.

**2) Task 1 — Statistical summaries + data quality checks**

- Performed descriptive statistics on key numeric columns: Purchase_Amount,Age

- Also computed useful validation metrics: Total rows,Transaction counts and distinct transaction IDs

- Null checks on Purchase_Amount and Transaction_Date

- Quartile summary (Q1, Q3) for Purchase_Amount using percentile_approx

This step helps understand distribution/spread, detect missing values, and prepare the dataset for reliable analysis/ML.

**3) Task 2 — Weekday vs Weekend hypothesis check**

Created time-based flags from Transaction_Date:

- day_of_week (1 = Sunday n 7 = Saturday)

- is_weekend (Saturday/Sunday)

- Compared weekday vs weekend using: Total transaction count, Average purchase amount, Total revenue, Standard deviation of purchase amount

A simple but strong statistical comparison to validate whether weekend behavior differs from weekdays using real transaction data.

**4) Task 3 — Correlation analysis**

- Computed correlation to understand relationships between numeric variables: Purchase_Amount vs Age

Correlation helps identify feature relationships and potential predictors for ML (and also highlights multicollinearity risks).

**5) Task 4 — Feature Engineering for ML prep** 

Engineered minimal, non-redundant features:

✅ Time pattern: day_of_week

✅ Skew handling: purchase_log = log(Purchase_Amount + 1)

✅ Customer behavior (recency): days_since_last_purchase

**🎯 Key Takeaways**

- Statistical summaries are essential to understand dataset health before modeling

- Simple hypothesis comparisons can reveal meaningful business behavior patterns

- Correlation checks help understand numeric relationships early

- Clean, minimal feature engineering (time + log + recency) prepares data effectively for ML
