# OneLake Data Ingestion Methods  
  
This repository provides an overview of the various methods available for ingesting data into OneLake within Microsoft Fabric. The table below summarizes each method, including its description, processing frequency, and supported data sources.  
  
## Ingestion Methods Table  
  
| Icon                | Feature                | Description                                                                                          | Processing Frequency | Data Source Support                                                                                   |
|------------------------|------------------------|------------------------------------------------------------------------------------------------------|----------------------|------------------------------------------------------------------------------------------------------|
|![OneLake](icons/onelake.png) | [OneLake File Explorer](https://learn.microsoft.com/en-us/fabric/onelake/onelake-file-explorer)  | Integration with Windows File Explorer, allowing users to manually drag and drop files.              | Manual               | Any files and tables in Delta/Parquet format.                                                         |
|![Notebook](icons/notebook.png) | [API Access](https://learn.microsoft.com/en-us/fabric/onelake/onelake-access-api)             | Open access to OneLake through existing ADLS Gen2 APIs                                               | Varies by Application| Any application that can call OneLake via DFS APIs (e.g. Azure Databricks, Fabric Spark, Python, etc).|
|![Pipeline](icons/pipeline.png) | [Pipelines](https://learn.microsoft.com/en-us/fabric/data-factory/data-factory-overview#data-pipelines)              | Build complex workflows that can move PB-size data, and define sophisticated control flow pipelines. | Batch                | Various (~50 data sources).                                                                           |
|![Dataflow](icons/dataflow.png) | [Dataflows](https://learn.microsoft.com/en-us/fabric/data-factory/data-factory-overview#dataflows)              | Provide a low-code interface for ingesting data from hundreds of sources, transforming data using 300+ transformations. | Batch | Various (150+ data sources). |
|![Warehouse](icons/warehouse.png) | [Warehouse](https://learn.microsoft.com/en-us/fabric/data-warehouse/ingest-data-copy)              | Ingest data using the T-SQL COPY statement for high-throughput data ingestion from Azure storage.    | Batch                | External Azure Storage (Parquet and CSV).                                                             |
|![Shortcut](icons/shortcut.png) | [Shortcuts](https://learn.microsoft.com/en-us/fabric/onelake/onelake-shortcuts)              | Shortcuts act as symbolic links to other storage locations.                                          | Near Real-Time       | Internal OneLake locations, ADLS Gen2, Amazon S3, S3 Compatible, GCS, Dataverse                      |
|![Mirroring](icons/mirror.png) | [Mirroring](https://learn.microsoft.com/en-us/fabric/database/mirrored-database/overview)              | Replicates data and metadata into OneLake, converting it to an analytics-ready Parquet format.       | Near Real-Time       | Azure Cosmos DB, Azure Databricks Unity Catalog, Azure SQL DB, Azure SQL MI, Fabric SQL DB, Snowflake |
|![Mirroring](icons/mirror.png) | [Open Mirroring](https://learn.microsoft.com/en-us/fabric/database/mirrored-database/open-mirroring)         | Enables any application to write change data directly into a mirrored database in Fabric.            | Near Real-Time       | Supports any data source that can write to a OneLake landing zone in the specified format.           |
|![Event Stream](icons/eventstream.png) | [Event Streams](https://learn.microsoft.com/en-us/fabric/real-time-intelligence/event-streams/overview)          | Real-time ingestion and processing of events using a no-code interface.                              | Near Real-Time       | Various (e.g. Azure Event Hubs, Azure IoT Hub, Apache Kafka, Azure SQL DB (CDC), etc)                |
