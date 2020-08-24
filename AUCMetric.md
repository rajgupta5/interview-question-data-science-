AUC Metric for Classification

AUC is the area under the ROC curve. It is a popularly used metric to evaluate ML models for classification

***What is AUC?***

AUC is the area under the ROC curve. It is a popularly used classification metric.

Here is a 3 minute video explaining AUC and the ROC curve:
https://youtu.be/R4jdKWt7OP4

Classifiers such as logistic regression and naive Bayes predict class probabilities as the outcome instead of the predicting the labels themselves. A new data point is classified as positive if the predicted probability of positive class is greater a threshold. Each threshold leads to a different classifier. Hence, typical metrics such as accuracy and F1 score depend on the threshold one  picks. AUC for such classifiers gives an aggregated metric across thresholds.


***Why do we care about AUC and the ROC curve?***
AUC is popular because

It is a threshold independant metric – Helps evaluate the model without being  dependent on the specific threshold we choose
The ROC curve is often used to chose the threshold
Some classifiers such as an SVM or a perceptron give the class labels directly as the  outcome and not class probabilities. 


***Does it make sense to compute the AUC  metric for classifiers such as the SVM which give class labels as outcome? ***

The answer is Yes. It is often useful to get class probability outcomes instead of absolute class values. And it turns out most would have computed the AUC at some point or the other for the SVM classifier using scikit-learn - lets see what goes on under the hood though.


***Platt Scaling: How to Compute AUC for an SVM Classifier?***
The following 10 minute video explains computing the AUC metric for an SVM classifier, or other classifiers that give absolute class values as outcomes.

https://youtu.be/jVgN5rD33o0

The video explains the process of calibrating the outcomes of such classifiers to get class probabilities, from which one can compute the AUC.
