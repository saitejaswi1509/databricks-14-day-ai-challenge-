### 📅 Day 7 – Workflows & Job Orchestration | Databricks 14 Days AI Challenge | Phase 2
This notebook set focuses on building production-ready data pipelines using Databricks Jobs and multi-task workflows.

**📘 What I Learned**
* Difference between Databricks notebooks and Jobs
* How to build multi-task workflows (Bronze → Silver → Gold)
* Parameterizing notebooks using widgets
* Scheduling jobs with triggers
* Managing task dependencies and execution order
* End-to-end job orchestration using Databricks Workflows
 
**🏗️ Architecture Implemented**
  
Medallion Architecture Bronze (Raw Data)
 ↓
Silver (Cleaned & Standardized)
 ↓
Gold (Aggregated Business Metrics)

**Each layer is implemented as a separate notebook and orchestrated using a single multi-task Databricks Job.**

**🛠️ Hands-on Tasks Completed**

- Added parameter widgets to all notebooks
- Modularized Day 6 logic into separate Bronze, Silver, and Gold notebooks
- Created a multi-task Databricks Job
- Configured task dependencies
- Scheduled the workflow for daily execution
- Validated end-to-end execution and outputs

**⚙️ Technologies Used**
- Databricks
- PySpark
- Delta Lake
- Databricks Workflows & Jobs

**✅ Outcome**
- Successfully built and scheduled a production-style automated data pipeline following industry best practices.

- This marks the transition from interactive notebooks to fully orchestrated data engineering workflows.
