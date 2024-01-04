# **Task Statement 1.1: Create data repositories for ML**

This task focuses on creating the foundational data repositories needed for machine learning (ML) projects. To accomplish this, you need to identify the data sources and determine the appropriate storage mediums.

## **Identify Data Sources**

In the context of AWS, data sources refer to the different places or locations from which data can be collected and used for machine learning projects. Some common AWS data sources include:

- [AWS Databases](https://aws.amazon.com/products/databases/): AWS offers a variety of managed databases that can be used as data sources, such as Amazon RDS (Relational Database Service), Amazon DynamoDB (NoSQL database), and Amazon Aurora.
- [Amazon S3](https://aws.amazon.com/s3/): Amazon Simple Storage Service (S3) is an object storage service that allows you to store and retrieve any amount of data. It is commonly used as a data lake to store large volumes of unstructured or structured data.
- [Amazon Redshift](https://aws.amazon.com/redshift/): Amazon Redshift is a fully managed data warehousing service, which can be used to store and analyze large datasets for data analytics and business intelligence.
- [Amazon Kinesis](https://aws.amazon.com/kinesis/): Amazon Kinesis is a real-time data streaming service that can be used to ingest and process large streams of data from various sources, such as IoT devices, logs, and social media feeds.

## **Determine Storage Mediums**

Once you have identified the data sources, you need to determine the appropriate storage mediums based on the characteristics of your data and the requirements of your machine learning workloads. AWS provides several storage mediums that can be used for different purposes:

**Amazon S3 (Simple Storage Service)**

- Amazon S3 is an object storage service that allows you to store files in buckets. Each object in S3 has a unique key, which represents the full path to the object within the bucket.
- The maximum size of an individual object that can be stored in S3 is 5TB, making it suitable for large-scale data storage requirements.
- S3 is the backbone for many AWS Machine Learning services and is commonly used to create a data lake—a centralized repository for storing raw and processed data, accessible by multiple data consumers and ML workloads.
- One of the significant advantages of S3 is its virtually infinite size, as it automatically scales to accommodate any amount of data without requiring manual provisioning.
- S3 decouples storage from compute, enabling a centralized architecture for data storage, and supporting any file format, making it a versatile choice for handling diverse data types.
- Common file types, such as documents, images, videos, and data files, can be stored in S3, making it a suitable option for storing ML training datasets and model artifacts.

**S3 Data Partitioning**

- S3 supports a data partitioning pattern that helps speed up range queries on large datasets. The pattern is based on how data is organized in S3 bucket paths, such as `s3://bucket/year/month/day`. This allows for efficient querying and filtering based on specific criteria like date ranges.

**S3 Storage Tiers**

- Amazon S3 offers different storage tiers to cater to various access patterns and cost considerations. These tiers include:
  - [Frequently Accessed](https://aws.amazon.com/s3/storage-classes/#Frequent_Access): Suitable for frequently accessed data with low-latency requirements.
  - [Infrequently Accessed](https://aws.amazon.com/s3/storage-classes/#Infrequent_Access): Ideal for data that is accessed less frequently, with lower storage costs but slightly higher retrieval costs.
  - [Intelligent-Tiering](https://aws.amazon.com/s3/storage-classes/#Intelligent_Tiering): Automatically moves data between frequent and infrequent access tiers based on usage patterns, optimizing costs.
  - [Glacier](https://aws.amazon.com/glacier/): Designed for data archival, offering the lowest storage costs but with longer retrieval times.

**S3 Lifecycle Rules**

- S3 Lifecycle Rules allow you to automate data management tasks based on the age and access pattern of objects in S3 buckets. This includes transitioning objects between storage tiers and specifying expiration actions for data retention.

**S3 Encryption**

- Amazon S3 provides multiple options for encrypting data at rest and in transit, ensuring the security of sensitive information.
- Server-Side Encryption (SSE) options include SSE-S3, which uses S3-managed keys; SSE-KMS, which uses AWS Key Management Service (KMS) keys; and SSE-C, where the client manages the encryption keys.
- Additionally, S3 supports Client-Side Encryption, where data is encrypted before being uploaded to S3 using client-side encryption libraries.

**S3 Security**

- S3 security is managed through IAM (Identity and Access Management) policies that control access to S3 resources (buckets and objects).
- IAM policies consist of a set of rules that define what actions (API calls) are allowed or denied on specific resources.
- IAM policies are attached to IAM users, groups, or roles and determine the level of access they have to S3 resources.
- S3 also allows you to grant public access to a bucket or object if required, enforce encryption for objects uploaded, and grant access to another AWS account if needed.

**Networking - VPC Endpoint Gateway**

- VPC (Virtual Private Cloud) Endpoint Gateway allows traffic to stay within your VPC, enhancing security and minimizing data egress costs when private services like AWS SageMaker need to access S3 resources.

**Logging and Audit**

- S3 access logs can be stored in another S3 bucket, providing visibility into who accessed the S3 resources and when.
- API calls made to S3 can be logged in AWS CloudTrail, which provides an audit trail of all AWS API activities.

**Amazon EFS**: [Amazon Elastic File System (EFS)](https://aws.amazon.com/efs/) is a fully managed file storage service that can be mounted to multiple EC2 instances concurrently. It is suitable for workloads that require shared file access, such as distributed ML training jobs where multiple instances need to access the same data.

**Amazon EBS**: [Amazon Elastic Block Store (EBS)](https://aws.amazon.com/ebs/) provides block-level storage volumes that can be attached to EC2 instances. It is commonly used for boot volumes and block-level data storage for individual instances. While EBS volumes are attached to specific instances, they can still be used for persistent data storage in machine learning applications.

