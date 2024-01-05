## Train Pipelines

https://github.com/MicrosoftLearning/mslearn-dp100/blob/main/08%20-%20Create%20a%20Pipeline.ipynb

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

### [HPO](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-tune-hyperparameters?view=azureml-api-1)

Sampling Types
- GridParameterSampling 
- RandomParameterSampling
- BayesianParameterSampling

Early Termination Types
- BanditPolicy
- MedianStoppingPolicy

Running
- Training script
    - include arg for each hyperparameter you want to vary
    - log target performance metric
- HyperDriveConfig

### [Auto ML](https://learn.microsoft.com/en-us/azure/machine-learning/concept-automated-ml?view=azureml-api-1)

Automated Machine Learning 
- Prep
- Train
- Tune

```
from azureml.train.automl import AutoMLConfig

automl_run_config = RunConfiguration(framework='python')
automl_config = AutoMLConfig(name='Automated ML Experiment',
                             task='classification',
                             primary_metric = 'AUC_weighted',
                             compute_target=aml_compute,
                             training_data = train_dataset,
                             validation_data = test_dataset,
                             label_column_name='Label',
                             featurization='auto',
                             iterations=12,
                             max_concurrent_iterations=4)
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