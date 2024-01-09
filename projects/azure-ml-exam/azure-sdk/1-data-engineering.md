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

### Create Tabular Dataset

```
from azureml.core import Dataset

blob_ds = ws.get_default_datastore()
csv_paths = [(blob_ds, 'data/files/current_data.csv'),
             (blob_ds, 'data/files/archive/*.csv')]
tab_ds = Dataset.Tabular.from_delimited_files(path=csv_paths)
tab_ds = tab_ds.register(workspace=ws, name='csv_table')
```

### Create File Dataset

```
from azureml.core import Dataset

blob_ds = ws.get_default_datastore()
file_ds = Dataset.File.from_files(path=(blob_ds, 'data/files/images/*.jpg'))
file_ds = file_ds.register(workspace=ws, name='img_files')
```

### Sample Use Case

Tabular data stored in parquet format partitioned by year, month

Dataset
- size: int
- weight: float
- price: float
- date: datetime
- date_year: int
- date_month: int


1. Save data temporary on local
2. Upload data to datastore

```
sales_path = "./sales.parquet"
datastore.upload_files([sales_path], ".", "sales_data", overwrite=True, show_progress=False)
```

3. Create dataset from files

```
from azureml.core import Dataset

dataset = Dataset.Tabular.from_delimited_files(path=(datastore, 'sales_data/*.parquet'))
```

4. Partition the dataset

```
partitioned_dataset = dataset.partition_by(partition_keys=['date_year', 'date_month'], target=(datastore, "partition_by_key_res"), name="sales_data")
```

5. Register the partitioned dataset

```
try:
    partitioned_dataset = partitioned_dataset.register(workspace=ws, 
                                        name='sales_data',
                                        description='sales data dataset',
                                        tags = {'format':'parquet'},
                                        create_new_version=False)
except Exception as ex:
    print(ex)
```

You can filter based on partition of the dataset to load specific files. In V1 of the Python SDK you can't specify a specific version and version management is done for you (1 -> 2 -> 3)

### Responsible AI
- https://learn.microsoft.com/en-us/azure/machine-learning/concept-responsible-ai?view=azureml-api-1#privacy-and-security

- https://fairlearn.org/v0.5.0/quickstart.html

