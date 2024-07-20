# OlampicDataAnalysis
# Tokyo Olympics Data Analysis Using ETL Process in Azure Cloud

## Project Overview
This project aims to analyze Tokyo Olympics data using ETL processes in Azure Cloud. The data includes information about athletes, coaches, entries by gender, medals, and teams.

## Data Files
- `Athletes.csv`
- `Coaches.csv`
- `EntriesGender.csv`
- `Medals.csv`
- `Teams.csv`

## Setup Instructions
1. **Azure Services**: Ensure you have access to Azure Data Factory, Azure Synapse Analytics, and Azure Blob Storage.
2. **Upload Data**: Upload the CSV files to Azure Blob Storage.
3. **ETL Pipeline**: Create an ETL pipeline in Azure Data Factory to ingest, transform, and load the data into Azure Synapse Analytics.
4. **Data Transformation**: Use ADF or Azure Databricks to clean and transform the data.
5. **Data Analysis**: Write SQL queries to analyze the data and use Power BI for visualization.

## Example SQL Query
```sql
SELECT Team, SUM(Gold) AS Gold, SUM(Silver) AS Silver, SUM(Bronze) AS Bronze
FROM Medals
GROUP BY Team
ORDER BY SUM(Gold) DESC;
