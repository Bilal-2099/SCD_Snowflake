# SCD Data Warehousing with Snowflake

![Python](https://img.shields.io/badge/Python-3.x-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![GitHub Repo](https://img.shields.io/badge/GitHub-Bilal--2099-orange)

## 📌 Project Overview
This project demonstrates how to implement Slowly Changing Dimensions (SCD) in a data warehouse environment using Snowflake.  
It focuses on preserving history of dimensional data while enabling analytics over time.

---

## 📊 Architecture / Flow
```
[Source System] → [Staging] → [SCD Dimension Tables (Type-1/Type-2)] → [Fact Tables / Analytics]
```
> Example: Insert new records, update changes with SCD logic, maintain current & historical rows.

---

## 🧰 Key Concepts
- **SCD Type 1**: Overwrite existing dimension attributes (no history preserved).
- **SCD Type 2**: Insert new rows when changes occur, mark previous rows as expired (history preserved).
- Manage effective dates, expiry dates, current-flags, and surrogate keys.
- Use Snowflake’s `MERGE INTO` statements or stored procedures to implement SCD logic efficiently.

---

## ⚡ Quick Start

### 1️⃣ Clone the repo
```bash
git clone https://github.com/Bilal-2099/SCD_DataWarehousing_Snowflake.git
cd SCD_DataWarehousing_Snowflake
```

### 2️⃣ Set up environment
- Ensure you have access to a Snowflake account and credentials.
- Install any required Python packages or tools (if relevant).
- Review SQL scripts (for example `scd_type2_scripts.sql`, `merge_dimension.sql`) in the repository.

### 3️⃣ Configure Snowflake
- Set up your database, schema, warehouse, and role.
- Upload or stage source data into the staging area.
- Execute the SCD pipelines (e.g., run the `MERGE` scripts against Snowflake).

### 4️⃣ Run the transformation logic
```sql
-- Example:
USE DATABASE YOUR_DB;
USE SCHEMA YOUR_SCHEMA;

-- Execute SCD logic scripts
```
(Refer to the repository’s SQL/README for detailed script names.)

---

## 🎯 Why This Project Matters
- Preserving historical dimension data is **critical** for time-based analytics (sales trend, customer behavior, product lifecycle).
- SCD Type 2 implementation is a core skill for data engineering and warehousing.
- Using Snowflake gives you experience with a modern cloud data warehouse platform.
- This project makes a strong portfolio piece, showcasing your ability to design, build and maintain data warehouse dimensions.

---

## 👤 Author
**Bilal Raza** — Python Developer & Data Engineering Student at S.M.I.T under Sir Qasim Hassan  
GitHub: [Bilal-2099](https://github.com/Bilal-2099)

---

## 📌 Possible Improvements
- Extend to **SCD Type 3 or Type 6** for additional scenarios.
- Automate pipeline execution using schedule tools (e.g., Apache Airflow).
- Incorporate data quality checks and row-level validation.
- Build dashboards or visualizations to show historical dimension changes.
- Implement CI/CD for your Snowflake SQL and scripts via GitHub Actions.

---

### 📄 License
MIT License