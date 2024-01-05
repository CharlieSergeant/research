# Azure Machine Learning Specialty Exam Reference Guide

## 1. Manage Azure resources for machine learning (25-30%)

### Create an Azure Machine Learning workspace
- Create an Azure Machine Learning workspace
- Configure workspace settings
- Manage a workspace by using Azure Machine Learning studio

### Manage data in an Azure Machine Learning workspace
- Select Azure storage resources
- Register and maintain datastores
- Create and manage datasets

### Manage compute for experiments in Azure Machine Learning
- Determine the appropriate compute specifications for a training workload
- Create compute targets for experiments and training
- Configure Attached Compute resources including Azure Databricks
- Monitor compute utilization

### Implement security and access control in Azure Machine Learning
- Determine access requirements and map requirements to built-in roles
- Create custom roles
- Manage role membership
- Manage credentials by using Azure Key Vault

### Set up an Azure Machine Learning development environment
- Create compute instances
- Share compute instances
- Access Azure Machine Learning workspaces from other development environments

### Set up an Azure Databricks workspace
- Create an Azure Databricks workspace
- Create an Azure Databricks cluster
- Create and run notebooks in Azure Databricks
- Link an Azure Databricks workspace to an Azure Machine Learning workspace

## 2. Run experiments and train models (20-25%)

### Create models by using the Azure Machine Learning designer
- Create a training pipeline by using Azure Machine Learning designer
- Ingest data in a designer pipeline
- Use designer modules to define a pipeline data flow
- Use custom code modules in designer

### Run model training scripts
- Create and run an experiment by using the Azure Machine Learning SDK
- Configure run settings for a script
- Consume data from a dataset in an experiment by using the Azure Machine Learning SDK
- Run a training script on Azure Databricks compute
- Run code to train a model in an Azure Databricks notebook

### Generate metrics from an experiment run
- Log metrics from an experiment run
- Retrieve and view experiment outputs
- Use logs to troubleshoot experiment run errors
- Use MLflow to track experiments
- Track experiments running in Azure Databricks

### Use Automated Machine Learning to create optimal models
- Use the Automated ML interface in Azure Machine Learning studio
- Use Automated ML from the Azure Machine Learning SDK
- Select pre-processing options
- Select the algorithms to be searched
- Define a primary metric
- Get data for an Automated ML run and retrieve the best model

### Tune hyperparameters with Azure Machine Learning
- Select a sampling method
- Define the search space
- Define the primary metric
- Define early termination options
- Find the model that has optimal hyperparameter values

## 3. Azure Machine Learning Specialty Exam Reference Guide

## Deploy and operationalize machine learning solutions (35-40%)

### Select compute for model deployment
- Consider security for deployed services
- Evaluate compute options for deployment

### Deploy a model as a service
- Configure deployment settings
- Deploy a registered model
- Deploy a model trained in Azure Databricks to an Azure Machine Learning endpoint
- Consume a deployed service
- Troubleshoot deployment container issues

### Manage models in Azure Machine Learning
- Register a trained model
- Monitor model usage
- Monitor data drift

### Create an Azure Machine Learning pipeline for batch inferencing
- Configure a ParallelRunStep
- Configure compute for a batch inferencing pipeline
- Publish a batch inferencing pipeline
- Run a batch inferencing pipeline and obtain outputs
- Obtain outputs from a ParallelRunStep

### Publish an Azure Machine Learning designer pipeline as a web service
- Create a target compute resource
- Configure an inference pipeline
- Consume a deployed endpoint

### Implement pipelines by using the Azure Machine Learning SDK
- Create a pipeline
- Pass data between steps in a pipeline
- Run a pipeline
- Monitor pipeline runs

### Apply ML Ops practices
- Trigger an Azure Machine Learning pipeline from Azure DevOps
- Automate model retraining based on new data additions or data changes
- Refactor notebooks into scripts
- Implement source control for scripts

## 4. Implement responsible machine learning (5-10%)

### Use model explainers to interpret models
- Select a model interpreter
- Generate feature importance data

### Describe fairness considerations for models
- Evaluate model fairness based on prediction disparity
- Mitigate model unfairness

### Describe privacy considerations for data
- Describe principles of differential privacy
- Specify acceptable levels of noise in data and the effects on privacy