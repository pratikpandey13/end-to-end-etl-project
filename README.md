# Project Title: End-to-End Data Engineering Pipeline for Data Analysis

## Overview:
This project involved designing and implementing an end-to-end data engineering pipeline that efficiently ingests, processes, and analyzes data sourced from a locally hosted MS SQL Server. The pipeline utilizes various Azure services, including Azure Data Factory, Azure Data Lake, Azure Databricks, and Azure Synapse Analytics, to ensure robust data handling and insightful analysis.

![Data Pipeline](https://github.com/pratikpandey13/end-to-end-etl-project/blob/main/end-to-end-de-project.jpg)

Steps : 

1. Data Ingestion from Locally Hosted MS SQL Server to Azure Data Factory
The project commenced with the ingestion of data from a locally hosted MS SQL Server. To facilitate this, I set up a self-hosted integration runtime within Azure Data Factory. This integration runtime established a secure connection between the local SQL Server and Azure.

-- Implementation:
Configured linked services in Azure Data Factory to connect to the SQL Server database.
Created data ingestion pipelines using Azure Data Factory's copy activity, enabling efficient transfer of data.
Implemented incremental loading strategies to ensure only new or updated records were ingested, optimizing data transfer and minimizing load times.

2. Loading the Data from Azure Data Factory to Data Lake
Once the data was ingested into Azure Data Factory, the next step involved loading this data into Azure Data Lake Storage (ADLS).

-- Implementation:
Created a dedicated container within ADLS Gen2 to store the ingested data.
Utilized the Azure Data Factory pipeline to copy the data from the ingestion stage to ADLS, ensuring it was stored in an organized and accessible manner.
Applied data partitioning strategies to enhance performance and facilitate easier data retrieval.

3. Data Transformation Using Azure Databricks
After successfully loading the data into the Data Lake, I leveraged Azure Databricks for data transformation. This involved cleaning, aggregating, and enriching the data to make it suitable for analysis.

-- Implementation:
Developed notebooks in Databricks using PySpark for data processing.
Performed data cleansing operations, such as handling missing values and removing duplicates.
Conducted complex transformations, including joins and aggregations, to derive meaningful insights from the raw data.
Ensured that the transformed data was schema-compliant and ready for analytical processing.

4. Loading Transformed Data Back into Data Lake Gen 2
Following the transformation process, the refined dataset was then written back into Azure Data Lake Gen2 for storage and future access.

-- Implementation:
Configured output paths in Databricks to store the transformed data in ADLS Gen2.
Employed partitioning strategies to optimize the storage and retrieval of the transformed data.
Utilized Delta Lake format for data storage to provide ACID transaction support and improve data reliability.

5. Performing Analysis Using Azure Synapse Analytics
The final step of the project involved analyzing the transformed data using Azure Synapse Analytics. This enabled the extraction of actionable insights and facilitated reporting.

-- Implementation:
Set up Azure Synapse Analytics to query the transformed data stored in ADLS Gen2.
Utilized SQL to perform exploratory data analysis (EDA), generating insights through various queries and aggregations.
Created visualizations and reports to present the findings, enabling stakeholders to make data-driven decisions.

## Conclusion
This end-to-end data engineering project demonstrated the ability to integrate multiple Azure services effectively, showcasing skills in data ingestion, transformation, and analysis. The resulting data pipeline not only streamlined data workflows but also provided valuable insights to drive business strategy and decision-making. The experience gained from this project reinforced my proficiency in cloud-based data engineering and data analytics tools, positioning me for future challenges in this dynamic field.
