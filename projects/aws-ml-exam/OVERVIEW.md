## AWS Machine Learning Specialty Exam Reference Guide

### Exam Content Domains and Weightings:

- **Domain 1: Data Engineering (20%)**
- **Domain 2: Exploratory Data Analysis (24%)**
- **Domain 3: Modeling (36%)**
- **Domain 4: Machine Learning Implementation and Operations (20%)**

---

### Domain 1: Data Engineering

**Task Statement 1.1: Create data repositories for ML.**
- Identify data sources: [AWS Data Sources](https://aws.amazon.com/products/databases/)
- Determine storage mediums: [Amazon S3](https://aws.amazon.com/s3/), [Amazon EFS](https://aws.amazon.com/efs/), [Amazon EBS](https://aws.amazon.com/ebs/)

**Task Statement 1.2: Identify and implement a data ingestion solution.**
- Identify data job styles and job types: Batch load, Streaming
- Orchestrate data ingestion pipelines using:
  - [Amazon Kinesis](https://aws.amazon.com/kinesis/)
  - [Amazon Kinesis Data Analytics](https://aws.amazon.com/kinesis/data-analytics/)
  - [Amazon Kinesis Data Firehose](https://aws.amazon.com/kinesis/data-firehose/)
  - [Amazon EMR](https://aws.amazon.com/emr/)
  - [AWS Glue](https://aws.amazon.com/glue/)
- Schedule jobs

**Task Statement 1.3: Identify and implement a data transformation solution.**
- Transform data in transit using:
  - [AWS Glue](https://aws.amazon.com/glue/)
  - [Amazon EMR](https://aws.amazon.com/emr/)
  - [AWS Batch](https://aws.amazon.com/batch/)
- Handle ML-specific data using MapReduce:
  - [Apache Hadoop](https://hadoop.apache.org/)
  - [Apache Spark](https://spark.apache.org/)
  - [Apache Hive](https://hive.apache.org/)

### Domain 2: Exploratory Data Analysis

**Task Statement 2.1: Sanitize and prepare data for modeling.**
- Identify and handle missing data, corrupt data, and stop words.
- Format, normalize, augment, and scale data.
- Determine whether there is sufficient labeled data:
  - Identify mitigation strategies.
  - Use data labeling tools: [Amazon Mechanical Turk](https://www.mturk.com/)

**Task Statement 2.2: Perform feature engineering.**
- Identify and extract features from datasets, including text, speech, image, and public datasets.
- Analyze and evaluate feature engineering concepts: Binning, Tokenization, Outliers, Synthetic Features, One-hot Encoding, Dimensionality Reduction.

**Task Statement 2.3: Analyze and visualize data for ML.**
- Create graphs: Scatter plots, Time series, Histograms, Box plots.
- Interpret descriptive statistics: Correlation, Summary Statistics, P-value.
- Perform cluster analysis: Hierarchical, Diagnosis, Elbow Plot, Cluster Size.

### Domain 3: Modeling

**Task Statement 3.1: Frame business problems as ML problems.**
- Determine when to use and when not to use ML.
- Know the difference between supervised and unsupervised learning.
- Select from among classification, regression, forecasting, clustering, and recommendation models.

**Task Statement 3.2: Select the appropriate model(s) for a given ML problem.**
- XGBoost, Logistic Regression, K-means, Linear Regression, Decision Trees, Random Forests, RNN, CNN, Ensemble, Transfer Learning.
- Express the intuition behind models.

**Task Statement 3.3: Train ML models.**
- Split data between training and validation using cross-validation.
- Understand optimization techniques for ML training: Gradient Descent, Loss Functions, Convergence.
- Choose appropriate compute resources: GPU or CPU, Distributed or Non-distributed.
- Choose appropriate compute platforms: Spark or Non-Spark.
- Update and retrain models: Batch or Real-time/Online.

**Task Statement 3.4: Perform hyperparameter optimization.**
- Perform regularization: Drop out, L1/L2.
- Perform cross-validation.
- Initialize models.
- Understand neural network architecture: Layers and Nodes, Learning Rate, Activation Functions.
- Understand tree-based models: Number of Trees, Number of Levels.
- Understand linear models: Learning Rate.

**Task Statement 3.5: Evaluate ML models.**
- Avoid overfitting or underfitting: Detect and handle bias and variance.
- Evaluate metrics: AUC-ROC, Accuracy, Precision, Recall, RMSE, F1 Score.
- Interpret confusion matrices.
- Perform offline and online model evaluation: A/B Testing.
- Compare models by using metrics: Time to train a model, Quality of model, Engineering costs.
- Perform cross-validation.

### Domain 4: Machine Learning Implementation and Operations

**Task Statement 4.1: Build ML solutions for performance, availability, scalability, resiliency, and fault tolerance.**
- Log and monitor AWS environments using:
  - [AWS CloudTrail](https://aws.amazon.com/cloudtrail/)
  - [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/)
- Build error monitoring solutions.
- Deploy to multiple AWS Regions and multiple Availability Zones.
- Create AMIs and golden images.
- Create Docker containers.
- Deploy Auto Scaling groups.
- Rightsizing resources: Instances, Provisioned IOPS, Volumes.
- Perform load balancing.
- Follow AWS best practices.

**Task Statement 4.2: Recommend and implement the appropriate ML services and features for a given problem.**
- ML on AWS (application services):
  - [Amazon Polly](https://aws.amazon.com/polly/)
  - [Amazon Lex](https://aws.amazon.com/lex/)
  - [Amazon Transcribe](https://aws.amazon.com/transcribe/)
- Understand AWS service quotas.
- Determine when to build custom models and when to use Amazon SageMaker built-in algorithms.
- Understand AWS infrastructure: Instance types and cost considerations.
- Use Spot Instances to train deep learning models by using AWS Batch.

**Task Statement 4.3: Apply basic AWS security practices to ML solutions.**
- [AWS Identity and Access Management (IAM)](https://aws.amazon.com/iam/)
- S3 bucket policies
- Security groups
- VPCs
- Encryption and anonymization

**Task Statement 4.4: Deploy and operationalize ML solutions.**
- Expose endpoints and interact with them.
- Understand ML models.
- Perform A/B testing.
- Retrain pipelines.
- Debug and troubleshoot ML models:
  - Detect and mitigate drops in performance.
  - Monitor performance of the model.

---

### Appendix

**Technologies and concepts that might appear on the exam**
The following list contains technologies and concepts that might appear on the exam. This list is non-exhaustive and is subject to change. The order and placement of the items in this list are no indication of their relative weight or importance on the exam:

- Ingestion/collection
- Processing/ETL
- Data analysis/visualization
- Model training
- Model deployment/inference
- Operationalizing ML
- AWS ML application services
- Language relevant to ML (e.g., Python, Java, Scala, R, SQL)
- Notebooks and integrated development environments (IDEs)



**In-scope AWS services and features**
The following list contains AWS services and features that are in scope for the exam. This list is non-exhaustive and is subject to change:

- **Analytics:**
  - [Amazon Athena](https://aws.amazon.com/athena/)
  - [Amazon EMR](https://aws.amazon.com/emr/)
  - [AWS Glue](https://aws.amazon.com/glue/)
  - [Amazon Kinesis](https://aws.amazon.com/kinesis/)
  - [Amazon Kinesis Data Analytics](https://aws.amazon.com/kinesis/data-analytics/)
  - [Amazon Kinesis Data Firehose](https://aws.amazon.com/kinesis/data-firehose/)
  - [Amazon Kinesis Data Streams](https://aws.amazon.com/kinesis/data-streams/)
  - [Amazon QuickSight](https://aws.amazon.com/quicksight/)

- **Compute:**
  - [AWS Batch](https://aws.amazon.com/batch/)
  - [Amazon EC2](https://aws.amazon.com/ec2/)
  - [AWS Lambda](https://aws.amazon.com/lambda/)

- **Containers:**
  - [Amazon Elastic Container Registry (Amazon ECR)](https://aws.amazon.com/ecr/)
  - [Amazon Elastic Container Service (Amazon ECS)](https://aws.amazon.com/ecs/)
  - [Amazon Elastic Kubernetes Service (Amazon EKS)](https://aws.amazon.com/eks/)
  - [AWS Fargate](https://aws.amazon.com/fargate/)

- **Database:**
  - [Amazon Redshift](https://aws.amazon.com/redshift/)

- **Internet of Things:**
  - [AWS IoT Greengrass](https://aws.amazon.com/iot-greengrass/)

- **Machine Learning:**
  - [Amazon Comprehend](https://aws.amazon.com/comprehend/)
  - [AWS Deep Learning AMIs (DLAMI)](https://aws.amazon.com/machine-learning/amis/)
  - [AWS DeepLens](https://aws.amazon.com/deeplens/)
  - [Amazon Forecast](https://aws.amazon.com/forecast/)
  - [Amazon Fraud Detector](https://aws.amazon.com/fraud-detector/)
  - [Amazon Lex](https://aws.amazon.com/lex/)
  - [Amazon Mechanical Turk](https://www.mturk.com/)
  - [Amazon Polly](https://aws.amazon.com/polly/)
  - [Amazon Rekognition](https://aws.amazon.com/rekognition/)
  - [Amazon SageMaker](https://aws.amazon.com/sagemaker/)
  - [Amazon Textract](https://aws.amazon.com/textract/)
  - [Amazon Transcribe](https://aws.amazon.com/transcribe/)
  - [Amazon Translate](https://aws.amazon.com/translate/)

- **Management and Governance:**
  - [AWS CloudTrail](https://aws.amazon.com/cloudtrail/)
  - [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/)

- **Networking and Content Delivery:**
  - [Amazon VPC](https://aws.amazon.com/vpc/)

- **Security, Identity, and Compliance:**
  - [AWS Identity and Access Management (IAM)](https://aws.amazon.com/iam/)

- **Storage:**
  - [Amazon Elastic Block Store (Amazon EBS)](https://aws.amazon.com/ebs/)
  - [Amazon Elastic File System (Amazon EFS)](https://aws.amazon.com/efs/)
  - [Amazon FSx](https://aws.amazon.com/fsx/)
  - [Amazon S3](https://aws.amazon.com/s3/)

---

Please note that this reference guide is based on the information provided for the AWS Machine Learning Specialty exam. Always make sure to check the official AWS documentation and exam guide for the most up-to-date and accurate information. Good luck with your exam preparation!