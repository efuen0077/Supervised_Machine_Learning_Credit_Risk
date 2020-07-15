# Supervised Machine Learning: Credit Risk

## Challenge

### Summary and Analysis
✓ Describes the precision and
recall scores.
✓ Describes the balanced
accuracy score.

#### Oversampling vs Undersampling vs Combination

***Naive Random Oversampler:*** balanced accuracy score = 0.66 (or 66%) | 66 False Negatives | 6208 True Negatives |
35 False positives | 10896 True Positives.

***Synthetic Minority Oversampling Technique (SMOTE):*** balanced accuracy score = 0.66 (or 66%) | 67 False Negatives
5978 True Negatives | 34 False Positives | 11126 True Positives.

***Cluster Centroids:*** balanced accuracy score = 0.66 (or 66%) | 68 True Negatives | 9654 False Negatives | 
33 False Positives | 7450 True Positives.

***SMOTEEENN:*** balanced accuracy score = 0.55 (or 55%) | 74 True Negatives | 7454 False Negatives |
27 False positives | 9650 True Positives.



#### Ensemble
When creating our features and target for our data, we wanted our X value to NOT include the "loan_status" column, but it was also evident that "loan status" was our target, which is why it is our y-value. It was necessary to make sure that ALL columns in our "X" dataset were numerical (i.e. no strings), therefore, we used X = pd.get_dummies(X).

***BalancedRandomForestClassifier*** accuracy score = .99 (99%) | 35 True Negatives | 7 False Negatives |
66 False Positives | 17097 True Positives.

***EasyEnsembleClassifier*** accuracy score = .93 (or 93%) | 93 True Negatives | 983 False Negatives |
8 False Positives | 16121 True Positives.

### Recommendations
✓ Includes a final
recommendation on the model to
use, if any.
✓ Provides justification for your
recommendation.
