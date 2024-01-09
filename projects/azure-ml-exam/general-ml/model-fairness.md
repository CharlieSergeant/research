## Ethical and Fair ML

https://learn.microsoft.com/en-us/azure/machine-learning/concept-responsible-ai?view=azureml-api-1

[FairLearn](https://github.com/fairlearn/fairlearn) Library


### Interpretability

Global explanations: Model wide feature importance. How does the model generalize to new data?

Local explanations: Single record feature importance. How important each feature was for the prediction for this record.  

Model explanations: Model feature importances for a certain cohort of data points. Based on a condition or filter show the feature importance. 

### Fairness

Harm of allocation: extend or withold opportunity for certain groups

Harm of quality of service: doesn't work as well for one group as it does for another


Add in disparity metrics:
- how does the model perform for different subgroups? 
    - Men/Women
    - Race

#### Parity constraints:
Demographic party: Mitigate allocation harms (Binary classification, regression)
- What it compares: Predictions between different groups (true values are ignored)
- Reason to use: If the input data are known to contain biases, demographic parity may be appropriate to measure fairness
- Caveats: By only using the predicted values, information is thrown away. The selection rate is also a very coarse measure of the distribution between groups, making it tricky to use as an optimization constraint

Equalized odds: Diagnose allocation and quality of service harms (Binary classification)
- What it compares: True and False Positive rates between different groups
- Reason to use: If historical data does not contain measurement bias or historical bias that we need to take into account, and true and false positives are considered to be (roughly) of the same importance, equalized odds may be useful
- Caveats: If there are historical biases in the data, then the original labels may hold little value. A large imbalance between the positive and negative classes will also accentuate any statistical issues related to sensitive groups with low membership


Equal oppertunity: Diagnose allocation and quality of service harms (Binary classification)
- What it compares: True Positive rates between different groups
- Reason to use: If historical data are useful, and extra false positives are much less likely to cause harm than missed true positives, equal opportunity may be useful
- Caveats: If there are historical biases in the data, then the original labels may hold little value. A large imbalance between the positive and negative classes will also accentuate any statistical issues related to sensitive groups with low membership


Bounded group loss: Mitigate quality of service harms (Regression)

Mitigation algorithms:
- Reduction
- Post-processing

### Causual analysis

Use causal inference when you need to:

- Identify the features that have the most direct effect on your outcome of interest.
- Decide what overall treatment policy to take to maximize real-world impact on an outcome of interest.
- Understand how individuals with certain feature values would respond to a particular treatment policy.