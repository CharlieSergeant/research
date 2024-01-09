## Databricks

Offers data science and engineering teams a single platform to manage clusters and explore data interactively

Databricks Control Plane: AKS behind the scenes

Built on:
- [Apache Spark](https://spark.apache.org/docs/latest/api/python/getting_started/index.html): distributed real-time, large scale data processing
- [MLFlow](https://mlflow.org/docs/latest/getting-started/index.html): end to end ML lifecycle management
- [DeltaLake](https://docs.delta.io/latest/quick-start.html): ACID transactions on spark, metadata handling
- [Koalas](https://koalas.readthedocs.io/en/latest/reference/index.html): For Pandas-Spark API

### Getting Started

Examples: https://github.com/solliancenet/microsoft-learning-paths-databricks-notebooks/tree/master

Tutorial: https://learn.microsoft.com/en-us/azure/databricks/

Docs: https://api-docs.databricks.com/python/pyspark/latest/index.html

Veiw DBC files outside of databricks: VS Code -> Extensions -> DBC Language Syntax


### [Apache Spark](https://spark.apache.org/docs/latest/api/python/getting_started/index.html)
- SQL Dataframes (Parallel processing)
- Spark ML
- Graph
- Streaming
- Scala or Python

### [DeltaLake](https://docs.delta.io/latest/quick-start.html)
- transactional storage layer
- schema enforcement
- table repairs
- metadata refreshes
- parquet
- hive/dbfs directories 

User Defined Functions (UDF) which can operate on dataframes

### [MLFlow](https://mlflow.org/docs/latest/getting-started/index.html)
- track expirements
- log metrics
- compare runs

### Databricks Workspace

- data is stored via DBFS
- Root folder for all Databricks assets (notebooks, libraries and dashboards)

**Start Azure Databricks**

Azure Portal -> Create a Resource -> Azure Databricks -> Create

https://azure.microsoft.com/en-us/pricing/details/databricks/

**Create Azure Databricks Cluster**

Azure Databricks Resource -> Launch Workspace -> Clusters -> Create Cluster (Single Node, Scala Spark)

Other Workflows:
- Create Notebook


- Databricks Workflows
- Databricks Runtime
- Databricks I/O
- Databricks Serverless
- Databricks Enterprise Security



