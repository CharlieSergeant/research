# Azure Machine Learning Specialty Exam Reference Guide

## Manage Azure resources for machine learning (25-30%)

### Create an Azure Machine Learning workspace
- [Create an Azure Machine Learning workspace](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-manage-workspace?tabs=python)
- [Configure workspace settings](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-configure-environment?tabs=python)
- [Manage a workspace in Azure Machine Learning studio](https://docs.microsoft.com/en-us/azure/machine-learning/overview-what-is-ml-studio)

### Manage data in an Azure Machine Learning workspace
- [Select Azure storage resources](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-access-data)
- [Register and maintain datastores](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-access-data#register-datastore)
- [Create and manage datasets](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-register-datasets)

### Manage compute for experiments in Azure Machine Learning
- [Determine compute specifications](https://docs.microsoft.com/en-us/azure/machine-learning/concept-compute-target)
- [Create compute targets](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-attach-compute-studio)
- [Configure Attached Compute resources including Azure Databricks](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-use-mlcompute)
- [Monitor compute utilization](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-monitor)

### Implement security and access control in Azure Machine Learning
- [Determine access requirements](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-assign-roles)
- [Create custom roles](https://docs.microsoft.com/en-us/azure/role-based-access-control/custom-roles)
- [Manage role membership](https://docs.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal)
- [Manage credentials with Azure Key Vault](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-use-credentials)

### Set up an Azure Machine Learning development environment
- [Create compute instances](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-attach-compute-studio)
- [Share compute instances](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-attach-compute-studio#share)
- [Access Azure Machine Learning workspaces from other development environments](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-use-mlflow)

### Set up an Azure Databricks workspace
- [Create an Azure Databricks workspace](https://docs.microsoft.com/en-us/azure/databricks/workspace/resource-settings/workspace-resource-settings#workspace-administration)
- [Create an Azure Databricks cluster](https://docs.microsoft.com/en-us/azure/databricks/clusters/clusters-create)
- [Create and run notebooks in Azure Databricks](https://docs.microsoft.com/en-us/azure/databricks/notebooks/notebooks-manage)
- [Link Azure Databricks to Azure Machine Learning](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-use-mlflow#mlflow-experiments)

## Run experiments and train models (20-25%)

### Create models by using the Azure Machine Learning designer
- [Create a training pipeline](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-your-first-pipeline)
- [Ingest data in a designer pipeline](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-your-first-pipeline#data-ingestion)
- [Use designer modules to define a pipeline data flow](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-your-first-pipeline#pipeline-data-flow)
- [Use custom code modules in designer](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-your-first-pipeline#add-python-script)

### Run model training scripts
- [Create and run an experiment by using the Azure Machine Learning SDK](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-your-first-experiment)
- [Configure run settings for a script](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-train-cli)
- [Consume data from a dataset in an experiment](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-your-first-experiment#train-a-model)
- [run a training script on Azure Databricks compute](https://github.com/Azure/MachineLearningNotebooks/blob/master/how-to-use-azureml/machine-learning-pipelines/intro-to-pipelines/aml-pipelines-use-databricks-as-compute-target.ipynb)
- [run code to train a model in an Azure Databricks notebook](https://learn.microsoft.com/en-us/azure/databricks/machine-learning/train-model/)

### Generate metrics from an experiment run
- [Log metrics from an experiment run](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-track-experiments)
- [Retrieve and view experiment outputs](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-track-experiments#explore-outputs)
- [Use logs to troubleshoot experiment run errors](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-debug-visual-studio-code)
- [Use MLflow to track experiments](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-use-mlflow)
- [Track expirements running in Azure Databricks](https://learn.microsoft.com/en-us/azure/databricks/mlflow/tracking#access-the-mlflow-tracking-server-from-outside-azure-databricks)

### Use Automated Machine Learning to create optimal models
- [Use Automated ML interface in Azure Machine Learning studio](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-portal-experiments#automated-machine-learning)
- [Use Automated ML from the Azure Machine Learning SDK](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-portal-experiments#automated-machine-learning-sdk)
- [Select pre-processing options](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-portal-experiments#pre-processing-options)
- [Select algorithms to be searched](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-portal-experiments#automated-ml-configuration)
- [Define a primary metric](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-portal-experiments#configure-automated-ml)
- [Get data for an Automated ML run retrieve the best model](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-portal-experiments#configure-automated-ml)

### Tune hyperparameters with Azure Machine Learning
- [Select a sampling method](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-tune-hyperparameters#random-sampling)
- [Define the search space](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-tune-hyperparameters#search-spaces)
- [Define the primary metric](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-tune-hyperparameters#primary-metric)
- [Define early termination options](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-tune-hyperparameters#early-termination)
- [Find the model that has optimal hyperparameter values](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-tune-hyperparameters#evaluate)

## Deploy and operationalize machine learning solutions (35-40%)

### Select compute for model deployment
- [Consider security for deployed services](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-secure-web-service)
- [Evaluate compute options for deployment](https://docs.microsoft.com/en-us/azure/machine-learning/concept-compute-instance)

### Deploy a model as a service
- [Configure deployment settings](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-deploy-azure-kubernetes-service)
- [Deploy a registered model](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-deploy-azure-kubernetes-service#deploy-automl-model)
- [Deploy a model trained in Azure Databricks to an Azure Machine Learning endpoint](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-deploy-azure-kubernetes-service#deploy-automl-model)
- [Consume a deployed service](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-consume-web-service)
- [Troubleshoot deployment container issues](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-troubleshoot-deployment)

### Manage models in Azure Machine Learning
- [Register a trained model](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-deploy-and-where)
- [Monitor model usage](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-enable-data-collection)
- [Monitor data drift](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-monitor-data-drift)

### Create an Azure Machine Learning pipeline for batch inferencing
- [Configure a ParallelRunStep](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-machine-learning-pipelines)
- [Configure compute for a batch inferencing pipeline](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-machine-learning-pipelines#batch-inferencing-pipeline)
- [Publish a batch inferencing pipeline](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-machine-learning-pipelines)
- [Run a batch inferencing pipeline and obtain outputs](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-machine-learning-pipelines#run-the-pipeline)
- [Obtain outputs from a ParallelRunStep](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-machine-learning-pipelines#obtain-outputs)

### Publish an Azure Machine Learning designer pipeline as a web service
- [Create a target compute resource](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-portal-experiments#set-up)
- [Configure an inference pipeline](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-portal-experiments#inference-pipeline)
- [Consume a deployed endpoint](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-consume-web-service)

### Implement pipelines by using the Azure Machine Learning SDK
- [Create a pipeline](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-machine-learning-pipelines)
- [Pass data between steps in a pipeline](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-machine-learning-pipelines#pass-data-between-pipeline-steps)
- [Run a pipeline](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-machine-learning-pipelines#run-the-pipeline)
- [Monitor pipeline runs](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-machine-learning-pipelines#monitor-pipeline-runs)

### Apply ML Ops practices
- [Trigger an Azure Machine Learning pipeline from Azure DevOps](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-portal-experiments#set-up)
- [Automate model retraining based on new data additions or data changes](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-machine-learning-pipelines)
- [Refactor notebooks into scripts](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-refactor-to-script)
- [Implement source control for scripts](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-use-mlflow)

### Implement responsible machine learning (5-10%)

### Use model explainers to interpret models
- [Select a model interpreter](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-machine-learning-interpretability)
- [Generate feature importance data](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-machine-learning-interpretability)

### Describe fairness considerations for models
- [Evaluate model fairness based on prediction disparity](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-machine-learning-interpretability)
- [Mitigate model unfairness](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-machine-learning-interpretability)

### Describe privacy considerations for data
- [Describe principles of differential privacy](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-machine-learning-interpretability#privacy)
- [Specify acceptable levels of noise in data and the effects on privacy](https://docs.microsoft.com/en-us/azure/machine-learning)

## Memorize these libraries
- [Scikit Learn](https://scikit-learn.org/stable/): Modeling library
- [Azure ML Python SDK (V1)](https://pypi.org/project/azureml-core/)
- [Apache Spark](https://spark.apache.org/docs/latest/api/python/getting_started/index.html): distributed real-time, large scale data processing
- [MLFlow](https://mlflow.org/docs/latest/getting-started/index.html): end to end ML lifecycle management
- [DeltaLake](https://docs.delta.io/latest/quick-start.html): ACID transactions on spark, metadata handling


## Notes

Pretest link

https://home.pearsonvue.com/Clients/Microsoft/Online-proctored.aspx

https://docs.microsoft.com/en-us/learn/certifications/certification-exams#exam-formats-and-question-types

Cert must be renewed yearly but dont have to retake the whole exam. Its a shorter open book test that highlights some of the new features that have come out in the field
 
 