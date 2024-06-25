# Loading and explaining target variable 
After loading and splitting the data, I used a one hot encoder to separate the categorical variables based on their values. 
Because the target variable (company) is categorical, I created a bar chart instead of histogram to show the frequencies. Companies C & E appear to be tied with the highest frequency, while D has the least. It looks like the range in frequencies goes from 22 (highest) to 15 (lowest)

# k Nearest Neighbor
For the first model, I used the k Nearest Neighbor. The default model produces a test set score of 0.33, meaning that the model accurately predicted the correct pizza company for 33% of the test set. This then is extrapolated to mean the model would be correct 33% of the time for new data. The cross validation results indicate that 8 & 9 are the best performing k's and 23 the worst performing (0.30). While the knn_gscv.best_params_ said that 8 was the best, when I manually adjusted the parameter, k=9 outperformed k=8, 0.45 vs 0.48, respectively. I then adjusted to k=4, which according to the rank is 9th best and got a score of 0.42.
I adjusted to k=1 for the worst performing, which is originally ranked as 20th, and got a score of 0.33, the same as the default test accuracy. 

