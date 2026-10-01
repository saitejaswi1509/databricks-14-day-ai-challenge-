# Cursor dashboard

Static Databricks AI/BI (Lakeview) dashboard over `ecommerce.gold.products`, built from Cursor and stored here as a Databricks Asset Bundle.

Live dashboard (workspace): https://dbc-36ba8347-bc42.cloud.databricks.com/dashboardsv3/01f1bd9e986916f6afa6e31bc6e0e1e0/published?w=7474656595007259

Source bundle repo (Cursor git): https://cursor.com/codebase/saitejaswi-kondapally/ecommerce-gold-dashboard

## What it shows

| Chart | Question it answers |
|---|---|
| Pie · number of products | How many products, by name (one slice each) |
| Bar · revenue ranges | How many products sit in `< $10k`, `$10k–$20k`, and `$20k+` |
| Bar · most purchases | Ranked purchase counts |
| Bar · revenue by product | Direct revenue comparison |

## Deploy from this folder

```bash
cd cursordashboard
export DATABRICKS_CONFIG_PROFILE=<your-profile>
databricks bundle validate --strict --target dev
databricks bundle deploy --target dev --auto-approve
```

Token/OAuth needs **SQL**, **Unity Catalog**, **dashboards**, and **workspace** scopes (or **all-apis**).
