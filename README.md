# Credit Risk Analysis
## Overview
This project is to test different techniques to evaluate models with unbalanced classes to predict credit risks.  Particularly, we want to predict High Credit Risks and focus on the "High Risk Recall" number which tells us how well our model performs predicting high credit risks where the prediction of high risk individuals is measured against the actual high risk individuals. We are not really concerned how well Low Credit Risks are predicted since that prediction does not predict High Credit Risks and will not impact the credit card company.

## Results 
### Random Oversampling
- Balanced Accuracy: 0.65
- High Risk Precision: 0.01
- High Risk Recall: 0.71

![This is an image](/images/RandomOversampling.png)

### SMOTE Oversampling
- Balanced Accuracy: 0.66
- High Risk Precision: 0.01
- High Risk Recall: 0.63

![This is an image](/images/SmoteOversampling.png)

### Cluster Centroids Undersampling
- Balanced Accuracy: 0.54
- High Risk Precision: 0.01
- High Risk Recall: 0.69

![This is an image](/images/ClusterCentroidsUndersampling.png)

### SMOTEENN Combination (Over and Under) Sampling
- Balanced Accuracy: 0.67
- High Risk Precision: 0.01
- High Risk Recall: 0.73

![This is an image](/images/SMOTEENNCombinationSampling.png)

### Balanced Random Forest Classifier
- Balanced Accuracy: 0.77
- High Risk Precision: 0.03
- High Risk Recall: 0.65

![This is an image](/images/BalancedRandomForestClassifier.png)

### Easy Ensemble Classifier
- Balanced Accuracy: 0.93
- High Risk Precision: 0.09
- High Risk Recall: 0.92

![This is an image](/images/EasyEnsembleClassifier.png)

# Summary
As we can see from the results,the Random Oversampling, SMOTE Oversampling,C luster Centroids Undersampling and Balanced Random Forest Classifier models have a High Risk Recall between .65 and .73 which would not be an effective predictor since the model would not be able to predict 23% of High Risk credit users. On average, they get about 70 correct out of 100 so, they get a D rating.

However, the Easy Ensemble Classifier has a High Risk Recall of .92 which is quite an improvement from the previous high for High Risk Recall of .73. 

While the Easy Ensemble Classifier scores pretty well for our target, I believe that with better data and more features, we should be able to get a recall score closer to .98 or .99.  At this point, I can not reccomend these classifiers but the Easy Ensemble Classifier shows promise and should be considered after more testing and tweaking.

