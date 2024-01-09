
## Regression

Mean Squared Error (MSE): The mean of the squared differences between predicted and actual values. This yields a relative metric in which the smaller the value, the better the model's fit.
- What it measures: The average squared difference between predicted and actual values.
- Use case: Commonly used for regression problems.

Root Mean Squared Error (RMSE): The square root of the MSE. This yields an absolute metric in the same unit as the label (in this case, numbers of rentals). The smaller the value, the better the model (in a simplistic sense, it represents the average number of rentals by which the predictions are wrong).
- What it measures: The square root of the average squared difference between predicted and actual values.
- Use case: Provides a interpretable metric in the same units as the target variable.

Mean Absolute Error (MAE):
- What it measures: The average absolute difference between predicted and actual values.
- Use case: Provides a robust measure of error in regression problems.

R2 Score (Coefficient of Determination): A relative metric in which the higher the value, the better the model's fit. In essence, this metric represents how much of the variance between predicted and actual label values the model is able to explain.
- What it measures: The proportion of the variance in the dependent variable that is predictable from the independent variables.
- Use case: Evaluates the goodness of fit in regression problems.

## Classification

Accuracy:
- What it measures: The proportion of correctly classified instances out of the total instances.
- Use case: Suitable for balanced datasets.

Precision:
- What it measures: The proportion of true positive predictions out of the total positive predictions.
- Use case: Useful when minimizing false positives is critical.

Recall (Sensitivity, True Positive Rate):
- What it measures: The proportion of true positive predictions out of the total actual positives.
- Use case: Important when identifying all positive instances is crucial.

F1 Score:
- What it measures: The harmonic mean of precision and recall.
- Use case: Balances precision and recall, especially when there is an imbalance in the classes.

Area Under the Receiver Operating Characteristic Curve (AUC-ROC):
- What it measures: The area under the ROC curve, which visualizes the trade-off between true positive rate and false positive rate.
- Use case: Evaluates the model's ability to discriminate between classes.

Log Loss (Logarithmic Loss):
- What it measures: The logarithm of the likelihood that the predicted probabilities match the true labels.
- Use case: Commonly used for binary and multiclass classification problems.

Confusion Matrix:
- What it measures: A table showing the counts of true positive, true negative, false positive, and false negative predictions.
- Use case: Provides a detailed understanding of the model's performance.
- The model predicted 0 and the actual label is 0 (true negatives, top left)
- The model predicted 1 and the actual label is 1 (true positives, bottom right)
- The model predicted 0 and the actual label is 1 (false negatives, bottom left)
- The model predicted 1 and the actual label is 0 (false positives, top right)

## Clustering