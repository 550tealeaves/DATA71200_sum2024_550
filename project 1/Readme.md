# Dataset
This dataset was taken from Kaggle; I searched for supervised learning and this was one of the options on the list. [Here is the link](https://www.kaggle.com/datasets/starlitlolith/canada-pizza-price-prediction)


# Cleaning
It is a relatively clean dataset, with no missing values, but I did make a modification to one column. The column diameter was originally listed as string values - 22 inch, 18 inch etc. I changed the feature name to diameter_in and reformatted the column to just be integers (22, 18 etc). There were also some typos that I corrected.

Delving deeper into the the features, I do notice some potential problems. What is the difference between beef and meat in the toppings feature, also smoked beef vs beef? 

It looks like the variant feature is the most predictive a company name because certain values are specifically linked to certain companies. So I might try the one hot encoding for this feature.

The size feature is also interesting - what is the difference between XL and jumbo or regular and medium? 


# Objective of analysis
I want to predict the Company that makes the pizza based on the features. From the initial glance, I would say that the most important features to include in the model are 
1. topping
2. variant
3. size 
4. price 

Perhaps the diameter is relevant, but the values seem to be equally represented across all companies. I don't think the extra sauce, cheese, or mushrooms will be included because that's something commonly offered at most companies.  

# Results
After many hours of frustration and thankfully some guidance from the professor, I was able to complete the machine learning model. Overall, I think there were some redundancies in the code, but being so new to this subject, I did not want to remove anything for fear of breaking the code. 

It looks like logistic regression had stronger accuracy than k-nearest neighbor. The best performing k was #8 (0.454), and the worst performing was #23 (0.484). Now why does the worst performing k perform better than the best, I have no idea. 
In logistic regression, the best performing has a prediction of 0.51.

