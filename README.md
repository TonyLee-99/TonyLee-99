### Hi, I'm Zhengtao (Tony) Li

Data scientist finishing an M.S. in Applied Data Science at the **University of Chicago** (Dec 2026), with a B.S. in Statistics and Analytics from **UNC-Chapel Hill**.
I build analytics and LLM systems on real public data. Each project ends in a decision, and the numbers that didn't work out are reported too.

**Selected work**

- **[Experimentation Platform](https://github.com/TonyLee-99/experimentation-platform)**: a warehouse-native A/B-testing engine (CUPED/CUPAC, SRM and covariate-balance gates, sequential tests). It found an assignment imbalance (z = 33) in Criteo's 14M-user ad experiment that the standard SRM check misses.
- **[PPP Duplicate Loan Detection](https://github.com/TonyLee-99/ppp-duplicate-loan-detection)**: entity resolution on 8.6M first-draw PPP loans that share no business ID. It flags 36,288 businesses holding 2+ loans ($1.05B beyond their first loan). Their loans charge off at 13.4%, against 6.2% for all first-draw loans.
- **[Marketplace Analytics](https://github.com/TonyLee-99/marketplace-analytics)** ([live dashboard](https://tonylee-99.github.io/marketplace-analytics/dashboard/)): a dbt + DuckDB warehouse, 17 governed KPIs and an executive dashboard on 99K real Olist orders. Most of the "late delivery costs 1.9 stars" effect is survey timing: on reviews written after delivery, the penalty is −0.51★.
- **[Analytics Agent](https://github.com/TonyLee-99/analytics-agent)**: a text-to-SQL agent with read-only guardrails, confidence-based abstention and a governed metric layer. BIRD execution accuracy rises from 62.6% to 73.2%. Business-metric questions go from 14/30 to 29/30 once metrics are compiled.
- **[Venture AI OS](https://github.com/TonyLee-99/venture-ai-os)**: an AI diligence system for an early-stage AI × digital-assets fund. Every memo claim must cite a stored source, and a blind critic from a second model family rated only 30% of drafted claims fully supported. It also includes a point-in-time screening backtest.
- **[Specialty Infusion FP&A](https://github.com/TonyLee-99/specialty-infusion-fpa)**: a buy-and-bill margin engine and 2027 scenario plan (Excel with 1,757 live formulas, plus a Power BI model) on public CMS data. After sequestration and bad debt, Medicare's drug margin is about 1.6%. The 2028 exposure is white bagging, not drug price negotiation.

**Also**: [Virtual Engineer](https://github.com/TonyLee-99/uchicago-virtual-engineer-capstone) is my UChicago capstone (team of 4, Office of the CTO): LLM-assisted alarm triage for campus building automation on BigQuery and Google Cloud.
Coursework: [churn prediction](https://github.com/TonyLee-99/data-science-projects), [MLOps with MLflow and Feast](https://github.com/TonyLee-99/mlops-pipeline-mlflow-feast), [BART news summarization](https://github.com/TonyLee-99/ML2-Final-Project), [data versioning with DVC and dbt](https://github.com/TonyLee-99/data-versioning-project).

**Tools:** Python (pandas, scikit-learn, LightGBM, PyTorch), SQL (DuckDB, BigQuery), dbt, R, Spark, Docker, GitHub Actions, Tableau, Power BI, Excel

[LinkedIn](https://www.linkedin.com/in/zhengtaoli) · zhengtaoli2024@gmail.com
