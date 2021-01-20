# Project 2 - Ames Housing Data and Kaggle Challenge


# Problem Statement

Given a dataset of houses and their features, we must find the best model 
to predict the sale price of these houses and understand which features of the
houses influence the sale price the most. 
The goal is helping property owners in order to maximize their house values.


# Data dictionary 

I used the infromation provided on the kaggle challenge which is extensive.
I was able to understand the features and compute the null values using this
dictionary.

https://www.kaggle.com/c/dsir-202021214-e-project-2-regression-challenge/data


# Cleaning and EDA

The most tedious process here was the cleaning of the data as there were many
null values and odd values as well. The number of columns and rows also made
the process difficult. 

When I got done with cleaning I was able to start the 
exploratory analysis. I chose to start with only the numerical values at first.
I did some visualization of the features with the highest correlation with 
sale price. 

I decided to pick 4 categorical features based on their correlation with the
sale price. To do that I excluded all the numerical features except the sale
price and looked at the correlation. I picked the 4 most correlated features
and created dummy variables.


# Modeling 

I used 4 models for this project. The first one was my initial regression model
where I only used the numerical features of the dataset. It didn't perform so 
bad with a R2 score of .83 and I used it for my kaggle submission.

The second one was an imporoved regression model where I included the encoded 4 categorical 
values I selected during the EDA/selection feature. I also scaled the data and this model 
was an imporvement with a R2 score of .89. This was my best model

The third model I used was Lasso where I did some cross-validation. I kept the same features,
numerical and categorical. Unfortunately. it didn't perform better than the second model.
The R2 score of this model is .87

The last one is a ridge model with cross-validation. This model perform better than 
lasso with a R2 score of .88. It was really close to the second model


# Conclusion 

Based on my analysis and the data provided, it is possible to approximate the sale price of a house given it's features. The best model I came up with is a linear regression model explaining 88.7 of the variance in precicted values.

Some features are more influential than others like the overall quality of a house the square footage of the living area, the square footage of the basement and the garage. The foundation is also a factor as well as the neighborhood and the exterior material quality.

While those features increase the house price, they can also negatively affect it if they are out of the norm. Really big square footage don't result in higher prices. The same thing can apply to additional features where they don't add a lot to the value of a house.

My recommandation to property owners looking to maximize the value of their house apart from what they can't control is to remodel the houses if possible. The best factor on sale price is the overall quality of the house so renovations are the key.



Link to presentation:
https://drive.google.com/file/d/1e4g_3CGyG2VtHQOP1ydSB3wLYEK2kYki/view?usp=sharing
