![alt text](https://github.com/cosfer2804/FCDATA/blob/main/screenshot/logo.png) 

# FINAL PROJECT - SPOTIFY PODCASTS EPISODES ENGINE RECOMMENDER

By: <br/>
[Angela Wang](https://www.linkedin.com/in/angela-wang-716632b1/)

## Table of Contents
- [Scenario](#scenario)
- [Objective](#objective)
- [Tools and Methods](#tools-and-methods)
- [Models](#models)
- [Insight](#insights)
- [Next Steps](#next-steps)

## Scenario
The rise of podcasts in the past years and their prominent growth in the future are clear signs of the interest that people have in experiencing a new way of getting information/entertainment. The popular apps in which you can stream podcasts are Spotify, Apple Podcast, and Google Podcasts.
In this project we will take in consideration Spotify as one of the most used among people and also cause it has a good section for developers to retrieve data. As an avid podcasts consumer, I noticed that Spotify recommends only similar podcasts show but not episodes with similar content therefore I've decided to create one of my own.

## Objective
* Build an engine recommender to suggest podcasts with similar content of the one you are listening to.

## Tools and methods

### Trello - using agile method (Kanban)
organize the activities by dividing them into four main groups: to do, doing, done and review code. Check my [trello](https://trello.com/b/Ke2jn3vM/final-project-spotify-episodes-recommender)

### Github
Github is a code hosting platform for version control and collaboration. We used it to share the files and keep a backlock of the updates. Check our [repository](https://github.com/cosfer2804/FCDATA)

### Canva
To create the presentation

### Python
We divide the work done in python into two notebooks.
In the [classification_eda](https://github.com/cosfer2804/FCDATA/blob/main/python/classification_eda.ipynb) we did the cleaning steps:
* standardize headers name;
* EDA - review columns' distribution, counts and correlation
* check and fill the nulls;
* check duplicates;
* visualizations - Matplotlib and Seaborn to check if there are outliers
* Pre-processing: encode categories and scale numerics
* export the cleaned dataframe to a new csv.

In the [final model](https://github.com/cosfer2804/FCDATA/blob/main/python/classification_final.ipynb) notebook we did some cleaning and then run 9 different classification models:
* Train, test, split
* Define model
* Check accuracy of our classification model
* Fit the model to more balanced data
* Correlating categories with chi squared
* Fit the model to more balanced data using resampling techniques SMOTE and Tomelink and visualize with confusion_matrix and heatmap

### Models
To perform each model, we developed a for loop in which we applied Logistic Regression, Random Forest, KNeighbors and Gradient Boosting to the same dataframe. In this way, it was possible to compare and evaluate which methods obtained the best results.

So after testing nine different models, we decided to give attention to two of them that had a more relevant result. It is worth noting that each model represents two different marketing strategies. 

#### Model 1 - KNeighbors (using SMOTE for resampling)
Despite achieving only 69.6% accuracy, this model is the most ideal for implementing a marketing strategy that will focus on potential customers without losing those who have already accepted the offer. 

When we evaluate the confusion matrix, it is possible to notice that the model predicts 5.6% of true positives from the total number of customers, which corresponds to more than 90% of the customers who accepted the offer. On the other hand, we notice that the model predicts 30% false positives. However, in our case false positives are considered as possible customers. This way, we can use this model to design a marketing strategy to keep most of the customers that have already accepted the proposal and make new offers to potential customers. 

It is worth noting that the model only made statistical evaluations. Therefore, if there is any interest in implementing this strategy, financial planning is required to assess its viability.

<img width="400" alt="KNeighbors" src="https://github.com/cosfer2804/FCDATA/blob/main/screenshot/knn_best1.png">



### Insights
* The average balance increases esponentially from Q1 to Q3 in category A, while it  remains invariate in category D. Categories B and C have a linear average balance   grow from Q1 to Q3 and drop from Q3 to Q4.
* 62% of the clients that accepted the offer has low credit rating, followed by 26%  with medium creadit rating and only 12% with high credit rating.
* It seems that there is a preference in receiving the offer through postcard in the group who accepted the offer.

### Next Steps
To further deep dive into the study we might need some more demographic (age) and geographic (residence) information about the target. For istance, in some countries, people tend to go to holidays during Q2 and Q3, so therefore more money are kept in the bank account. Also, during holidays, people might need a credit card?

