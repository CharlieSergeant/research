# Resources

- Subscription: ```AZURE_SUBSCRIPTION_ID``` (Your Azure Subscription ID)
- Resource Group: ```AZURE_RESOURCE_GROUP``` 
- Workspace Name: ```AZURE_WORKSPACE_NAME``` (Your defined Azure ML Space Workspace)
- Region: ```AZURE_REGION```
- Account Url: ```AZURE_ACCOUNT_URL``` 
- Container: ```AZURE_CONTAINER_NAME``` (Container in Storage Account for blob storage)
- Storage Account: ```https://{AZURE_ACCOUNT_URL}/{AZURE_CONTAINER_NAME}``` (Blob Storage Reference Point)
- Azure Data Store Name: ```AZURE_DATASTORE_NAME``` (ML Data Blob Reference Point)
- Azure Compute Cluster: ```AZURE_COMPUTE_CLUSTER``` (Compute for training jobs)
- Azure Deploy Cluster: ```AZURE_DEPLOY_CLUSTER``` (Compute for endpoints)

Make a .env file and add in

```
AZURE_SUBSCRIPTION_ID=FILLIN
AZURE_RESOURCE_GROUP=FILLIN
AZURE_WORKSPACE_NAME=FILLIN
AZURE_REGION=FILLIN
AZURE_ACCOUNT_URL=FILLIN
AZURE_CONTAINER_NAME=FILLIN
AZURE_DATASTORE_NAME=FILLIN
AZURE_COMPUTE_CLUSTER=FILLIN
AZURE_DEPLOY_CLUSTER=FILLIN

PROJECT_NAME=FILLIN

MODEL_VERSION=V1
MODEL_RUN_DATE=FILLIN
MODEL_RUN_MODE=FILLIN
``` 

## Getting Started
- [python](https://www.python.org/downloads/)
- [Azure ML Python SDK (V1)](https://pypi.org/project/azureml-core/)
- [Azure ML Python SDK (V2)](https://pypi.org/project/azure-ai-ml/)
- [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest)
- [Azure CLI ML Ext](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-configure-cli?view=azureml-api-2&tabs=public)
- [Azure ML VS Code](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-manage-resources-vscode?view=azureml-api-2)

## Tutorials and Examples
- [Exercises](https://microsoftlearning.github.io/mslearn-dp100/)
- [Examples](https://github.com/Azure/MachineLearningNotebooks)
- [PacktTutorial](https://github.com/PacktPublishing/Mastering-Azure-Machine-Learning-Second-Edition)

## Azure ML Studio (Workspace)

### Expirement Setup

Workspace: ```from azureml.core import Workspace```
- Authenticated session with your Azure Subscription
- AZURE_SUBSCRIPTION_ID, AZURE_RESOURCE_GROUP, AZURE_WORKSPACE_NAME

Expirements: ```from azureml.core import Expirement```
- Logging
- Run
- Expirement LifeCycle
- Expirements will be registered and will show up in the ```Jobs``` tab

Run: ```from azureml.core import Run```
- Run context of an expirement

ScriptRunConfig: ```from azureml.core import ScriptRunContext```
- Python Script to be run during the experiment
- Submit the ScriptRunConfig to the expirement

Environment ```from azureml.core import Environment```
- Create a python environment for the expirement
- Pin dependancies and extend default environment
- Environments will be registered and will show up in the ```Environments``` tab 

Compute: ```from azureml.core.compute import ComputeTarget, AmlCompute```
- Compute Instances: Development workstations that data scientists can use to work with data and models. 
- Compute Clusters: Scalable clusters of virtual machines for on-demand processing of experiment code. 
- Inference Clusters: Deployment targets for predictive services that use your trained models. 
- Attached Compute: Links to existing Microsoft Azure compute resources, such as Virtual Machines or Azure Databricks clusters. 

### Data

Dataset: ```from azureml.core import Dataset```
- Versioned files inside of a Datastore
- Datasets will be registered to datapaths under the Datastore and can be created, updated or archived
- Datasets will be registered and will show up in the ```Data``` tab under Data assets

### Model

Model: ```from azureml.core import Model```
- Models will be registered and will show up in the ```Models``` tab

HyperparamterTuning: ```from azureml.train.hyperdrive import GridParameterSampling, HyperDriveConfig, PrimaryMetricGoal, choice```
- Allows the user to identify optimized hyperparameters 

AutoML: ```from azureml.train.automl import AutoMLConfig```
- Additional install ```pip install azureml-train-automl```
- Submit AutoMLConfig as an expirement
- On completion most AutoML jobs will generate the code used for building the automated pipeline for further investigation
- AutoML Jobs will be registered and show up in the ```Automated ML``` and ```Jobs``` tabs

Interpret: ```from interpret.ext.blackbox import TabularExplainer```
- Explain the influence that each feature contributes to the predicted label 
- Additional installs ```pip install azureml-explain-model azureml-interpret```
- Model Explanations will show up in the ```Jobs``` tab under Run Details -> Explanations

Deploy: ```from azureml.core.model import InferenceConfig```
- from azureml.core.webservice import AciWebservice, Webservice
- Deploy model as a webservice to an Inference Cluster
- Deployed models will be registered as an Endpoint and will show up under the ```Endpoints``` tab
- Realtime endpoints vs batch endpoints vs OpenAI endpoints

Monitoring:
- enable app insights on the deployed endpoint service to add monitoring. 
- Monitoring will show up on the Azure ML workspace home (not studio) on the Overview -> Application Insights -> Logs section

Data Drift: ```from azureml.datadrift import DataDriftDetector```
- Specify the features you want to monitor for data drift

### Orchestration 

Pipeline: ```from azureml.pipeline.core import Pipeline```
- encapsulates the sequence of steps needed to build a machine learning solution
    - prepare the data
    - train the model
- Pipelines will be registered and will show up in the ```Pipelines``` tab





