# Supervised Machine Learning: Credit Risk

## Challenge

### Summary and Analysis
✓ Describes the precision and
recall scores.
✓ Describes the balanced
accuracy score.

#### Oversampling vs Undersampling vs Combination
In order to oversample our data, we used the following two methods: ***Naive Random*** Oversampling and ***Synthetic Minority Oversampling Technique (SMOTE)***. The Naive Random Oversampling method gave us the following information: balanced accuracy score = 0.66 (or 66%), a confusion matrix (indicating that we have: 66 False Negatives, 6208 True Negatives, 35 False positives, and 10896 True Positives). Our classification report ***ADD STUFF HERE*** The SMOTE Oversampling method gave us an accuracy score of 0.66 (or 66%) -- which is equaivalent to that of the Naive Random Oversampling method-- and a confusion matrix that indicated we had 67 False Negatives, 5978 True Negatives, 34 False Positives, and 11126 True Positives. ***ADD STUFF HERE***

Now, we used the ***Cluster Centroids*** resampler in an effort to ***undersample*** our data. When using this technique, we obtained an accuracy score of 0.66 (or 66%) and a confusion matrix that generated the following data: 68 True Negatives, 9654 False Negatives, 33 False Positives, and 7450 True Positives.

#### Ensemble


### Reccommendations
✓ Includes a final
recommendation on the model to
use, if any.
✓ Provides justification for your
recommendation.
