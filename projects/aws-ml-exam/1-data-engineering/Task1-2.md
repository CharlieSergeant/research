# **Task Statement 1.2: Identify and Implement a Data Ingestion Solution**

This task involves identifying data job styles and types for data ingestion and orchestrating data ingestion pipelines using various AWS services. The two main data job styles are batch load and streaming.

## **Data Job Styles and Job Types**

- Batch Load: A batch load is a data ingestion style where data is collected and processed in discrete groups or batches. It involves gathering data over a period of time and then processing the data all at once. Batch processing is often used when data can be collected and processed in non-real-time situations, and it is suitable for scenarios where lower latency is acceptable.

- Streaming: Streaming is a data ingestion style that involves processing data in real-time as it is generated or received. Streaming data is processed incrementally and immediately. It is commonly used for applications that require real-time data analysis and responsiveness.

## **Orchestrate Data Ingestion Pipelines**

To orchestrate data ingestion pipelines, several AWS services are available:

**Amazon Kinesis**

- [Amazon Kinesis](https://aws.amazon.com/kinesis/) is a suite of services for real-time data streaming and processing. It is an alternative to Apache Kafka and is commonly used for applications involving application logs, metrics, and IoT (Internet of Things) data.
- It supports streaming processing frameworks and automatically replicates data to ensure high availability and fault tolerance.

**Kinesis Streams**

- [Kinesis Streams](https://aws.amazon.com/kinesis/streams/) is a service that enables low-latency streaming data ingestion. Data is divided into shards for processing and storage.
- Data retention in Kinesis Streams is configurable, with a default retention period of 24 hours, which can be extended up to 365 days.
- Once data is inserted into Kinesis Streams, it cannot be deleted or modified.
- The maximum size of an individual record (data item) in Kinesis Streams is 1 MB.
- Producers can write up to 1 MB of data per second per shard, and consumers can read up to 2 MB of data per second per shard.
- Kinesis Streams is often used to create real-time machine learning algorithms that require low-latency data processing.

**Kinesis Firehose**

- [Kinesis Firehose](https://aws.amazon.com/kinesis/firehose/) is a service that simplifies the loading and delivery of streaming data. It automatically loads streaming data into storage destinations like Amazon S3, Amazon Redshift, ElasticSearch, and Splunk in near real-time.
- Kinesis Firehose supports automatic scaling based on the incoming data volume and supports compression to reduce storage costs.
- Unlike Kinesis Streams, Kinesis Firehose does not store data, making it suitable for applications where data storage is not a primary requirement.
- It is a fully managed service and is often used as an ingestion service for serverless data transformations.

**Kinesis Data Analytics**

- [Kinesis Data Analytics](https://aws.amazon.com/kinesis/data-analytics/) allows real-time ETL (Extract, Transform, Load) and machine learning algorithm processing on streaming data.
- It supports SQL or Apache Flink to write computations on streaming data.
- Data can be connected from various sources, including Kinesis Streams and Kinesis Firehose.
- Kinesis Data Analytics enables responsive analytics, stream ETL, and continuous metric generation on streaming data.

**Kinesis Video Stream**

- [Kinesis Video Streams](https://aws.amazon.com/kinesis/video-streams/) facilitates real-time video streaming for both producers and consumers.
- Producers can send video data, and consumers can use frameworks like MXNet and TensorFlow for processing and analysis.

**Kinesis Summary**

In summary, [Amazon Kinesis](https://aws.amazon.com/kinesis/) offers a comprehensive set of services for real-time data streaming and processing. Kinesis Streams and Kinesis Firehose provide different approaches to streaming data ingestion, with Streams offering low-latency and customizable retention periods, and Firehose providing automatic data loading into various storage destinations. Kinesis Data Analytics allows real-time ETL and processing of streaming data, while Kinesis Video Stream is designed for real-time video streaming applications. Understanding the capabilities and use cases of these services is crucial for implementing efficient data ingestion solutions in AWS Machine Learning projects.

Certainly, here's the summary for Amazon EMR, AWS Glue, and scheduling jobs:

**Amazon EMR (Elastic MapReduce)**

- [Amazon EMR](https://aws.amazon.com/emr/) is a cloud-native big data platform that facilitates processing and analyzing large datasets using popular frameworks like Apache Hadoop, Apache Spark, and more.
- EMR provides scalable clusters for different data processing tasks, making it suitable for tasks like data preprocessing, ETL (Extract, Transform, Load), data analysis, and machine learning.
- It allows you to focus on data analysis by automatically provisioning, scaling, and managing the underlying infrastructure.
- EMR can be used for batch and real-time processing of large datasets, making it a powerful tool for machine learning data preparation and processing.

**AWS Glue**

- [AWS Glue](https://aws.amazon.com/glue/) is a fully managed ETL (Extract, Transform, Load) service that helps automate the process of preparing and loading data for analytics.
- It provides a [Glue Data Catalog](https://aws.amazon.com/glue/features/data-catalog/) that acts as a metadata repository for all tables and datasets, allowing automated schema inference and versioning.
- Glue Crawlers automatically scan your data sources, such as S3, Redshift, and RDS, to infer schemas and partitions. These Crawlers can be scheduled or run on demand.
- The Glue Data Catalog integrates with other AWS services like Amazon Athena and Amazon Redshift, making it easier to query and analyze data.

**Scheduling Jobs**

- To manage data processing pipelines, AWS provides various scheduling options for automating tasks:
  - **Amazon EMR** supports job scheduling using applications like Apache Airflow. This allows you to define workflows and dependencies between different data processing tasks.
  - **AWS Glue** supports scheduling of ETL jobs. Jobs can be scheduled to run at specific intervals or in response to specific events, ensuring that data transformations are performed timely and automatically.
  - AWS offers **AWS Data Pipeline**, which is a web service for orchestrating and automating the movement and transformation of data between different AWS services and on-premises data sources.
  - **AWS Step Functions** provide visual workflows to orchestrate multiple AWS services, including data processing steps. This service allows you to build, deploy, and manage applications with multiple components and long-running workflows.







