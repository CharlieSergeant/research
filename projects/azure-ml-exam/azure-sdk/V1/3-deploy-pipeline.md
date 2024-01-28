## Deploy Pipeline

Need to have ```init() and run(data) ``` functions in an entrypoint script

### EntryPoint

#### init()

Initialize the trained model

```
import os
import numpy as np
from azureml.core import Model
import joblib

def init():
    # Runs when the pipeline step is initialized
    global model

    # load the model
    model_path = Model.get_model_path('classification_model')
    model = joblib.load(model_path)
```

#### run(data)

Run the predict on the model and perform any needed preprocessing and postprocessing logic 

```
def run(data):
    # Simple simple run function for model
    return model.predict(data)
```

### Batch Inference Pipeline

Example: Sales data engineering pipeline is updated nightly to our datastore dataset called ```sales_data```

A model is trained on the sales data and deployed as an endpoint on a AKS cluster

We would like to analyze how the model is preforming on new data since its train date. We schedule a weekly batch inference pipeline to track performance. Once performance dips past a given metric threshold we can rerun our train pipeline

1. Create new pipeline leveraging a ParallelRunStep
2. Run the pipeline
3. Publish the pipeline as an endpoint
4. Setup Batch Inference Schedule

### [Model Monitoring](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-monitor-online-endpoints?view=azureml-api-2)

### [Data Drift](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-enable-data-collection?view=azureml-api-1)