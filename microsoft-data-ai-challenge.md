# This repository serves as my notebook in taking the [Microsoft Data and AI: Who Hacked? Challenge](https://docs.microsoft.com/en-us/learn/challenges?id=6e76f1bd-257e-48d5-875b-b6f1e25cf028&WT.mc_id=cloudskillschallenge_6e76f1bd-257e-48d5-875b-b6f1e25cf028).

### Table of Contents

# Azure Synapse Analytics
<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/synapse-overview.png">
</p>

Azure Synapse Analytics is an integrated analytics platform, which combines data warehousing, big data analytics, data integration, and visualization into a single environment. It can work by acting as the one stop shop to meet all of your analytical needs in an integrated environment if you do not have an analytical environment in place already.

It supports multiple analytical types such as:

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/types-analytics.png">
</p>

### Descriptive analytics
Descriptive analytics answers the question *“What is happening in my business?”*

Common solution: Create a data warehouse.

Azure Synapse Analytics leverages the dedicated SQL pool capability that enables you to create a persisted data warehouse to perform this type of analysis.

### Diagnostic analytics
Diagnostic analytics deals with answering the question *“Why is it happening?*

Common solution: Explore information in existing data warehouse or a wider search in your data estate to find more data.

You can use the same serverless SQL pool capability within Azure Synapse Analytics that enables you to interactively explore data within a data lake. Serverless SQL pools can quickly enable a user to search for additional data.

### Predictive analytics
Predictive analysis answers the question *“What is likely to happen in the future based on previous trends and patterns?”*

Azure Synapse Spark, an integrated Apache Spark engine, pools can be used with other services such as Azure Machine Learning Services, or Azure Databricks.

### Prescriptive analytics
This type of analytics looks at *executing actions based on real-time or near real-time analysis of data*, using predictive analytics.

Azure Synapse Analytics provides this capability through both Apache Spark, Azure Synapse Link, and by integrating streaming technologies such as Azure Stream Analytics.

Azure Synapse Analytics brings two worlds, serverless and dedicated resources, together with a unified data integration experience to ingest, prepare, manage, and serve data using Azure Synapse Pipelines. In addition, you can visualize the data in the form of dashboards and reports for immediate analysis using Power BI, which is integrated into the service too.

## Apache Spark pool with full support for Scala, Python, SparkSQL, and C#
You can develop big data engineering and machine learning solutions using Apache Spark for Azure Synapse. You can take advantage of the big data computation engine to deal with complex compute transformations that would take too long in a data warehouse. For machine learning workloads, you can use SparkML algorithms and AzureML integration for Apache Spark 2.4 with built-in support for Linux Foundation Delta Lake.

## Data integration with Azure Synapse Pipelines
Azure Synapse Pipelines leverages the capabilities of Azure Data Factory and is the cloud-based ETL and data integration service that allows you to create data-driven workflows for orchestrating data movement and transforming data at scale.

You can create and schedule data-driven workflows with Azure Synapse Pipelines. You can build complex ETL processes that transform data visually with data flows or by using compute services such as Azure Databricks.

## Perform operational analytics with near real-time hybrid transactional and analytical processing with Azure Synapse Link
Azure Synapse Analytics enables you to reach out to operational data using Azure Synapse Link, and is achieved without impacting the performance of the transactional data store. As data changes in the transactional system, the changed data is fed to the analytical store in a Column store format from which Azure Synapse Link can query with no disruption to the source system.

## When to use Azure Synapse Analytics
Across all organizations and industries, the common use cases for Azure Synapse Analytics are identified by the need for:

### Modern data warehousing
This involves the ability to integrate all data, including big data, to reason over data for analytics and reporting purposes from a descriptive analytics perspective, independent of its location or structure.

### Advanced analytics
Enables organizations to perform predictive analytics using both the native features of Azure Synapse Analytics, and integrating with other technologies such as Azure Databricks.

### Data exploration and discovery
The serverless SQL pool functionality provided by Azure Synapse Analytics enables Data Analysts, Data Engineers and Data Scientist alike to explore the data within your data estate. This capability supports data discovery, diagnostic analytics, and exploratory data analysis.

### Real time analytics
Azure Synapse Analytics can capture, store and analyze data in real-time or near-real time with features such as Azure Synapse Link, or through the integration of services such as Azure Stream Analytics and Azure Data Explorer.

### Data integration
Azure Synapse Pipelines enables you to ingest, prepare, model and serve the data to be used by downstream systems. This can be used by components of Azure Synapse Analytics exclusively.

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/synapse-only-process.png">
</p>

It can also interact with existing Azure services that you may already have in place for your existing analytical solutions.

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/synapse-azure-process.png">
</p>

### Integrated analytics
With the variety of analytics that can be performed on the data at your disposal, putting together the services in a cohesive solution can be a complex operation. Azure Synapse Analytics removes this complexity by integrating the analytics landscape into one service.
