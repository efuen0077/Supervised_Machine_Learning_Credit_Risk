# Supervised Machine Learning: Credit Risk

## Challenge

### Summary and Analysis
✓ Describes the precision and
recall scores.
✓ Describes the balanced
accuracy score.

#### Oversampling vs Undersampling vs Combination
In order to oversample our data, we used the following two methods: ***Naive Random*** Oversampling and ***Synthetic Minority Oversampling Technique (SMOTE)***. The Naive Random Oversampling method gave us the following information: balanced accuracy score = 0.66 (or 66%), a confusion matrix (indicating that we have: 66 False Negatives, 6208 True Negatives, 35 False positives, and 10896 True Positives). Our classification report ***-----*** The SMOTE Oversampling method gave us an accuracy score of 0.66 (or 66%) -- which is equaivalent to that of the Naive Random Oversampling method-- and a confusion matrix that indicated we had 67 False Negatives, 5978 True Negatives, 34 False Positives, and 11126 True Positives. ***---***

Now, we used the ***Cluster Centroids*** resampler in an effort to ***---*** our data. When using this technique, we obtained an accuracy score of 0.66 (or 66%) and a confusion matrix that generated the following data: 68 True Negatives, 9654 False Negatives, 33 False Positives, and 7450 True Positives. ***---***

We, then, resampled the data via ***combination*** by using the ***SMOTEEENN*** algorithm. The results are as follows: the balanced accuracy score calculated was 0.55 (or 55%) and the confusion matrix generated 74 True Negatives, 7454 False Negatives,  27 False positives, 9650 True Positives. ***---***

#### Ensemble
When creating our features and target for our data, we wanted our X value to NOT include the "loan_status" column, but it was also evident that "loan status" was our target, which is why it is our y-value. It was necessary to make sure that ALL columns in our "X" dataset were numerical (i.e. no strings), therefore, we used X = pd.get_dummies(X).

The ***BalancedRandomForestClassifier*** method generated an accuracy score of .99 (99%) and a confusion matrix that displayed the following: 35 True Negatives, False Negatives, 66 False Positives, 17097 True Positives. ***---*** The ***EasyEnsembleClassifier*** generated an accuracy score of .93 (or 93%) and a confusion matrix that shows: 93 True Negatives, 983 False Negatives, 8 False Positives, 16121 True Positives. ***---***

### Recommendations
✓ Includes a final
recommendation on the model to
use, if any.
✓ Provides justification for your
recommendation.
