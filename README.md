### Hi, I'm Zhengtao (Tony) Li

AI engineer, data engineer and data scientist finishing an M.S. in Applied Data Science at the **University of Chicago** (Dec 2026), with a B.S. in Statistics and Analytics from **UNC-Chapel Hill**.
I build data pipelines, warehouses and analytics on real public data, at real scale. Each project ends in a decision, and the numbers that didn't work out are reported too.

**AI agents**

- **[Analytics Agent v2](https://github.com/TonyLee-99/analytics-agent)**: a permission-aware Slack copilot over 157 City documents and a Postgres warehouse of 4.0M Chicago 311 requests, with document ACLs and row-level security enforced per user. A 40-attack red team leaked 0 times, and it answers 93% of 30 questions correctly vs 27% for docs-only RAG.
- **[Invoice Posting Agent](https://github.com/TonyLee-99/invoice-posting-agent)** ([demo](https://tonylee-99.github.io/invoice-posting-agent/demo/)): LLM-assisted accounts payable in TypeScript that must never double-post: the LLM extracts fields (F1 0.94), and posting to QuickBooks is deterministic and idempotent. Across 300 chaos seeds with 2,803 injected faults no invoice was lost; with the defences off, 86 of 100 seeds double-posted.
- **[Support Agent Evals](https://github.com/TonyLee-99/support-agent-evals)**: a customer-support agent and its eval flywheel, refereed by Sierra's tau2-bench retail. It reaches 85% pass^1 vs 70% for the default agent on a frozen 10-task split (small sample, with CIs), and failed conversations become CI regression gates.

**Data engineering**

- **[Provider 360 Lakehouse](https://github.com/TonyLee-99/provider-360-lakehouse)**: a PySpark + Delta Lake pipeline, orchestrated with Dagster, that conforms 3 CMS sources (Open Payments, Medicare Part D, NPPES; 73.3M rows) into a master table of 1.66M providers. CMS republications are applied with a guarded MERGE that matches CMS's own change labels on 100% of records, and payments reconcile to CMS totals to the cent ($3.42B).
- **[Chicago 311 Warehouse](https://github.com/TonyLee-99/chicago-311-warehouse)**: an incremental warehouse for all 14.9M Chicago 311 requests (dbt snapshots, Kimball marts, write-audit-publish, Airflow). Every publish is reconciled to the City's counts (302 of 304 cells exact, 2 explained), and the audit gate once blocked a publish missing 3.1M rows.
- **[Bluesky Event Lakehouse](https://github.com/TonyLee-99/bluesky-event-lakehouse)**: a streaming lakehouse on Bluesky's live firehose (Kafka/Redpanda, Spark Structured Streaming, Iceberg) that captured 11.5M events. An independent replay found 0 missing, and five chaos tests ended with 0 lost and 0 duplicated.

**Analytics and ML**

- **[Experimentation Platform](https://github.com/TonyLee-99/experimentation-platform)**: a warehouse-native A/B-testing engine (CUPED/CUPAC, SRM and covariate-balance gates, sequential tests). It found an assignment imbalance (z = 33) in Criteo's 14M-user ad experiment that the standard SRM check misses.
- **[PPP Duplicate Loan Detection](https://github.com/TonyLee-99/ppp-duplicate-loan-detection)**: entity resolution on 8.6M first-draw PPP loans that share no business ID. It flags 36,288 businesses holding 2+ loans ($1.05B beyond their first loan). Their loans charge off at 13.4%, against 6.2% for all first-draw loans.
- **[Marketplace Analytics](https://github.com/TonyLee-99/marketplace-analytics)** ([live dashboard](https://tonylee-99.github.io/marketplace-analytics/dashboard/)): a dbt + DuckDB warehouse, 17 governed KPIs and an executive dashboard on 99K real Olist orders. Most of the "late delivery costs 1.9 stars" effect is survey timing: on reviews written after delivery, the penalty is −0.51★.
- **[Venture AI OS](https://github.com/TonyLee-99/venture-ai-os)**: an AI diligence system for an early-stage AI × digital-assets fund. Every memo claim must cite a stored source, and a blind critic from a second model family rated only 30% of drafted claims fully supported. It also includes a point-in-time screening backtest.
- **[Specialty Infusion FP&A](https://github.com/TonyLee-99/specialty-infusion-fpa)**: a buy-and-bill margin engine and 2027 scenario plan (Excel with 1,757 live formulas, plus a Power BI model) on public CMS data. After sequestration and bad debt, Medicare's drug margin is about 1.6%. The 2028 exposure is white bagging, not drug price negotiation.

**Also**: [Virtual Engineer](https://github.com/TonyLee-99/uchicago-virtual-engineer-capstone) is my UChicago capstone (team of 4, Office of the CTO): LLM-assisted alarm triage for campus building automation on BigQuery and Google Cloud.
Coursework: [churn prediction](https://github.com/TonyLee-99/data-science-projects), [MLOps with MLflow and Feast](https://github.com/TonyLee-99/mlops-pipeline-mlflow-feast), [BART news summarization](https://github.com/TonyLee-99/ML2-Final-Project), [data versioning with DVC and dbt](https://github.com/TonyLee-99/data-versioning-project).

**Tools:** Python, TypeScript, SQL (DuckDB, BigQuery), dbt, Airflow, Dagster, PySpark (batch and Structured Streaming), Kafka, Delta Lake, Apache Iceberg, Terraform, Docker, GitHub Actions · LLM agents, RAG, evals, MCP, FastAPI, Next.js, Postgres · pandas, scikit-learn, LightGBM, PyTorch, R · Tableau, Power BI, Excel

[LinkedIn](https://www.linkedin.com/in/zhengtaoli) · zhengtaoli2024@gmail.com
