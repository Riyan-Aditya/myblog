---
title: "ML roadmap (By Daniel Bourke)"
description: Summary of ML roadmap from Daniel Bourke's Youtube video.
date: "2020-09-16"
---

I like this roadmap from [Daniel Bourke's Youtube video](https://www.youtube.com/watch?v=pHiMN_gy9mk).  
The roadmap can be accessed [here](https://whimsical.com/CA7f3ykvXpnJ9Az32vYXva).

![](https://griyanaditya.files.wordpress.com/2020/09/image.png?w=1024)

  
I think this roadmap provides a good overview of how to learn ML. One-stop-shop for everything. The roadmap covers the basic explanation of ML, the available tools and resources and link to the maths behind them if required.

I also like how the video encourages you to approach the learning as a "cook" rather than a "chemist". Start small. Step-by-step. Learn by doing rather than understanding everything in detail.

**Quick overview**

Basically, **machine learning gives the ability for a machine to learn without being explicitly programmed.**

1. _Problems with long lists of rules_  
    Eg: it will be complex to program a self-driving car via traditional programming  
    
2. _Continually changing environment_  
    Eg: self-driving car can adapt if there is a new road or traffic sign  
    
3. _Discovering insights within large collections of data_  
    Eg: it will be too much to go to every single transaction manually if you are Amazon

**ML problems**

Types of learning for ML:

1. _Supervised learning_  
    You have data and labels. The model tries to learn the relationship between data and label.  
    
2. _Unsupervised learning_  
    You have data but no labels. The model tries to find patterns in data without something to reference on.  
    
3. _Transfer learning_  
    Take an existing ML model, then adjust it on your own and use it for your own problem.  
    
4. _Reinforcement learning_  
    When an agent perform an action and being rewarded or penalised based on if the action is favourable or not

ML problem domains:

1. _Classification_  
    The model will use training dataset to learn and then use them to best map the input to the output/label.  
    Eg: classify a mail as spam or not spam  
    
2. _Regression_  
    The model will identify the relationship between the dependent and independent variables.  
    Eg: the price of a stock over time  
    
3. _Sequence-to-sequence_  
    Usually in languages for translation.  
    Eg: Given a sequence in English, translate it to Spanish.  
    
4. _Clustering_  
    Typically an unsupervised problem. Where the model groups data points based on similarity.  
    Eg: Sort a soccer player based on their attributes (striker/defender/goalkeeper etc)  
    
5. Dimensionality reduction  
    If you have so much input (100 variables), find the 10 most important variables.  
    Eg: by using PCA (principal component analysis)

**ML process**

First, you need to **collect some data.** It is important here to recognise the type of data you need. Data can be structured data in a table (eg: categorical, numerical, ordinal data etc) or unstructured data (eg: images, speech etc). Remember, rubbish in, rubbish out.

Second, you need to **prepare the data**. Typical data preparation steps:

- _Exploratory data analysis (EDA)_  
    This process involves understanding your data. Including exploring whether there are outliers and missing data.  
    
- _Data pre-processing_  
    This step is to prepare your data before the modelling process.
    - Do you fill missing values?
    - Do we need to do feature encoding (changing categorical data into numbers)?
    - Do we need to do feature normalisation?
    - Do we need to do feature engineering?
    - Do we need to deal with data imbalances?  
        
- _Data splitting_  
    For training (70-80% data), validation (10-15% data) and test set (10-15% data) as needed. It is important to not use the test set to tune the model.

The third step is to **train the model**.

- This is done by choosing an algorithm based on your problem and data.
- Beware of _underfitting_ (when the model doesn't perform as well as you would like based on performance metrics) and _overfitting_ (when the model performs far better on the training set than on the test set) the model.
- Typically we overfit first, then reduce through various _regularisation technique_.
- Finally, we can tune various hyperparameters by using validation set data.  
    Eg of hyperparameters: learning rate (usually most important), number of layers, batch size, number of trees etc

Next, we **evaluate the model** based on available metrics. There are several considerations here:

- How long does a model take to train?
- How long does a model need to predict?  
    Eg: It is no good to have a self-driving car model that is 99% accurate but takes 15 seconds to make a prediction
- Consider scenario such as what happens if the input data changes
- Find out the least confident examples. What does the model usually get wrong?
- Consider bias & variance trade-off

Once we are confident, we can **serve the model**. We will not know how it performs until we put it out for real. Use different tools whether the final goal is an a mobile app or a web based application.

Finally, we need to continue evaluating the model and **retrain the model** if needed. The model may change if the data source has changed (such as new road) or data source has been upgraded (such as new hardware used).

**What have I learnt from this roadmap?**

Good news. I know the basic. I have used Python before and familiar with the libraries. I guess I am closer to intermediate in ML. I have watched or read or have done tutorial covering some of these ML algorithms.

I guess I will start here:  

![](https://griyanaditya.files.wordpress.com/2020/09/image-1.png?w=1024)

  
To do lists (probably in this order):

- Do the 3 example projects
- Learn/try how to use [streamlit](https://www.streamlit.io/) to deploy a basic proof of concept
- Go through the [fast.ai](https://www.fast.ai/) curriculum (seems to be highly recommended by DB, the author)
- Test my knowledge in [workera.ai](https://workera.ai/)
- Projects, projects and projects. Probably using [Kaggle](https://www.kaggle.com/)
- SQL maybe?
