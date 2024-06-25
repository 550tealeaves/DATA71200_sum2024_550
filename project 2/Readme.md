# Loading and explaining target variable 
After loading and splitting the data, I used a one hot encoder to separate the categorical variables based on their values. 
Because the target variable (company) is categorical, I created a bar chart instead of histogram to show the frequencies. Companies C & E appear to be tied with the highest frequency, while D has the least. It looks like the range in frequencies goes from 22 (highest) to 15 (lowest)

# k Nearest Neighbor
For the first model, I used the k Nearest Neighbor. The default model produces a test set score of 0.33, meaning that the model accurately predicted the correct pizza company for 33% of the test set. This then is extrapolated to mean the model would be correct 33% of the time for new data. The cross validation results indicate that 8 & 9 are the best performing k's and 23 the worst performing (0.30). While the knn_gscv.best_params_ said that 8 was the best, when I manually adjusted the parameter, k=9 outperformed k=8, 0.45 vs 0.48, respectively. I then adjusted to k=4, which according to the rank is 9th best and got a score of 0.42.
I adjusted to k=1 for the worst performing, which is originally ranked as 20th, and got a score of 0.33, the same as the default test accuracy. 


# Random Forest
The second model utilized the Random Forest. The default model says that it can accurately predict the correct pizza company for 81% of the training data and 45% of the test set. I was not completely certain how to interpret the cross validation results. The CV scores mean is 0.46 and the other value is 0.53. When plotting the important features, extra mushrooms and diameter in inches are the most important features for decision making. 

When I tripled the estimators to 15, the training set accuracy increased slightly, to 84%, while there was no change to the test set accuracy. Plotting these important features shows that extra mushrooms and size regular were the most important features to this decision making. 

In the third version, I increased the estimators to 20, it, there was no change to training set accuracy, but test set accuracy decreased to 39%. For feature importance, extra mushrooms, price in Canadian dollars, and regular size were the most important features to decision making. Precision, recall, and F1 generally decreased as the number of estimators increased. 


## What went well and what requires improvement
*It Worked*
- After much frustration, the code ran for most of the notebook
- k nearest neighbor was the easiest to understand

*Work in progress*
- Interpretation of the cross validation for the Random Forest - not sure if I coded it properly
- Not sure if I got the best and worst parameters for Random Forest, probably could have used an alternative method, like Support Vector Machines
- Was unsure if the logistic regression was necessary to keep for k nearest neighbor - I kept it but it may not have mattered. 
- Feature scaling - received an invalid syntax. Gemini converted it into a something that only accepted numbers and promised their world. 
