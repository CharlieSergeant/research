## Datastores

Encapsulates the information required to connect to data sources.

### [Types](https://learn.microsoft.com/en-us/azure/machine-learning/concept-data?view=azureml-api-2)
- Azure Blob Container
- Azure File Share
- Azure Data Lake Gen1
- Azure Data Lake Gen2

### Ingest
- Snowflake
- Amazon S3
- Azure SQL DB

### Create Dataset

```
from azure.ai.ml.entities import Data
from azure.ai.ml.constants import AssetTypes

my_path = '<supported-path>'

my_data = Data(
    path=my_path,
    type=AssetTypes.URI_FILE,
    description="<description>",
    name="<name>",
    version="<version>"
)

ml_client.data.create_or_update(my_data)
```


### Create MLTable

```
from azure.ai.ml.constants import AssetTypes
from azure.ai.ml import Input

my_training_data_input = Input(type=AssetTypes.MLTABLE, path="azureml:input-data-automl:1")
```

https://github.com/MicrosoftLearning/mslearn-azure-ml/blob/main/Labs/03/Work%20with%20data.ipynb