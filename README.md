### Hi, I'm Zhengtao (Tony) Li

Data engineer and data scientist finishing an M.S. in Applied Data Science at the **University of Chicago** (Dec 2026), with a B.S. in Statistics and Analytics from **UNC-Chapel Hill**.
I build data pipelines, warehouses and analytics on real public data, at real scale. Each project ends in a decision, and the numbers that didn't work out are reported too.

**Data engineering**

- **[Chicago 311 Warehouse](https://github.com/TonyLee-99/chicago-311-warehouse)**: an incremental warehouse for all 14.9M Chicago 311 service requests (Python, SQL, dbt, DuckDB, Airflow). Immutable Parquet landing, dbt snapshots for change history, Kimball marts and write-audit-publish. Every publish is reconciled against the City's own counts: 302 of 304 month × status cells match exactly and the other 2 are explained. The audit gate once blocked a half-built publish that was missing 3,096,285 requests.
- **[Bluesky Event Lakehouse](https://github.com/TonyLee-99/bluesky-event-lakehouse)**: a streaming lakehouse on Bluesky's live firehose (Kafka/Redpanda, Spark Structured Streaming, Apache Iceberg). It captured 11.5M real events in 6.8 hours. A second independent read of the source found 0 missing events, five chaos tests (kill -9, broker restart, duplicate replay) ended with 0 lost and 0 duplicated, and 368,881 deletes were applied 100%. A load test sustained 41,600 events/s, 89× the live rate.

**Analytics and ML**

- **[Experimentation Platform](https://github.com/TonyLee-99/experimentation-platform)**: a warehouse-native A/B-testing engine (CUPED/CUPAC, SRM and covariate-balance gates, sequential tests). It found an assignment imbalance (z = 33) in Criteo's 14M-user ad experiment that the standard SRM check misses.
- **[PPP Duplicate Loan Detection](https://github.com/TonyLee-99/ppp-duplicate-loan-detection)**: entity resolution on 8.6M first-draw PPP loans that share no business ID. It flags 36,288 businesses holding 2+ loans ($1.05B beyond their first loan). Their loans charge off at 13.4%, against 6.2% for all first-draw loans.
- **[Marketplace Analytics](https://github.com/TonyLee-99/marketplace-analytics)** ([live dashboard](https://tonylee-99.github.io/marketplace-analytics/dashboard/)): a dbt + DuckDB warehouse, 17 governed KPIs and an executive dashboard on 99K real Olist orders. Most of the "late delivery costs 1.9 stars" effect is survey timing: on reviews written after delivery, the penalty is −0.51★.
- **[Analytics Agent](https://github.com/TonyLee-99/analytics-agent)**: a text-to-SQL agent with read-only guardrails, confidence-based abstention and a governed metric layer. BIRD execution accuracy rises from 62.6% to 73.2%. Business-metric questions go from 14/30 to 29/30 once metrics are compiled.
- **[Venture AI OS](https://github.com/TonyLee-99/venture-ai-os)**: an AI diligence system for an early-stage AI × digital-assets fund. Every memo claim must cite a stored source, and a blind critic from a second model family rated only 30% of drafted claims fully supported. It also includes a point-in-time screening backtest.
- **[Specialty Infusion FP&A](https://github.com/TonyLee-99/specialty-infusion-fpa)**: a buy-and-bill margin engine and 2027 scenario plan (Excel with 1,757 live formulas, plus a Power BI model) on public CMS data. After sequestration and bad debt, Medicare's drug margin is about 1.6%. The 2028 exposure is white bagging, not drug price negotiation.

**Also**: [Virtual Engineer](https://github.com/TonyLee-99/uchicago-virtual-engineer-capstone) is my UChicago capstone (team of 4, Office of the CTO): LLM-assisted alarm triage for campus building automation on BigQuery and Google Cloud.
Coursework: [churn prediction](https://github.com/TonyLee-99/data-science-projects), [MLOps with MLflow and Feast](https://github.com/TonyLee-99/mlops-pipeline-mlflow-feast), [BART news summarization](https://github.com/TonyLee-99/ML2-Final-Project), [data versioning with DVC and dbt](https://github.com/TonyLee-99/data-versioning-project).

**Tools:** Python, SQL (DuckDB, BigQuery), dbt, Airflow, Spark (incl. Structured Streaming), Kafka, Apache Iceberg, Terraform, Docker, GitHub Actions · pandas, scikit-learn, LightGBM, PyTorch, R · Tableau, Power BI, Excel

[LinkedIn](https://www.linkedin.com/in/zhengtaoli) · zhengtaoli2024@gmail.com
