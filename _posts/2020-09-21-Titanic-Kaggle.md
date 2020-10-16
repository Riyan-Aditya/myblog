---
title: "Classification tutorial following titanic dataset"
description: My attempt to follow a classification ML problem tutorial based on the famous Titanic dataset from Kaggle.
date: "2020-09-21"
---

This project is based on a [YouTube video](https://www.youtube.com/watch?v=I3FBJdiExcg&t=1797s) by KenJee  
The author also provided [a link to Kaggle for his notebook](https://github.com/ageron/handson-ml2)  
This is also based on the popular [Kaggle's Titanic dataset](https://www.kaggle.com/c/titanic) which is used as the introduction for classification problem.

I was following the notebook, recreating it, and made some annotations for my own understanding. My follow along notebook is [here](https://github.com/Riyan-Aditya/MyBlog/tree/master/Other%20notebooks).

Ken provided a good overview in each notebook session as well as introductory comment for each cell. Often I read the comment then attempted to code by myself first, then checking with his code afterwards. Good progress for my learning.

**Introduction**

This [Titanic](https://en.wikipedia.org/wiki/MNIST_database) dataset is commonly used as the introduction into the Kaggle competition. With this dataset, we create a model to predict which passengers survived the Titanic shipwreck.

Coding process:

- Import data
- EDA
- Feature Engineering
- Data Preprocessing
    - Dropped null values, used dummy variables, imputed data with median and using standard scaler
- Model building
    - Using: _Naive Bayers, Logistic Regression, Decision Tree, K Nearest Neighbour, Random Forest, Support Vector Classifier, Extreme Gradient Boosting, Soft Voting Classifier_
- Model tuning

Result:

From the base model, the cross validation score achieved was around 75 to 80%. The best model seems to be the _Support Vector Classifier_ model. The ensemble method seems to perform better.

The models were later tuned by using _GridSearch_. Hyperparameter for model such as RandomForest may take ages to run. Overall, the model performance slightly improved (1 to 3%) after tuning. The _Extreme Gradient Boosting_ model received the highest improvement. Some voting classifier were also conducted using combinations of the tuned models.

At the end, **the best performance model** with the Kaggle's test dataset is the **hard voting** of the tuned model. This achieved **79%** score with the test set.

![](https://griyanaditya.files.wordpress.com/2020/09/newplot-2.png?w=700)

**What I learnt**

Insights:

- Good idea to do EDA separately between numerical and categorical data.
- For categorical data such as cabin or ticket, don't be afraid to group variables based on certain category (eg: first letter of ticket). This can shorten combinations significantly.
- Using Pandas' _get\_dummies_ vs _OneHotEncoding_.
    - Generally for ML, _OHE_ seems to be better and can be used in pipelines
    - _get\_dummies_ can be applied to a dataframe automatically (it will automatically applied only for the categorical part of the DF).
- For model like _RandomForest_, maybe better to start with _RandomisedSearchCV_ then tune with _GridSearchCV_ to cut down searching costs.

**Next step?**

I am going to continue with Chapter 4 of the Geron's book
