### 📘 Day 13: Model Comparison & Feature Engineering | Databricks 14-Day AI Challenge

This notebook focuses on building a complete Spark ML workflow to train multiple models, compare their performance using MLflow, and select the best model based on evaluation metrics. The emphasis is on reusability, fairness in comparison, and production-ready design.

**📚 What I Learned**

**Training multiple models**

Learned why training more than one algorithm is essential to avoid bias and to identify the most reliable model for a given dataset.

**Hyperparameter tuning**

Understood how model parameters (such as tree depth, number of trees, and regularization) impact performance and model complexity.

**Feature importance**

Explored how different models rely on features differently and how understanding feature impact improves interpretability and business trust.

**Spark ML Pipelines**

Learned how to use Spark ML Pipelines to standardize preprocessing, feature engineering, and model training into a single reusable workflow.

**🛠️ Hands-On Implementation**
**Step 1: Load Source Dataset**

Loaded the raw e-commerce transactions table from Databricks to begin the ML workflow.

**Step 2: Customer-Level Feature Engineering**

Aggregated transaction-level data to customer level to derive meaningful features such as:

- Transaction count

- Total spend

- Average spend

- Demographic attributes (Age, Country)

This ensured the prediction task was aligned with customer behavior, not individual transactions.

**Step 3: Define Spending Tiers (Target Variable)**

Calculated 33rd and 66th percentile thresholds on total customer spend and labeled users into:

- Low

- Medium

- High spending tiers

This transformed the problem into a multi-class classification task.

**Step 4: Train–Test Split**

Split the dataset into training and testing sets to evaluate model generalization fairly.

**Step 5: MLflow Experiment Setup**

Initialized an MLflow experiment to track:

- Model runs

- Parameters

- Evaluation metrics

This enabled transparent and reproducible model comparison.

**Step 6: Build a Reusable Spark ML Pipeline**

Created a single preprocessing pipeline that included:

- Label encoding for the target variable

- Encoding of categorical features

- Feature vector assembly

The same preprocessing steps were reused across all models to ensure a fair comparison.

**Step 7: Train Multiple Models**

Using the same pipeline, trained three different models:

- **Logistic Regression (baseline linear model)** BEST MODEL💥
  
- Random Forest (non-linear, tree-based model)

- Naive Bayes (probabilistic baseline)

**Step 8: Track and Compare Metrics in MLflow**

Evaluated all models using:

- F1-score

- Accuracy

Compared model performance directly in the MLflow UI using built-in visualizations.

<img width="3560" height="1946" alt="image" src="https://github.com/user-attachments/assets/5b184da8-b322-4454-94d3-e592339e7594" />


**Step 9: Select the Best Model**

Based on MLflow metric comparison, selected the best-performing model using F1-score as the primary criterion.

<img width="3574" height="2060" alt="image" src="https://github.com/user-attachments/assets/40119426-c7d3-45c7-bf60-8f478e1ff82b" />


**✅ Key Outcome**

- Successfully trained and compared three ML models using Spark ML

- Built a clean, reusable ML pipeline

- Used MLflow UI for transparent comparison

- Selected the best model based on objective metrics

This exercise reinforced that machine learning is not just about training models, but about systematic comparison and evaluation.
