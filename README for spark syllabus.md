# ⚡ PySpark in Databricks — Beginner Training

**Author:** Raamashaamy &nbsp;|&nbsp; **Date:** March 2026 &nbsp;|&nbsp; **Platform:** Databricks  
**Duration:** 11 Sessions &nbsp;|&nbsp; **Total Hours:** ~10–12 hrs

---

## 📌 About This Course

A hands-on, structured training program for absolute beginners to learn **Apache Spark using the PySpark API on Databricks**. Each session builds on the previous one — from core theory to real-world DataFrame operations, SQL, joins, window functions, and performance basics — culminating in a **Capstone Mini Project**.

---

## 🗂️ Session Index

| Session | Title | Type |
|--------:|-------|------|
| [Session 00](#session-00--spark-theory-foundation--reading-files) | Spark Theory Foundation & Reading Files | Theory + Demo |
| [Session 01](#session-01--spark-basics--your-first-dataframe) | Spark Basics & Your First DataFrame | Hands-On |
| [Session 02](#session-02--dataframe-transformations---part-1) | DataFrame Transformations — Part 1 | Hands-On |
| [Session 03](#session-03--dataframe-transformations---part-2) | DataFrame Transformations — Part 2 | Hands-On |
| [Session 04](#session-04--aggregations--groupby) | Aggregations & GroupBy | Hands-On |
| [Session 05](#session-05--spark-sql) | Spark SQL | Hands-On |
| [Session 06](#session-06--joins) | Joins | Hands-On |
| [Session 07](#session-07--built-in-functions) | Built-in Functions (`pyspark.sql.functions`) | Hands-On |
| [Session 08](#session-08--window-functions) | Window Functions | Hands-On |
| [Session 09](#session-09--udfs--schema-management) | UDFs & Schema Management | Hands-On |
| [Session 10](#session-10--performance-basics) | Performance Basics (Intro Level) | Hands-On |
| [Capstone](#-capstone-mini-project) | Capstone Mini Project | Project |

---

## Session 00 — Spark Theory Foundation & Reading Files

> 🎯 **Goal:** Understand *why* Spark exists and how it is structured before touching any code.

- History of Apache Spark and motivation over MapReduce
- Spark architecture: Driver, Executors, Cluster Manager
- RDD vs DataFrame vs Dataset — conceptual overview
- `SparkContext` vs `SparkSession`
- Reading files: CSV, JSON, Parquet using `spark.read`
- Inferring schema vs defining schema explicitly
- Basic `.show()`, `.printSchema()`, `.dtypes` exploration

---

## Session 01 — Spark Basics & Your First DataFrame

> 🎯 **Goal:** Launch Spark, load real data, and explore a DataFrame confidently.

- Launch `SparkSession` with `SparkSession.builder`
- Read CSV, JSON, Parquet files into a DataFrame
- `.show()`, `.printSchema()`, `.dtypes`, `.columns`
- `.count()` and `.describe()` for quick profiling
- Write output back to disk (CSV / Parquet)

---

## Session 02 — DataFrame Transformations — Part 1

> 🎯 **Goal:** Select, filter, and reshape columns with core transformation methods.

- `.select()` and `.filter()` / `.where()`
- `.withColumn()` — adding and modifying columns
- `.withColumnRenamed()` and `.drop()`
- Column expressions: `col()`, `lit()`, arithmetic operators
- `.alias()` for renaming expressions inline

---

## Session 03 — DataFrame Transformations — Part 2

> 🎯 **Goal:** Clean and prepare data — handle duplicates, nulls, ordering, and types.

- `.distinct()` and `.dropDuplicates()`
- `.orderBy()` / `.sort()` for sorting results
- `.limit()` for previewing large datasets
- Handling nulls: `.isNull()`, `.isNotNull()`, `.fillna()`, `.dropna()`
- `.cast()` for type casting columns

---

## Session 04 — Aggregations & GroupBy

> 🎯 **Goal:** Summarise data using group-level aggregations and pivot tables.

- `.groupBy().agg()` with multiple aggregations
- Built-in functions: `sum()`, `avg()`, `count()`, `min()`, `max()`
- `.groupBy().count()` shorthand
- `F.countDistinct()` for unique value counts
- `.pivot()` for basic pivot table creation

---

## Session 05 — Spark SQL

> 🎯 **Goal:** Query DataFrames using familiar SQL syntax alongside the DataFrame API.

- Create temp views with `.createOrReplaceTempView()`
- Run SQL queries using `spark.sql("SELECT ...")`
- SQL vs DataFrame API — when to use which
- Subqueries and CTEs in Spark SQL
- Mix SQL and DataFrame API in the same pipeline

---

## Session 06 — Joins

> 🎯 **Goal:** Combine DataFrames using all major join types safely and efficiently.

- Inner, Left, Right, Full Outer joins
- `.join(df2, on=..., how=...)` syntax
- Joining on multiple columns
- Handling duplicate column names after a join
- Broadcast join — what it is and when to use `broadcast()`

---

## Session 07 — Built-in Functions

> 🎯 **Goal:** Use the rich `pyspark.sql.functions` library for common data transformations.

**String functions**
- `upper()`, `lower()`, `trim()`, `concat()`, `split()`, `regexp_replace()`

**Date functions**
- `current_date()`, `datediff()`, `date_format()`, `to_date()`

**Conditional logic**
- `when().otherwise()`

**Array functions**
- `explode()`, `collect_list()`, `array_contains()`

---

## Session 08 — Window Functions

> 🎯 **Goal:** Perform row-level calculations within partitions — ranking, running totals, lag/lead.

- `Window.partitionBy().orderBy()` — defining a window spec
- `row_number()`, `rank()`, `dense_rank()`
- `lag()` and `lead()` for accessing adjacent rows
- Running totals with `sum().over(window)`
- Practical use case: Get the latest record per customer

---

## Session 09 — UDFs & Schema Management

> 🎯 **Goal:** Extend PySpark with custom Python logic and define schemas explicitly.

- Define and register a Python UDF with `udf()`
- Apply UDF on a DataFrame column
- Why UDFs are slow — when to avoid them
- Define schema using `StructType` and `StructField`
- Read files with an explicit custom schema

---

## Session 10 — Performance Basics (Intro Level)

> 🎯 **Goal:** Understand the fundamentals of Spark performance and avoid common beginner pitfalls.

- Understanding partitions: `.repartition()` vs `.coalesce()`
- Caching: `.cache()` vs `.persist()`
- `.explain()` — reading a basic query / execution plan
- Avoiding common beginner mistakes (repeated `.count()`, unnecessary shuffles)
- Writing partitioned output: `.write.partitionBy()`

---

## 🏆 Capstone Mini Project

> 🎯 **Goal:** Apply everything learned in a realistic end-to-end data pipeline.

A four-step mini pipeline that ties together all sessions:

```
Step 1 → Read raw data (CSV / JSON)
Step 2 → Clean & transform (handle nulls, fix types, apply filters)
Step 3 → Aggregate using GroupBy and Window functions
Step 4 → Join with a lookup / dimension table
```

---

## 🚀 Getting Started

1. **Import notebooks** into your Databricks workspace via *Repos* or manual upload.
2. **Attach a cluster** — Databricks Runtime 13.x or above recommended.
3. Run sessions **in order** (Session 00 → 10) for the best learning experience.
4. Each notebook is self-contained with datasets created inline — no external files needed.

---

*Training material by **Raamashaamy** | March 2026*
