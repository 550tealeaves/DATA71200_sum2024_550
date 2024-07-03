# Unsupervised Learning
After loading the data and performing a 75/25 split, I scaled the data and then did some pre-processing before running the PCA.

## Pre-processing
- First scaled the data. While most of the data is categorical, the two variables "diameter_in" & "price_cad" required scaling. 
- The decision-tree classifier shows that it is able to accurately predict the correct pizza company 84% of the time on the training set and only 58% on the test set. 

## PCA
We see in the first component it is a bit difficult to tell if the features have zero or negative sign. The teal color looks to range from 0 to -0.1. 
The second component shows more overall negative values, especially for features such as "large", "crunchy", "classic", "tuna", and "sausage". 