# Unsupervised Learning
After loading the data and performing a 75/25 split, I scaled the data and then did some pre-processing before running the PCA.

## Pre-processing
- First scaled the data. While most of the data is categorical, the two variables "diameter_in" & "price_cad" required scaling. 
- The decision-tree classifier shows that it is able to accurately predict the correct pizza company 84% of the time on the training set and only 58% on the test set. 

## PCA
We see in the first component it is a bit difficult to tell if the features have zero or negative sign. The teal color looks to range from 0 to -0.1. 
The second component shows more overall negative values, especially for features such as "large", "crunchy", "classic", "tuna", and "sausage". 
When testing the accuracy, we see that the training set accuracy remains as before (84%) but that of the test set shows a precipitous drop to 0.18 (18%). This suggests that this method is algorithm is overfitting to the training data and does not generalize to new data. 

## Support Vector Machines (SVM)
We then ran a test using SVM, which, according to the textbook, learns the importance of each training data point to the decision boundary between 2 classes. We ran 2 models and noted that the accuracies of both sets decreased dramatically (0.40-training, 0.36-test) but then the training data accuracy increased on the 2nd run. (0.54-training, 0.33-test)

## PCA ON UNSCALED VS SCALED DATA
In the unscaled, we see that only the two variables, "price_cad" and "company" have a positive signs in the first component. In the second component, price_cad has a negative value, compared to the positive value of "company". All other features hover around 0. The accuracy for training set is 0.42 and 0.30 in test set.  
In the scaled data, the accuracy dropped to 0.29 for training set and 0.24 for test set.

## 95% Variance
The unscaled data makes it harder to distinguish between positive and negatives for the features. Most of the visualization has a teal color that ranges from 0.1 to -0.1. The scaled data makes this distinction much clearer. While overall, teal is probably the most common in the visualization, it is much easier to see the positive and negatives.

## NVF
NVF can identify the original components of the combined data and its useful when the data is positive. We see in the visualizations that most of the features are very close to 0. In the scaled, "vegetables" & "pepperoni" have the highest positive value. 