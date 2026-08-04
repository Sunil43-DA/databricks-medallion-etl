# Databricks Medallion ETL Pipeline using PySpark

## Project Overview

This project demonstrates an end-to-end ETL pipeline built using **Databricks Community Edition** and **PySpark**, following the **Medallion Architecture (Bronze → Silver → Gold)**.

The pipeline ingests raw CSV data, transforms it into Parquet format, performs data cleansing and enrichment, and produces business-ready aggregated datasets for analytics.

---

## Technologies Used

- Databricks Community Edition
- Apache Spark
- PySpark
- Python
- Parquet
- Git
- GitHub

---

## Medallion Architecture

```
CSV File
     │
     ▼
 Bronze Layer
 (Raw CSV → Parquet)
     │
     ▼
 Silver Layer
 (Data Cleaning + Transformation)
     │
     ▼
 Gold Layer
 (Business Aggregations)
```

---

## Bronze Layer

- Read CSV
- Infer schema
- Preserve raw data
- Write as Parquet

---

## Silver Layer

- Standardize column names
- Create derived column

```
total_price = quantity × price
```

- Filter records

```
total_price > 1000
```

- Store cleaned Parquet data

---

## Gold Layer

Business aggregations:

- Total Sales by Region
- Order Count by Region

---

## PySpark Operations Used

- spark.read()
- select()
- withColumn()
- withColumnRenamed()
- filter()
- groupBy()
- agg()
- write.mode("overwrite")

---

## Output

The project creates three layers:

```
bronze/
silver/
gold/
```

containing Parquet datasets for analytics.

---

## Author

**Sunil Reddy**

LinkedIn:
https://www.linkedin.com/in/sunil-reddy-35aa203ab

GitHub:
https://github.com/Sunil43-DA
