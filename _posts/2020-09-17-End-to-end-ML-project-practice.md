---
title: "End to End ML Project tutorial from Chapter 2 of the Hands-on Machine Learning book"
description: My first attempt to follow an example of an end to end ML project (regression).
date: "2020-09-17"
---

This project is based on Chapter 2 of [a book by Aurelien Geron](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/)  
The author also provided [a github link for the notebook](https://github.com/ageron/handson-ml2)

I was following the notebook, recreating it, and made some annotations for my own understanding. But 95% of the work was following Geron's. My follow along notebook is [here](https://github.com/Riyan-Aditya/MyBlog/tree/master/Other%20notebooks/Follow%20along%20Hands-on%20ML%20book%20by%20A%20Geron).

**Introduction**

The dataset we are using is the California Housing Prices dataset based on 1990 California census (see Figure below). We were trying to **predict the mean house prices** in each district by using **regression**.

![](https://griyanaditya.files.wordpress.com/2020/09/california_housing_prices_plot.png?w=1024)

In summary, it is an end to end ML project:

- Importing data from Github
- Exploratory Data Analysis
- Preparing data  
    Includes: imputing, dealing with categorical data, custom transformer, and applying pipelines
- Select and train model  
    The example used: linear regression, decision tree, random forest and support vector regression
- Fine tune model / hyperparameter adjustment  
    Via: GridSearch and Randomised search

**Results:**

![](https://griyanaditya.files.wordpress.com/2020/09/newplot-1.png?w=700)

As seen above, the lowest RMSE is for RandomForest with GridSearch tuning. With this model, the RMSE of the test set is $47.7k

**What I learnt**

What do i say. I learnt a lot as this is my first time going through the whole process.

Insights:

- Random test-train split may not be good if the data is skewed. Test data should have a similar "sub-group" distribution as the full data set => use _StratifiedShuffleSplit_
- Experiment with attributes. _Feature engineering_ may create a better metrics  
    Eg: In this example, number\_of\_bedrooms and number\_of\_household didn’t correlate well with median\_house\_value. Once we create number\_of\_rooms/household => this metric much more correlated to median\_house\_value
- Using _SimpleImputer_
- Using _OrdinalEncoder_ vs _OneHotEncoder_
- Feature engineering via custom transformer
- Using Feature Scaling such as _StandardScaler_
- Sparse vs dense matrix. _Sparse matrix in OneHotEncoder_ due to the presence of many 0's.
- Applied the above via _pipeline_
- Using K-fold cross validation (_cross\_val\_score_). Beware of training time.
- Can do automatic hyperparameter via _GridSearchCV_ and _RandomisedSearchCV_
- Sometimes, knowing the final RMSE isn't enough. How do we know if this performs better compared to an already deployed model ==> might be good to find the 95% CI

What I found confusing in this tutorial:

- I found it confusing for the author to rename housing to strat\_train\_set. I would prefer to keep the "train set" variable label throughout the exercise.

**Next step?**

- Probably continue for classification problem tutorial
