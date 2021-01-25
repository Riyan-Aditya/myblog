---
title: "Transform data from fingerprint machine"
description: A simple Python code to transform the data from fingerprint machine in Excel to be used for monthly salary calculation. 
date: "2021-01-25"
---


# Background

The HR in my family's restaurant business has been struggling to calculate salaries for the workers each month. One of the pain point is to translate the data from the fingerprint machine into the required format for salary calculation. Note that we are paying hourly wages, hence we use a fingerprint machine to record the time when the workers come in and out, as well as the time when they take a break.  

The data from the fingerprint looks like this. Every employee is identified based on their worker id, name, timestamp and status. Status indicates when they come for work and take break. 

<img src="https://github.com/Riyan-Aditya/MyBlog/blob/master/images/fingerprint_absent/fingerprint_input.PNG">

For salary calculation, the HR requires the data in different format. Where each row represents each day. there should be four fingerprint data per day (start work, start break, end break, end work). I created a python app, to reorganise the format above into like this. 

<img src="https://github.com/Riyan-Aditya/MyBlog/blob/master/images/fingerprint_absent/fingerprint_output.PNG">

This little program has **saved our HR about 1-2 days of admin time per month**, where they used to have to pivot the data manually. Now I can help them solve this in less than 5 minutes 


# Solution

Normally, this can be easily solved with the Pandas' pivot_table function. However, there are several challenges:
* There is nothing that distinquish between when the workers starting their work and when they starting a break
* Workers often rescan their fingerprint when they feel that the machine does not register their input
* Workers sometimes do not register their break (maybe the forgot or they have customers so they do not take a break)
* Datetime format was initially different in different fingerprint machines. 

Hence, this lead to an uneven number of rows to pivot. To solve this I had to use several groupby function. I have also added several options to choose the right datetime format as required. The code can be viewed [here](https://github.com/Riyan-Aditya/fingerprint).

For now, I have created a web app locally in Voila to help simplify the process. Every month I need to run the program to help our HR. An overview of the app can be seen here:

<img src="https://github.com/Riyan-Aditya/MyBlog/blob/master/images/fingerprint_absent/app_demo.PNG">


# To do
Online deployment. I would like to deploy this so the HR can use it without my help. Previously I have tried to deploy this via Binder, but I struggle to get the output to be saved in xlsx format. 
