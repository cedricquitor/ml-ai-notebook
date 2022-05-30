# This repository serves as my notebook in taking the [Microsoft Data and AI: Who Hacked? Challenge](https://docs.microsoft.com/en-us/learn/challenges?id=6e76f1bd-257e-48d5-875b-b6f1e25cf028&WT.mc_id=cloudskillschallenge_6e76f1bd-257e-48d5-875b-b6f1e25cf028).

### Table of Contents

# Introduction to Azure Synapse Analytics
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

# Design a Modern Data Warehouse using Azure Synapse Analytics
## Describe a modern data warehouse
A modern data warehouse lets you bring together all your data at any scale easily, and means you can get insights through analytical dashboards, operational reports, or advanced analytics for all your users.

The pace of change in both the capabilities of technologies, and the elastic nature of cloud services has meant that new opportunities have been presented to evolve the data warehouse to handle modern workloads including:

### Increased volumes of data
Microsoft Azure services have the capability to scale its capacity to meet the demands that an organization faces as its data grows. In traditional on-premises data, scaling on-premises servers is a non-trivial task that involves costs, procurement of additional hardware, as well as potential disruption to the business to meet the demand.

You can auto-scale or scale in one click with Azure. It is pay-as-you go compared to on-premise which requires you to pay upfront cost.

### New varieties of data
Staging data is also simplified using Azure Data Lake Store Gen2, which can store a wide variety of data in its raw format, making the process of ingesting data into a data warehouse much easier.

Traditional data warehouses in the past have had difficulty in handling certain types of data. For example, extrapolating data from sources such as PDF files through to sound files were either too complex or cost prohibitive. The improvements in AI technologies such as Form Recognizer and Speech to Text Cognitive Services means that these types of data sources can now be passed through a cognitive service and outputted in a text-based format that can be stored in the Azure Data Lake Store Gen2, along with the source files themselves.

### Data velocities
Traditional on-premises data warehouses in the main have dealt with the batch movement of data based on a schedule. Some organization may build real-time data warehouse if the business need is compelling and the organization can absorb the cost of the implementation.

## Define a modern data warehouse architecture
When thinking about usage patterns that customers are using today to maximize the value of their data, a modern data warehouse lets you bring together all your data at scale easily, so you get to the insights through analytics dashboards, operational reporting, or advanced analytics for your users.

The process of building a modern data warehouse typically consists of:

- Data Ingestion and Preparation.
- Making the data ready for consumption by analytical tools.
- Providing access to the data, in a shaped format so that it can easily be consumed by data visualization tools.

Prior to the release of Azure Synapse Analytics, this would be achieved in the following way:

### Data ingestion and preparation
At the foundation, customers build a data lake to store all their data and different data types with Azure Data Lake Store Gen2. To ingest data, customers can do so code-free with over 100 data integration connectors with Azure Data Factory. Data Factory empowers customers to do code-free ETL/ELT, including preparation and transformation.

Whether the data is an on-premises data sources, other Azure services, or other cloud services, customers can seamlessly author, monitor, and manage their big data pipelines with a visual environment that is easy to use.

### Making the data ready for consumption by analytical tools
Azure Synapse Analytics implements a data warehouse using a dedicated SQL pool that leverages the Massively Parallel Processing engine that brings together enterprise data warehousing and Big Data analytics.

### Providing access to the data, in a shaped format so that it can easily be consumed by data visualization tools
Power BI enables customers to build visualizations on massive amounts of data and ensures that data insights are available to everyone across their organization. Power BI supports an enormous set of data sources, which can be queried live, or be used to model and ingest for detailed analysis and visualization.

### Defining a modern data warehousing architecture with Azure Synapse Analytics
You can either use Azure Synapse exclusively, which works well for green field projects. But for organizations with existing investments in Azure with Azure Data Factory, Azure Databricks and Power BI, you can take a hybrid approach and combine them with Azure Synapse Analytics. It is also important to understand that you can also use a range of languages to ingest data, clean, transform and serve the data. These languages can include the SQL, Python and Scala language. All of which can be used within Azure Synapse Analytics.

# Use automated machine learning in Azure Machine Learning
## What is machine learning?
It is a technique where you can use data to train a model that predicts unknown information.

For example, suppose Adventure Works Cycles is a business that rents cycles in a city. The business could use historic data to train a model that predicts daily rental demand in order to make sure sufficient staff and cycles are available.

To do this, Adventure Works could create a machine learning model that takes information about a specific day (the day of week, the anticipated weather conditions, and so on) as an input, and predicts the expected number of rentals as an output.

## Azure Machine Learning
Azure Machine Learning is a cloud-based service that helps simplify some of the tasks and reduce the time it takes to prepare data, train a model, and deploy a predictive service. 

## Create an Azure Machine Learning workspace
Azure Machine Learning is a cloud-based platform for building and operating machine learning solutions in Azure. It includes a wide range of features and capabilities that help data scientists prepare data, train models, publish predictive services, and monitor their usage. Most importantly, it helps data scientists increase their efficiency by automating many of the time-consuming tasks associated with training models; and it enables them to use cloud-based compute resources that scale effectively to handle large volumes of data while incurring costs only when actually used.

## Create an Azure Machine Learning workspace
Follow these steps to create a workspace:
1. Sign into the [Azure](https://portal.azure.com/#home) portal using your Microsoft credentials.
2. Select ＋Create a resource, search for Machine Learning, and create a new Azure Machine Learning resource with an Azure Machine Learning plan. Use the following settings:

    - **Subscription:** Your Azure subscription
    - **Resource group:** Create or select a resource group
    - **Workspace name:** Enter a unique name for your workspace
    - **Region:** Select the geographical region closest to you
    - **Storage account:** Note the default new storage account that will be created for your workspace
    - **Key vault:** Note the default new key vault that will be created for your workspace
    - **Application insights:** Note the default new application insights resource that will be created for your workspace
    - **Container registry:** None (one will be created automatically the first time you deploy a model to a container)

3. Select Review + create. Wait for your workspace to be created (it can take a few minutes). Then go to it in the portal.
4. On the Overview page for your workspace, launch Azure Machine Learning studio (or open a new browser tab and navigate to https://ml.azure.com), and sign into Azure Machine Learning studio using your Microsoft account.
5. In Azure Machine Learning studio, toggle the ☰ icon at the top left to view the various pages in the interface. You can use these pages to manage the resources in your workspace.

You can manage your workspace using the Azure portal, but for data scientists and Machine Learning operations engineers, Azure Machine Learning studio provides a more focused user interface for managing workspace resources.

## Create compute resources
At its core, Azure Machine Learning is a platform for training and managing machine learning models, for which you need compute on which to run the training process.

### Create a compute cluster
Compute targets are cloud-based resources on which you can run model training and data exploration processes.

In [Azure Machine Learning studio](https://ml.azure.com/), expand the left pane by selecting the three lines at the top left of the screen. View the Compute page (under Manage). This is where you manage the compute targets for your data science activities. There are four kinds of compute resource you can create:
- **Compute Instances:** Development workstations that data scientists can use to work with data and models.
- **Compute Clusters:** Scalable clusters of virtual machines for on-demand processing of experiment code.
- **Inference Clusters:** Deployment targets for predictive services that use your trained models.
- **Attached Compute:** Links to existing Azure compute resources, such as Virtual Machines or Azure Databricks clusters.

1. Switch to the Compute Clusters tab, and add a new compute cluster with the following settings. You'll use this to train a machine learning model:
- **Location:** Select the same as your workspace. If that location is not listed, choose the one closest to you
- **Virtual Machine tier:** Dedicated
- **Virtual Machine type:** CPU
- **Virtual Machine size:**
    - Choose **Select from all options**
    - Search for and select **Standard_DS11_v2**
- Select **Next**
- **Compute name:** enter a unique name
- **Minimum number of nodes:** 0
- **Maximum number of nodes:** 2
- **Idle seconds before scale down:** 120
- **Enable SSH access:** Unselected
- Select **Create**

## Explore data
Machine learning models must be trained with existing data. In this case, you'll use a dataset of historical bicycle rental details to train a model that predicts the number of bicycle rentals that should be expected on a given day, based on seasonal and meteorological features.

### Create a dataset
In Azure Machine Learning, data for model training and other operations is usually encapsulated in an object called a dataset.

1. View the comma-separated data at https://aka.ms/bike-rentals in your web browser.
2. In [Azure Machine Learning studio](https://ml.azure.com/), expand the left pane by selecting the three lines at the top left of the screen. View the Data page (under Assets). The Data page contains specific data files or tables that you plan to work with in Azure ML. You can create datasets from this page as well.
3. Create a new dataset from web files, using the following settings:
- **Basic Info:**
    - **Web URL:** https://aka.ms/bike-rentals
    - **Name:** bike-rentals
    - **Dataset type:** Tabular
    - **Description:** Bicycle rental data
    - **Skip data validation:** do not select
- **Settings and preview:**
    - **File format:** Delimited
    - **Delimiter:** Comma
    - **Encoding:** UTF-8
    - **Column headers:** Only first file has headers
    - **Skip rows:** None
    - **Dataset contains multi-line data:** do not select
- **Schema:**
    - Include all columns other than **Path**
    - Review the automatically detected types
- **Confirm details:**
    - Do not profile the dataset after creation

4. After the dataset has been created, open it and view the Explore page to see a sample of the data. This data contains historical features and labels for bike rentals.

## Train a machine learning model
The automated machine learning capability in Azure Machine Learning supports supervised machine learning models - in other words, models for which the training data includes known label values. You can use automated machine learning to train models for:
- **Classification** (predicting categories or classes)
- **Regression** (predicting numeric values)
- **Time series forecasting** (predicting numeric values at a future point in time)

### Run an automated machine learning experiment
In Azure Machine Learning, operations that you run are called experiments. Follow the steps to run an experiment that uses automated machine learning to train a regression model that predicts bicycle rentals.

1. In [Azure Machine Learning studio](https://ml.azure.com/), view the Automated ML page (under Author).
2. Create an Automated ML run with the following settings:
- **Select dataset:**
    - **Dataset:** bike-rentals
- **Configure run:**
    - **New experiment name:** mslearn-bike-rental
    - **Target column:** rentals (this is the label that the model is trained to predict)
    - **Select compute cluster:** the compute cluster that you created previously
- **Select task and settings:**
    - **Task type:** Regression (the model predicts a numeric value)

Notice under task type there are settings View additional configuration settings and View Featurization settings. Now configure these settings.
- **Additional configuration settings:**
    - **Primary metric:** Select **Normalized root mean squared error**
    - **Explain best model:** Selected — _this option causes automated machine learning to calculate feature importance for the best model which makes it possible to determine the influence of each feature on the predicted label._
    - **Use all supported models:** Unselected. You'll restrict the experiment to try only a few specific algorithms.
    - **Allowed models:** Select only **RandomForest** and **LightGBM** — normally you'd want to try as many as possible, but each model added increases the time it takes to run the experiment.
    - **Exit criterion:**
        - **Training job time (hours):** 0.5 — _ends the experiment after a maximum of 30 minutes._
        - **Metric score threshold:** 0.085 — _if a model achieves a normalized root mean squared error metric score of 0.085 or less, the experiment ends._
    - **Concurrency:** _do not change_
- **Featurization settings:**
    - **Enable featurization:** Selected — _automatically preprocess the features before training._

Click Next to go to the next selection pane.
- **Optional** Select the validation and test type
    - **Validation type:** Auto
    - **Test dataset (preview):** No test dataset required

3. When you finish submitting the automated ML run details, it starts automatically. Wait for the run status to change from Preparing to Running.
4. When the run status changes to Running, view the Models tab and observe as each possible combination of training algorithm and pre-processing steps is tried and the performance of the resulting model is evaluated. The page automatically refreshes periodically, but you can also select ↻ Refresh. It might take 10 minutes or so before models start to appear, as the cluster nodes must be initialized before training can begin.
5. Wait for the experiment to finish. It might take a while — now might be a good time for a coffee break!

### Review the best model
After the experiment has finished you can review the best performing model. In this case, you used exit criteria to stop the experiment. Thus the "best" model the experiment generated might not be the best possible model, just the best one found within the time allowed for this exercise.

1. On the Details tab of the automated machine learning run, note the best model summary.
2. Select the **Algorithm name** for the best model to view its details.

The best model is identified based on the evaluation metric you specified, _Normalized root mean squared error_.

A technique called _cross-validation_ is used to calculate the evaluation metric. After the model is trained using a portion of the data, the remaining portion is used to iteratively test, or cross-validate, the trained model. The metric is calculated by comparing the predicted value from the test with the actual known value, or label.

The difference between the predicted and actual value, known as the _residuals_, indicates the amount of error in the model. The particular performance metric you used, normalized root mean squared error, is calculated by squaring the errors across all of the test cases, finding the mean of these squares, and then taking the square root. What all of this means is that smaller this value is, the more accurate the model's predictions.

3. Next to the _Normalized root mean squared error value_, select **View all other metrics** to see values of other possible evaluation metrics for a regression model.
4. Select the **Metrics** tab and select the **residuals** and **predicted_true** charts if they are not already selected.

Review the charts which show the performance of the model. The chart compares the predicted values against the true values, and shows the residuals, the differences between predicted and actual values, as a histogram.

The **Predicted vs. True** chart should show a diagonal trend in which the predicted value correlates closely to the true value. The dotted line shows how a perfect model should perform. The closer the line of your model's average predicted value is to the dotted line, the better its performance. A histogram below the line chart shows the distribution of true values.

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/predicted-vs-true.png">
</p>

The **Residual Histogram** shows the frequency of residual value ranges. Residuals represent variance between predicted and true values that can't be explained by the model, in other words, errors. You should hope to see the most frequently occurring residual values clustered around zero. You want to small errors with fewer errors at the extreme ends of the scale.

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/residual-histogram.png">
</p>

5. Select the **Explanations** tab. Select an explanation ID and then select **Aggregate feature Importance**. This chart shows how much each feature in the dataset influences the label prediction, like this:

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/feature-importance.png">
</p>

## Deploy a model as a service
After you've used automated machine learning to train some models, you can deploy the best performing model as a service for client applications to use.

### Deploy a predictive service
In Azure Machine Learning, you can deploy a service as an Azure Container Instances (ACI) or to an Azure Kubernetes Service (AKS) cluster. For production scenarios, an AKS deployment is recommended, for which you must create an inference cluster compute target. In this exercise, you'll use an ACI service, which is a suitable deployment target for testing, and does not require you to create an inference cluster.

1. In [Azure Machine Learning studio](https://ml.azure.com/), on the **Automated ML** page, select the run for your automated machine learning experiment.
2. On the **Details** tab, select the algorithm name for the best model.
3. On the **Model** tab, select the **Deploy** button and use the **Deploy to web service** option to deploy the model with the following settings:
- **Name:** predict-rentals
- **Description:** Predict cycle rentals
- **Compute type:** Azure Container Instance
- **Enable authentication:** Selected
4. Wait for the deployment to start - this may take a few seconds. Then, in the **Model summary** section, observe the **Deploy status** for the **predict-rentals** service, which should be **Running**. Wait for this status to change to **Successful**, which may take some time. You may need to select **↻ Refresh** periodically.
5. In Azure Machine Learning studio, view the **Endpoints** page and select the **predict-rentals** real-time endpoint. Then select the **Consume** tab and note the following information there. If you do not see the **Consume** tab, the deployment is not completely finished - you will need to wait and refresh the page. You would need the information from the **Consume** tab to connect to your deployed service from a client application.
- The REST endpoint for your service
- The primary or secondary key for your service

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/endpoints-2.png">
</p>

### Test the deployed service
Now you can test your deployed service.
1. On the **Endpoints** page, open the **predict-rentals** real-time endpoint.
2. When the **predict-rentals** endpoint opens, view the **Test** tab.
3. In the input data pane, replace the template JSON with the following input data:
```
{
  "Inputs": { 
    "data": [
      {
        "day": 1,
        "mnth": 1,   
        "year": 2022,
        "season": 2,
        "holiday": 0,
        "weekday": 1,
        "workingday": 1,
        "weathersit": 2, 
        "temp": 0.3, 
        "atemp": 0.3,
        "hum": 0.3,
        "windspeed": 0.3 
      }
    ]    
  },   
  "GlobalParameters": 1.0
}
```
4. Click on the **Test** button.
5. Review the test results, which include a predicted number of rentals based on the input features. The test pane took the input data and used the model you trained to return the predicted number of rentals.

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/workaround-test.png">
</p>

Let's review what you have done. You used a dataset of historical bicycle rental data to train a model. The model predicts the number of bicycle rentals expected on a given day, based on seasonal and meteorological _features_. In this case, the _labels_ are number of bicycle rentals.

### Clean-up
The web service you created is hosted in an _Azure Container Instance_. If you don't intend to experiment with it further, you should delete the endpoint to avoid accruing unnecessary Azure usage.

1. In [Azure Machine Learning studio](https://ml.azure.com/), on the **Endpoints** tab, select the **predict-rentals** endpoint. Then select **Delete (🗑)** and confirm that you want to delete the endpoint.

Deleting the endpoint ensures your subscription won't be charged for the container instance in which it is hosted. You will however be charged a small amount for data storage as long as the Azure Machine Learning workspace exists in your subscription. If you have finished exploring Azure Machine Learning, you can delete the Azure Machine Learning workspace and associated resources. However, if you plan to complete any other labs in this series, you will need to recreate it.

To delete your workspace:
1. In the [Azure portal](https://portal.azure.com/), in the **Resource groups** page, open the resource group you specified when creating your Azure Machine Learning workspace.
2. Click **Delete resource group**, type the resource group name to confirm you want to delete it, and select **Delete**.

# Create a Regression Model with Azure Machine Learning designer
_Regression_ is a form of machine learning that is used to predict a numeric _label_ based on an item's _features_. For example, an automobile sales company might use the characteristics of a car (such as engine size, number of seats, mileage, and so on) to predict its likely selling price. In this case, the characteristics of the car are the features, and the selling price is the label.

_Regression_ is an example of a _supervised_ machine learning technique in which you train a model using data that includes both the features and known values for the label, so that the model learns to _fit_ the feature combinations to the label. Then, after training has been completed, you can use the trained model to predict labels for new items for which the label is unknown.

## Explore data
To train a regression model, you need a dataset that includes historical _features_, characteristics of the entity for which you want to make a prediction. You also need known _label_ values, the numeric value that you want to train a model to predict.

### Create a pipeline
To use the Azure Machine Learning designer, you create a pipeline that you use to train a machine learning model. This pipeline starts with the dataset from which you want to train the model.

1. In [Azure Machine Learning studio](https://ml.azure.com/), expand the left pane by selecting the three lines at the top left of the screen. View the **Designer** page (under **Author**), and select + to create a new pipeline.
2. At the top right-hand side of the screen, select **Settings**. If the **Settings** pane is not visible, select the **⚙** icon next to the pipeline name at the top.
3. In **Settings**, you must specify a compute target on which to run the pipeline. Under **Select compute type**, select **Compute cluster**. Then under **Select Azure ML compute-type**, select the compute cluster you created previously.
4. In **Settings**, under **Draft Details**, change the draft name (**Pipeline-Created-on-date**) to **Auto Price Training**.
5. Select the close icon on the top right of the **Settings** pane to close the pane.

### Add and explore a dataset
In this module, you train a regression model that predicts the price of an automobile based on its characteristics. Azure Machine Learning includes a sample dataset that you can use for this model.

1. Next to the pipeline name on the left, select the button >> to expand the panel if it is not already expanded. The panel should open by default to the **Asset Library** pane, indicated by the books icon at the top of the panel. Note that there is a search bar to locate assets. Below the **Tags** and **Filter** buttons, there are two icons next to each other. Hover your mouse over the first cylinder icon (on the left) to see that it represents **Data Assets**. Hover your mouse over the second chart icon (on the right) to see that it represents **Components**.

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/designer-asset-library-data.png">
</p>

2. Click on the cylinder icon for **Data Assets**. Drag the **Automobile price data (Raw)** dataset onto the canvas.
3. Right-click (Ctrl+click on a Mac) the **Automobile price data (Raw)** dataset on the canvas, and on the **Outputs** menu, click **Dataset output** on the _Preview data_ graph icon.
4. Review the schema of the data. Note that you can see the distributions of the various columns as histograms.
5. Scroll to the right of the dataset until you see the **Price** column, which is the label that your model predicts.
6. Select the column header for the **price** column and view the details that are displayed in the pane to the right. These include various statistics for the column values, and a histogram with the distribution of the column values.
7. Scroll back to the left and select the **normalized-losses** column header. Then review the statistics for this column. Note there are quite a few missing values in this column. Missing values limit the column's usefulness for predicting the **price** label so you might want to exclude it from training.
8. View the statistics for the **bore**, **stroke**, and **horsepower** columns. Note the number of missing values. These columns have fewer missing values than **normalized-losses**, so they might still be useful in predicting **price** once you exclude the rows where the values are missing from training.
9. Compare the values in the **stroke**, **peak-rpm**, and **city-mpg** columns. These columns are all measured in different scales, and it is possible that the larger values for **peak-rpm** might bias the training algorithm and create an over-dependency on this column compared to columns with lower values, such as **stroke**. Typically, data scientists mitigate this possible bias by _normalizing_ the numeric columns so they're on the similar scales.
10. Close the **Automobile price data (Raw) result visualization** window so that you can see the dataset on the canvas like this:

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/dataset.png">
</p>

### Add data transformations
You typically apply data transformations to prepare the data for modeling. In the case of the automobile price data, you add transformations to address the issues you identified when you explored the data.

1. In the **Asset Library** pane on the left, click on the squares icon to access **Components**, which contain a wide range of modules you can use for data transformation and model training. You can also use the search bar to quickly locate modules.

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/designer-asset-library-components.png">
</p>

2. Find the **Select Columns in Dataset** module and drag it to the canvas, below the **Automobile price data (Raw)** module. Then connect the output at the bottom of the **Automobile price data (Raw)** module to the input at the top of the **Select Columns in Dataset** module, like this:

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/dataset-select-columns.png">
</p>

3. Select the **Select Columns in Dataset** module, and in its **Settings** pane on the right, select **Edit column**. Then in the **Select columns** window, select **By name** and use the + links to add all columns other than **normalized-losses**, like this:

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/select-columns.png">
</p>

In the rest of this exercise, you go through steps to create a pipeline that looks like this:

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/data-transforms.png">
</p>

4. Find a **Clean Missing Data** module and place it under the **Select Columns in Dataset** module on the canvas. Then connect the output from the **Select Columns in Dataset** module to the input of the **Clean Missing Data** module.
5. Select the **Clean Missing Data** module, and in the settings pane on the right, click **Edit column**. Then in the **Select columns** window, select **With rules**, in the **Include** list select **Column names**, in the box of column names enter **bore**, **stroke**, and **horsepower** like this:

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/clean-missing-values.png">
</p>

6. With the **Clean Missing Data** module still selected, in the settings pane, set the following configuration settings:
- **Minimum missing value ratio:** 0.0
- **Maximum missing value ratio:** 1.0
- **Cleaning mode:** Remove entire row

7. Find a **Normalize Data** module and drag it to the canvas, below the **Clean Missing Data** module. Then connect the left-most output from the **Clean Missing Data** module to the input of the **Normalize Data** module.
8. Select the **Normalize Data** module and view its settings. Note that it requires you to specify the transformation method and the columns to be transformed. Then, set the transformation to **MinMax**. Apply a rule to edit the columns to include the following 

**Column names:**
- **symboling**
- **wheel-base**
- **length**
- **width**
- **height**
- **curb-weight**
- **engine-size**
- **bore**
- **stroke**
- **compression-ratio**
- **horsepower**
- **peak-rpm**
- **city-mpg**
- **highway-mpg**

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/normalize-rules.png">
</p>

### Run the pipeline
To apply your data transformations, you must run the pipeline as an experiment.

1. Ensure that your pipeline looks similar to this image:

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/data-transforms.png">
</p>

2. Select **Submit**, and run the pipeline as a new experiment named **mslearn-auto-training** on your compute cluster.
3. Wait for the run to finish, which might take 5 minutes or more.

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/completed-job.png">
</p>

Notice that the left hand panel is now on the **Submitted Jobs** pane. You will know when the run is complete because the status of the job will change to **Complete**.

4. When the run has completed, click on **Job Details**. You will be taken to another window which will show the modules like this:

<p align="center" width="100%">
    <img width="50%" src="https://github.com/cedricquitor/ml-ai-notebook/blob/main/images/normalize-complete.png">
</p>

### View the transformed data
The dataset is now prepared for model training.

1. Select the completed **Normalize Data** module, and in its **Settings** pane on the right, on the **Outputs + logs** tab, select the **Preview data** icon for the **Transformed dataset**.
2. View the data. Note that the **normalized-losses** column has been removed, all rows contain data for **bore**, **stroke**, and **horsepower**, and the numeric columns you selected have been normalized to a common scale.
3. Close the normalized data result visualization.

## Create and run a training pipeline
