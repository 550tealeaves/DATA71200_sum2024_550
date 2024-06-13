# Dataset
This dataset was taken from Kaggle; I searched for supervised learning and this was one of the options on the list. [Here is the link](https://www.kaggle.com/datasets/starlitlolith/canada-pizza-price-prediction)


# Cleaning
It is a relatively clean dataset, with no missing values, but I did make a modification to one column. The column diameter was originally listed as string values - 22 inch, 18 inch etc. I changed the feature name to diameter_in and reformatted the column to just be integers (22, 18 etc).

# Objective of analysis
I want to predict the Company that makes the pizza based on the features. From the initial glance, I would say that the topping, variant, size, and price are probably the most important features to include in the model. Perhaps the diameter is relevant, but the values seem to be equally represented across all companies. I don't think the extra sauce, cheese, or mushrooms will be included because that's something commonly offered at most companies.  