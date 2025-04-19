
# 🚀 Cloud Analytics for Data Analyst Job Market Insights  
**End-to-End ETL, BigQuery Data Warehousing, and Tableau Visualizations using Google Cloud**

---

## 🔍 Project Overview  
This project focused on delivering end-to-end cloud analytics using **Google Cloud Platform (GCP)** to analyze over **16,000+ data analyst job postings in the U.S.**. We built a scalable **ETL pipeline** to ingest data from multiple sources—including a **Kaggle-hosted dataset** and a **real-time JSON feed from the SERP API**—and transformed it into a **BigQuery-based data warehouse**. The insights were visualized using **Tableau dashboards**, offering actionable intelligence on job roles, salaries, locations, and in-demand skills.

📦 **Dataset Source**:  
[Kaggle – Historic Data Analyst Job Postings](https://www.kaggle.com/datasets/lukebarousse/data-analyst-job-postings-google-search)

---
## Pipeline Archtecture
<img width="1050" alt="image" src="https://github.com/user-attachments/assets/d29a60e4-5cb1-42dc-96a6-737be2a47cfa" />

## 🧱 Cloud Architecture & Tools

| Layer                    | Technology/Service                          |
|-------------------------|---------------------------------------------|
| **Ingestion**           | Google Cloud Storage, SERP API, Kaggle CSV  |
| **Pipeline Orchestration** | Cloud Composer (Apache Airflow)          |
| **Transformations**     | Airflow DAGs (Python, SQL), staging & fact layers |
| **Data Warehouse**      | Google BigQuery with Star Schema            |
| **NoSQL (optional)**    | MongoDB Atlas via VPC Peering               |
| **Visualization**       | Tableau (connected to BigQuery)             |

---

## 🔄 ETL Pipeline Workflow

### 1. **Extract**
- Ingested structured CSV data from Kaggle.
- Pulled semi-structured JSON data from the SERP API to simulate real-time job posting updates.
- Stored both data types in **GCS buckets** (landing zone).

### 2. **Transform**
- Loaded data into a **staging layer** to ensure data quality checks.
- Merged and cleaned the data.
- Split into **Fact and Dimension** tables using a **Star Schema** design.

### 3. **Load**
- Cleaned and structured data was loaded into **BigQuery** for downstream analytics.

📌 **Why ETL (vs ELT)?**  
ETL was chosen to enforce quality checks *before* loading into BigQuery. The staging layer enabled filtering, normalization, and transformation, ensuring data integrity.

---

## 📈 Analysis & Visualization

Performed SQL-based exploration and built Tableau dashboards to derive insights such as:

- **Top Skills**: SQL, Tableau, Power BI, Python
- **Most Common Locations**: Missouri, Kansas, Oklahoma, Arkansas
- **Salary Trends**: Average salaries and role-based compensation (Data Engineers top earners)
- **Top Employers**: Upwork, Edward Jones, Talentify.io
- **Popular Platforms**: LinkedIn, Upwork, Indeed

Used advanced BigQuery queries to extract:
- Work-from-home job counts per company
- Salary by skill and job title
- Most requested job schedule types
- Top cities with highest average pay

---

## 🧠 Key Learnings & Highlights

- Built a **production-style ETL workflow** using **Airflow DAGs**, sensors, and schedulers.
- Leveraged **Cloud Composer v1** (due to resource limitations with v2).
- Explored **GCS sensors** for auto-triggered pipelines and set up **email alerting** on DAG failure/success.
- Used **VPC Peering** to securely connect Google Cloud and MongoDB Atlas (simulating hybrid cloud NoSQL).

---

## 🎯 Outcome

This project simulates a real-world cloud analytics workflow:
- Handling **semi-structured and structured data**
- Building a **repeatable and scalable ETL pipeline**
- Generating **meaningful job market insights**
- Delivering visual intelligence through **interactive Tableau dashboards**

It prepares students and professionals for roles involving **cloud data engineering**, **analytics**, and **modern data stacks**.
