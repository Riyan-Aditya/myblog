---
title: "Classification tutorial from Chapter 3 of the Hands-on Machine Learning book"
description: My first attempt to follow a classification example.
date: "2020-09-18"
---

This project is based on Chapter 3 of [a book by Aurelien Geron](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/)  
The author also provided [a github link for the notebook](https://github.com/ageron/handson-ml2)

I was following the notebook, recreating it, and made some annotations for my own understanding. My follow along notebook is [here](https://github.com/Riyan-Aditya/MyBlog/tree/master/Other%20notebooks/Follow%20along%20Hands-on%20ML%20book%20by%20A%20Geron).

Minor progress. In managed to become independent while following through the example notebook compared to when I was going through Project 1 (I tried to type some of the codes from scratch).

**Introduction**

The dataset is the [MNIST](https://en.wikipedia.org/wiki/MNIST_database) data that are commonly used as the "hello world" for image classification. Basically, given the input, we are trying to train a model and compare it to the feature label (which is the digit of the image).

![](https://griyanaditya.files.wordpress.com/2020/09/image-2.png?w=633)

Coding process:

- Load data
- Start from binary classifier.
- Multiclass classifier.
- Briefly cover multi label and multi output classification

Problem: Some of the model takes forever to train (maybe my limited hardware). I ended up using sub datasets (up to 5k data) from the training datasets (60k). Hence, my output wasn't optimal compared to the example notebook.

Result: Independent of the example, **I attempted to make the final prediction by using the SGD model (trained with 10k data) and applied to the test set (the last 1k data imported)**.

The following is the confusion matrix plot of the test set. Bright colour indicates missclassifed. We can observe that the model confuse:

- 3 and 5 (bright white box).
- 7 and 9
- Furthermore, many numbers are miss classified as an 8 (colum with an 8).

![](https://griyanaditya.files.wordpress.com/2020/09/image-5.png?w=345)

**What I learnt**

Insights:

- For classification problem, it is important to shuffle the dataset. Some algorithm may perform poorly if they get many instances in a row
    - But this is not good for data such as time series data
- Binary classification using _SGDClassifier_ & RandomForest => build a number 5 classifier
    
    - Performance metrics: accuracy, confusion matrix, precision, recall, F1, Precision Recall curve, ROC curve.
    
    - Consider _precision/recall tradeoff_. They go together. High precision is not useful for low recall
    - Use _PR curve_ instead of _ROC curve_ when positive class is rare or care more about FP than FN
- Multiclass classification => used _SVC_ and _SGD_
    - Assess with _confusion matrix_
    - Using _matshow()_ can help to visualise and give insight on which classes that are easily miss-classified

**Next step?**

I am buying this book and will continue on Chapter 4 next week. Really liked the explanation as well as the accompanying notebook in Github.

One of the added exercise is to go through the Titanic dataset on Kaggle. I watched a YouTube video on it before, tried to follow through but unfinished. I will re-attempt this again
