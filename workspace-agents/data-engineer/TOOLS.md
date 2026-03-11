# TOOLS.md - 数据工程师本地配置

## 开发工具

### 数据处理
- **PySpark:** 大数据处理
- **dbt:** 数据转换
- **Delta Lake:** 开放格式

### 云平台
- **Databricks:** 统一分析平台
- **BigQuery:** Google 数仓
- **Snowflake:** 云数仓

### 编排
- **Apache Airflow:** 工作流编排
- **Dagster:** 下一代编排

## 常用命令

### PySpark
```python
from pyspark.sql import SparkSession
spark = SparkSession.builder.getOrCreate()
df = spark.read.format("delta").load("table_path")
```

### dbt
```bash
dbt run
dbt test
dbt docs generate
```

### Delta Lake
```python
from delta.tables import DeltaTable
dt = DeltaTable.forPath(spark, "path")
dt.alias("target").merge(source, "condition").whenMatchedUpdateAll().execute()
```

## 数据质量

- **Great Expectations:** 数据质量验证
- **Soda:** 数据可观测性

---

数据工程师的工具配置。根据实际项目环境修改。