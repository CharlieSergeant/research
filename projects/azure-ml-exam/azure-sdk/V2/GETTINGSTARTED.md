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
- [Azure ML Python SDK (V2)](https://pypi.org/project/azure-ai-ml/)
- [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest)
- [Azure CLI ML Ext](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-configure-cli?view=azureml-api-2&tabs=public)
- [CLI Command List](https://learn.microsoft.com/en-us/cli/azure/ml?view=azure-cli-latest)
- [Azure ML VS Code](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-manage-resources-vscode?view=azureml-api-2)
- [MLClient Class](https://learn.microsoft.com/en-us/python/api/azure-ai-ml/azure.ai.ml.mlclient?view=azure-python)

## Tutorials and Examples
- [Exercises](https://github.com/MicrosoftLearning/mslearn-azure-ml)
- [Examples](https://github.com/Azure/azureml-examples/tree/main/sdk/python)

```pip install azure-ai-ml```

## Azure ML Studio (Workspace)

Workspace: ```from azure.ai.ml import MLClient```
- Authenticated session with your Azure Subscription
- AZURE_SUBSCRIPTION_ID, AZURE_RESOURCE_GROUP, AZURE_WORKSPACE_NAME

```
from azure.ai.ml import MLClient
from azure.identity import DefaultAzureCredential

ml_client = MLClient(
    DefaultAzureCredential(), subscription_id, resource_group, workspace
)
```

## Command block

use the command block to run a step or job

```from azure.ai.ml import command```

```
# configure job
job = command(
    code="./src",
    command="python train.py",
    environment="AzureML-sklearn-0.24-ubuntu18.04-py37-cpu@latest",
    compute="aml-cluster",
    experiment_name="train-model"
)

# connect to workspace and submit job
returned_job = ml_client.create_or_update(job)
```