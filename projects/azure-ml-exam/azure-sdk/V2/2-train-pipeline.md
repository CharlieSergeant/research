## Train Pipelines

https://github.com/Azure/azureml-examples/blob/main/tutorials/e2e-ds-experience/e2e-ml-workflow.ipynb

https://github.com/MicrosoftLearning/mslearn-azure-ml/blob/main/Labs/04/Work%20with%20compute.ipynb

### Reuse Pipeline Steps

These are called components. These steps allow caching and reuse features to help reduce time

1. Data Preparation
    - Selecting Columns
    - Splitting Data
2. Training
    - Algorithm Selection
    - ML Framework type (SKLearn, Keras, PyTorch)
3. Hyperparameter Tuning
    - Search Spaces

### [HPO](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-tune-hyperparameters?view=azureml-api-2)

```from azure.ai.ml.sweep import Choice, Normal```

Sampling Types
- GridParameterSampling 
- RandomParameterSampling
- BayesianParameterSampling
- SobalParameterSampling

```
from azure.ai.ml.sweep import Uniform, Choice

command_job_for_sweep = job(
    batch_size=Choice(values=[16, 32, 64]),    
    learning_rate=Uniform(min_value=0.05, max_value=0.1),
)

sweep_job = command_job_for_sweep.sweep(
    sampling_algorithm = "bayesian",
    ...
)
```

Early Termination Types
- BanditPolicy
- MedianStoppingPolicy

Running
- Training script
    - include arg for each hyperparameter you want to vary
    - log target performance metric
- Configure and run a sweep job

### [Auto ML](https://learn.microsoft.com/en-us/azure/machine-learning/concept-automated-ml?view=azureml-api-2)

Automated Machine Learning 
- Prep
- Train
- Tune

```
from azure.ai.ml import automl

# configure the classification job
classification_job = automl.classification(
    compute="aml-cluster",
    experiment_name="auto-ml-class-dev",
    training_data=my_training_data_input,
    target_column_name="Diabetic",
    primary_metric="accuracy",
    n_cross_validations=5,
    enable_model_explainability=True
)
```

Set Limits

```
classification_job.set_limits(
    timeout_minutes=60, 
    trial_timeout_minutes=20, 
    max_trials=5,
    enable_early_termination=True,
)
```

### Explainers

TabularExplainer
```
explainer = TabularExplainer(model, 
                             x_train, 
                             features=breast_cancer_data.feature_names, 
                             classes=classes)
```

MimicExplainer
```
explainer = MimicExplainer(model, 
                           x_train, 
                           LGBMExplainableModel, 
                           augment_data=True, 
                           max_num_of_augmentations=10, 
                           features=breast_cancer_data.feature_names, 
                           classes=classes)
```

PFIExplainer

```
explainer = PFIExplainer(model,
                         features=breast_cancer_data.feature_names, 
                         classes=classes)
```

Explain the entire model using gloabl explanations

Explain an individual prediction using local explanations