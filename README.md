# Supervised Machine Learning: Credit Risk

## Challenge

### Summary and Analysis

#### Resampling

- Naive Random Oversampler: balanced accuracy score = 0.66 (or 66%) | 66 True Negatives | 6208 False Negatives |
35 False Positives | 10896 True Positives.

There is an immense amount of false negatives (6208), which is NOT IDEAL for the model we are trying to work with. The imbalanced classification report shows this with a 0.01 precision. A recall of 0.65 is also not ideal. 

- Synthetic Minority Oversampling Technique (SMOTE): balanced accuracy score = 0.66 (or 66%) | 67 True Negatives
5978 False Negatives | 34 False Positives | 11126 True Positives.

There is, still, a large amount of false negatives. This, again, is not ideal for our model. The imbalanced classification report shows this with a 0.01 precision and 0.66 recall.

- Cluster Centroids: balanced accuracy score = 0.66 (or 66%) | 68 True Negatives | 9654 False Negatives | 
33 False Positives | 7450 True Positives.

There is a significantly higher amount of false negatives than false positives, indicating that this is not ideal for our model. The imbalanced classification report shows this with a 0.01 precision and 0.67 recall.

- SMOTEEENN: balanced accuracy score = 0.55 (or 55%) | 74 True Negatives | 7454 False Negatives |
27 False positives | 9650 True Positives.

The amount of false positives and false negatives are very similar. This is definitely not ideal for our model. The imbalanced classification report shows this with a 0.01 precision and 0.73 recall (this is second best out of the 6 models that we have).

#### Ensemble
When creating our features and target for our data, we wanted our X value to NOT include the "loan_status" column, but it was also evident that "loan status" was our target, which is why it is our y-value. It was necessary to make sure that ALL columns in our "X" dataset were numerical (i.e. no strings), therefore, we used X = pd.get_dummies(X).

- BalancedRandomForestClassifier: accuracy score = .99 (99%) | 35 True Negatives | 7 False Negatives |
66 False Positives | 17097 True Positives.



- EasyEnsembleClassifier: accuracy score = .93 (or 93%) | 93 True Negatives | 983 False Negatives |
8 False Positives | 16121 True Positives.



### Recommendations
The model that would be the best to use when trying identify good vs risky loans is the Balanced Random Forest CLassifier. This model had the highest accuracy score (99%), precision of 0.83 for high risk, 0.35 recall, the highest amount of True Positives and least amount of false negatives. I will say, however, that the Easy Ensemble Classifier is a close second with an accuracy score of 93%, precision of 0.09 and recall of 0.92 (for high risk classification).
