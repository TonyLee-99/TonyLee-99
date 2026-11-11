### Hi, I'm Zhengtao (Tony) Li

AI engineer, data engineer and data scientist finishing an M.S. in Applied Data Science at the **University of Chicago** (Dec 2026), with a B.S. in Statistics and Analytics from **UNC-Chapel Hill**.
I build data pipelines, warehouses and analytics on real public data, at real scale. Each project ends in a decision, and the numbers that didn't work out are reported too.

**AI agents**

- **[Analytics Agent v2](https://github.com/TonyLee-99/analytics-agent)**: a permission-aware copilot in Slack that answers over documents and a Postgres warehouse, deployed on 4.0M real Chicago 311 requests and 157 City documents. Document ACLs are enforced at retrieval time and every SQL query runs under the asking user's own role with row-level security. A 40-attack red team (half written blind by a different model) leaked 0 times; with the defences switched off the same checker finds 8 of 10 revocation scenarios leaking. 93% of 30 questions answered correctly vs 27% for docs-only RAG.
- **[Invoice Posting Agent](https://github.com/TonyLee-99/invoice-posting-agent)** ([demo](https://tonylee-99.github.io/invoice-posting-agent/demo/)): LLM-assisted accounts payable in TypeScript that must never double-post. The LLM extracts fields (F1 0.94 vs 0.77 for a regex baseline); matching, approval and posting are deterministic, with a transactional outbox, idempotent QuickBooks writes and nightly reconciliation. Across 300 chaos seeds (4,180 invoices, 2,803 injected remote faults, 925 worker crashes) no invoice was lost; with the defences off, 86 of 100 seeds double-posted.
- **[Support Agent Evals](https://github.com/TonyLee-99/support-agent-evals)**: a customer-support agent and the eval flywheel around it, with Sierra's tau2-bench retail as the external referee. On a frozen 10-task test split it reaches 85% pass^1 vs 70% for tau2's default agent (small sample, reported with CIs). Failed conversations are clustered and turned into CI regression gates; the biggest failure cluster turned out to be an interface bug, not the agent.

**Data engineering**

- **[Chicago 311 Warehouse](https://github.com/TonyLee-99/chicago-311-warehouse)**: an incremental warehouse for all 14.9M Chicago 311 service requests (Python, SQL, dbt, DuckDB, Airflow). Immutable Parquet landing, dbt snapshots for change history, Kimball marts and write-audit-publish. Every publish is reconciled against the City's own counts: 302 of 304 month × status cells match exactly and the other 2 are explained. The audit gate once blocked a half-built publish that was missing 3,096,285 requests.
- **[Bluesky Event Lakehouse](https://github.com/TonyLee-99/bluesky-event-lakehouse)**: a streaming lakehouse on Bluesky's live firehose (Kafka/Redpanda, Spark Structured Streaming, Apache Iceberg). It captured 11.5M real events in 6.8 hours. A second independent read of the source found 0 missing events, five chaos tests (kill -9, broker restart, duplicate replay) ended with 0 lost and 0 duplicated, and 368,881 deletes were applied 100%. A load test sustained 41,600 events/s, 89× the live rate.

**Analytics and ML**

- **[Experimentation Platform](https://github.com/TonyLee-99/experimentation-platform)**: a warehouse-native A/B-testing engine (CUPED/CUPAC, SRM and covariate-balance gates, sequential tests). It found an assignment imbalance (z = 33) in Criteo's 14M-user ad experiment that the standard SRM check misses.
- **[PPP Duplicate Loan Detection](https://github.com/TonyLee-99/ppp-duplicate-loan-detection)**: entity resolution on 8.6M first-draw PPP loans that share no business ID. It flags 36,288 businesses holding 2+ loans ($1.05B beyond their first loan). Their loans charge off at 13.4%, against 6.2% for all first-draw loans.
- **[Marketplace Analytics](https://github.com/TonyLee-99/marketplace-analytics)** ([live dashboard](https://tonylee-99.github.io/marketplace-analytics/dashboard/)): a dbt + DuckDB warehouse, 17 governed KPIs and an executive dashboard on 99K real Olist orders. Most of the "late delivery costs 1.9 stars" effect is survey timing: on reviews written after delivery, the penalty is −0.51★.
- **[Venture AI OS](https://github.com/TonyLee-99/venture-ai-os)**: an AI diligence system for an early-stage AI × digital-assets fund. Every memo claim must cite a stored source, and a blind critic from a second model family rated only 30% of drafted claims fully supported. It also includes a point-in-time screening backtest.
- **[Specialty Infusion FP&A](https://github.com/TonyLee-99/specialty-infusion-fpa)**: a buy-and-bill margin engine and 2027 scenario plan (Excel with 1,757 live formulas, plus a Power BI model) on public CMS data. After sequestration and bad debt, Medicare's drug margin is about 1.6%. The 2028 exposure is white bagging, not drug price negotiation.

**Also**: [Virtual Engineer](https://github.com/TonyLee-99/uchicago-virtual-engineer-capstone) is my UChicago capstone (team of 4, Office of the CTO): LLM-assisted alarm triage for campus building automation on BigQuery and Google Cloud.
Coursework: [churn prediction](https://github.com/TonyLee-99/data-science-projects), [MLOps with MLflow and Feast](https://github.com/TonyLee-99/mlops-pipeline-mlflow-feast), [BART news summarization](https://github.com/TonyLee-99/ML2-Final-Project), [data versioning with DVC and dbt](https://github.com/TonyLee-99/data-versioning-project).

**Tools:** Python, TypeScript, SQL (DuckDB, BigQuery), dbt, Airflow, Spark (incl. Structured Streaming), Kafka, Apache Iceberg, Terraform, Docker, GitHub Actions · LLM agents, RAG, evals, MCP, FastAPI, Next.js, Postgres · pandas, scikit-learn, LightGBM, PyTorch, R · Tableau, Power BI, Excel

[LinkedIn](https://www.linkedin.com/in/zhengtaoli) · zhengtaoli2024@gmail.com
