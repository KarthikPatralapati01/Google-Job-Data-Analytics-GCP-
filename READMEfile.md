# Cloud-Analytics-for-Data-Analyst-Job-Market-Insights

![ETL Process](etl1.jpg)
## Overview
The goal of this project was to perform cloud analytics and data warehouse implementation on a dataset of over 16,000 data analyst job postings in the US. The raw CSV data from Kaggle and JSON data from the SERP API was loaded into Google BigQuery for analysis. 

An ETL pipeline was built using Google Cloud Composer and Airflow to automate the extraction, transformation and loading of data into staging and production datasets. Queries were executed on BigQuery and visualizations created in Tableau to generate insights.

## Methodology
- **Data Sources**: CSV file from Kaggle obtained via web scraping and JSON file from SERP API Google search results 
- **Cloud Architecture**: Google Cloud Platform services including Cloud Storage buckets, Cloud Composer, BigQuery data warehouse and Tableau for visualization
- **ETL Pipeline**:
    - *Extract* - data from CSV and API 
    - *Transform* - staging and production transformations 
    - *Load* - to BigQuery tables
- **Analysis**: SQL queries on BigQuery anddashboards in Tableau

## Technical Details
- **Airflow**: pipeline automation and scheduling
- **BigQuery**: star schema with fact and dimension tables
- **Tableau**: interactive visualizations and KPI dashboards 

## Key Insights
- Huge demand for entry level data analyst roles
- Top skills: SQL, PowerBI, Tableau, Python 
- Top locations: Missouri, Kansas, Oklahoma, Arkansas
- Top companies: Upwork, Edward Jones, Talentify.io
- Most common recruitment channels: LinkedIn, Upwork, Indeed

## Conclusion
The project demonstrated effective use of cloud data pipeline and analytics tools to gather insights from a large, updating dataset. Automation using Composer and Airflow ensured timely ETL. BigQuery and Tableau facilitated data analysis and visualization.
