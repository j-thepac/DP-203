# Azure DP-203
[Azure Study Material](https://learn.microsoft.com/en-us/training/courses/dp-203t00)

## Topics

### 1. Get started with data engineering on Azure
  #### Introduction to data engineering on Azure
  #### Introduction to Azure Data Lake Storage Gen2
    - Data Lake Storage Uses - Security (ACL and POSIX) , Performance , Data Redundancy LRS and GRS
    - Blob ( flat namespace) vs Gen2 ( hierarchical namespace - Folders) 
    - Create Gen2 ? 
    - When to use which one ?"
  #### Introduction to Azure Synapse Analytics

## 2. Build data analytics solutions using Azure Synapse serverless SQL pools
  #### 1. Use Azure Synapse serverless SQL pool to query files in a data lake
    - serverless vs Dedicated
    - synax for serveless SQL - Openrowset, External DataSource , External File Format
   #### 2. Use Azure Synapse serverless SQL pools to transform data in a data lake
    - CETAS - with(target ) as select * from Source
    - create Pipelines + CETAS + SPROC , 
  ####  3. Create a lake database in Azure Synapse Analytics
    - Authentication: Anon (no auth ), SAS ( token) , Managed Identity (One rsrc gives authentication to other ), user Identity - (MFA)
    - Access control model = RBAC (assign roles to users, groups, or service principals.), ACL ( granular files , Foldrs )
    - Permission in DB
   #### 4. Secure data and manage users in Azure Synapse serverless SQL pools"

## 3. Perform data engineering with Azure Synapse Apache Spark Pools
  #### Analyze data with Apache Spark in Azure Synapse Analytics
    -  spark intro , read data from abfss + schema +header
    -  Notebook ,SQL in notebook 
   #### Transform data with Spark in Azure Synapse Analytics
    -  saveAsTable(permanent) / Catalog table vs CreateOrReplaceTempView (temp) ,Drop saveAsTable
    -  metastore , External tables 
   #### Use Delta Lake in Azure Synapse Analytics"
    -  Delta Lake 
    -  data lakehouse = Delta Lake + SQL+CRUDE
    -  External (path) vs Managed tables (or internal tables)
    -  CRUDE delta , Timetravel x 2 , 
    -  Create Catalog Table , Schema
    -  Streaming Data , Spark Structured Streaming,spark.readStream
    -  Delta Lake table as a streaming source and streaming sink
    -  Excercise to Create DB"

## 4. Transfer and transform data with Azure Synapse Analytics pipelines
  #### Build a data pipeline in Azure Synapse Analytics
    -  Integrration Runtime , LinkedService,Dataflow
   ####  Use Spark Notebooks in an Azure Synapse Pipeline"
    -  DataFlow 
    -  Notebook"

## 5. Implement a Data Analytics Solution with Azure Synapse Analytics
  #### Introduction to Azure Synapse Analytics
  #### Use Azure Synapse serverless SQL pool to query files in a data lake
  ####  Analyze data with Apache Spark in Azure Synapse Analytics
  #### Use Delta Lake in Azure Synapse Analytics
  ####  Analyze data in a relational data warehouse
  ####  Build a data pipeline in Azure Synapse Analytics"

## 6. Work with Data Warehouses using Azure Synapse Analytics
  #### Analyze data in a relational data warehouse
    -  Serverless comes along with Synapse, Dedicated SQL can be provisioned in Synapse > SQL pools > New 
    -  Used for - Dim ,Fact ,star ,Snow Flake Schema , FK ,PK , normalized ( reduce duplication)
    -  Create Datwarehouse , dedicated SQL pools , 
   #### Load data into a relational data warehouse
    -  Cluster Index=CLUSTERED COLUMNSTORE INDEX ,CLUSTERED INDEX ,HEAP (#memory-temp table only)
    -  NonClusterted Index = create index i on T (c1) -- create clustered index i on T (c1)
    -  Partition = ()
    -  Distribution (Data stored in Nodes ) - Hash (c1,c2), RoundRobin , Replicated 
    -  Dedicated SQL don't support foreign key and unique constraints 
    -  SELECT...INTO vs. CTAS (SQL ) vs CETAS (gen2) 
    -  create Table T (C1 INT IDENTITY(1,1) NOT NULL). --Skey auto Increament
    -  Type0,1,2 , Code for all. Code to load Fact
   #### Manage and monitor data warehouse activities in Azure Synapse Analytics
    - Auto Scaling - Spark , Dedicated SQL 
    -  Paue , Autp Pause - Spark
    -  Dedicated SQL pools Scale , Apache Spark Pool Scaling, Pause , 
    -  Create Worload Importance in Query - Dedicated SQL(WORKLOAD CLASSIFIER)
    -  Azure Advsior
    -  List of sys.views in dedicated SQL - ( Dynamic Management Views for Query Debugging )
   #### Secure a data warehouse in Azure Synapse Analytics"
    -  Firewalls , Preivate Endpoints , Virtual Network ,Conditional Access
    -  EntaID, Managed Identities , SQL Authentication ,SAS
    -  Column / Row level Security (silent filtering) (Dedicated SQL )
    -  Dynamic Masking (Dedicated SQL 
    -  Dynamic Masking - CLI ) [AzSqlDatabaseDataMaskingPolicy*2 ,x_ AzSqlDatabaseDataMaskingRule *3] , API
    -  Encryption"

## 7. Work with Hybrid Transactional and Analytical Processing Solutions using Azure Synapse Analytics
  #### Plan hybrid transactional and analytical processing using Azure Synapse Analytics
  -  Azure Synapse Link ( Auto Sync )- Cosmos ,Azure SQL/Server and Dataverse called analytical store support -> Dedicated SQL
  #### Implement Azure Synapse Link with Azure Cosmos DB
  ####  Implement Azure Synapse Link for SQL"
  -  Azure SQL/Server > Gen2 > Dedicated SQL"

## 8. Implement a Data Streaming Solution with Azure Stream Analytics
  #### Get started with Azure Stream Analytics
    -  temporal (time-based) 
    -  Azure Stream Analytics , Cluster 
    -  stream processing defined using SQL Queries
    -  temporal windowing functions x 5 - , Tumbling ,Hopping ,Sliding , Session,, Snapshot
    -  Uses Stream Analytics job Paas 
  ####  Ingest streaming data using Azure Stream Analytics and Azure Synapse Analytics
    -  Azure Event Hubs or Azure IoT Hub(capture Realtime data)-> Azure Stream Analytics (The captured data transformed) --> Data loaded to gen2 / Dedicated using Synapse 
    - Create resource and Turn On Dedicated SQL pool in Synapse for Azure Stream Analytics to function
  ####  Visualize real-time data with Azure Stream Analytics and Power BI"
    -  U can also connect Azure Stream Analytics directly to PowerBI"

## 9. Implement a data lakehouse analytics solution with Azure Databricks\
  #### Explore Azure Databricks
    -  Databricks (same as Synapse Notebooks ) - SQL , Spark, ML features 
    - Unity Catalog ,Microsoft Purview ( software-as-a-service (SaaS))- data governance similar to Lean IX
    -  Databricks Uses Delta Lake
   #### Perform data analysis with Azure Databricks
   #### Use Apache Spark in Azure Databricks
   #### Manage data with Delta Lake
    -  Schema Enformcement is automatically Done
    -  Uses Merge , Update , RestoreToVersion ,see history 
   #### Build data pipelines with Delta Live Tables
    -  Delta Live Tables (DLT) similar to Synapse Dataflows
   #### Deploy workloads with Azure Databricks Workflows"
    -  Azure Databricks Workflows similar to Synapse Pipelines"

## 10. Govern data across an enterprise
#### Introduction to Microsoft Purview
#### Discover trusted data using Microsoft Purview
#### Catalog data artifacts by using Microsoft Purview
#### Manage Power BI assets by using Microsoft Purview
#### Integrate Microsoft Purview and Azure Synapse Analytics"
---------------
