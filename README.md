# Welcome To Riyan's blog

In this repository, I am uploading code, notebooks and posts from my personal blog: https://riyan-aditya.github.io/MyBlog/.

The blog documents my effort to be a better Data Scientiest and Data Analyst. Also contains one or two code that I made to help people around me to be more efficient.

This summary page showcase projects that I am most proud off. All the projects are organised based on topic on https://riyan-aditya.github.io/MyBlog/categories/.

The blog was made with the help of [fastpages](https://github.com/fastai/fastpages)

# Projects

I have made a series of projects, all of which are available on my blog : https://riyan-aditya.github.io/MyBlog/categories/

This page highlights those projects that I am most proud of. 

## Table of Content :
- [Data visualisation](https://github.com/Riyan-Aditya/MyBlog#data-visualisation)
- [Machine learning](https://github.com/Riyan-Aditya/MyBlog#machine-learning)

## Data visualisation

**Covid19 in Indonesia**

I am using the data from [KawalCovid](https://kawalcovid19.id/) and others to give me a quick overview of the latest worldwide and Indonesian data. The full blog posts [here](https://riyan-aditya.github.io/MyBlog/data%20viz/2020/10/12/CovidID.html) contain interactive data vizualisation that I update weekly. 

Sample visualisation (from December 2020):

<img src="https://github.com/Riyan-Aditya/MyBlog/blob/master/images/covid19_sample_images/daily_cases_per_prov.PNG">

*Daily cases and daily tests in Indonesia*
<img src="https://github.com/Riyan-Aditya/MyBlog/blob/master/images/covid19_sample_images/daily_cases_and_tests.PNG">


## Machine Learning

**FIFA21 EPL player position classification (unsupervised learning)**

I webscrapped the data for all the  players who play in EPL from the FIFA21 game from this [website](https://sofifa.com/players?type=all&lg%5B0%5D=13). This is my first attempt to conduct an unsupervised learning by using data from players' attributes to predict players' position. 

Models used in this learnings are logistic, k-nearest neighbour, random forest and support vector machine. Overall, the best model after tuning is the *SVM* where it has roughly *90% accuracy* and F1 score to predict the position of the players in the test set. Unsurprisingly, midfielders are the position that are hardest to predict (wingers probably have similar attribute to wide forwards and defensive midfielders might have similar skillset to defenders).

The full blog posts [here](https://riyan-aditya.github.io/MyBlog/web%20scrap/data%20viz/ml/2020/11/09/FIFA21-EPL-pos-pred.html#Accuracy-and-F1-score)

Sample visualisation:

*Position vs wage in FIFA21. Note: Kevin de Bruyne is the outlier*
<img src="https://github.com/Riyan-Aditya/MyBlog/blob/master/images/fifa21_pos_classification/fifa21_pos_clas.PNG">

*Covariance matrix for the test result*
<img src="https://github.com/Riyan-Aditya/MyBlog/blob/master/images/fifa21_pos_classification/conf_matrix_test.PNG">







