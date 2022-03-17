![alt text](https://github.com/newgala/Final-Project/blob/main/spotify.png) 

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

![alt text](https://github.com/newgala/Final-Project/blob/main/chart.jpg) 

The rise of podcasts in the past years and their prominent growth in the future are clear signs of the interest that people have in experiencing a new way of getting information/entertainment. The popular apps in which you can stream podcasts are Spotify, Apple Podcast, and Google Podcasts.
In this project we will take in consideration Spotify as one of the most used among people and also cause it has a good section for developers to retrieve data. As an avid podcasts consumer, I noticed that Spotify recommends only similar podcasts show but not episodes with similar content therefore I've decided to create one of my own.

## Objective
* Build an engine recommender to suggest podcasts with similar content of the one you are listening to.

## Tools and methods

### Trello - using agile method (Kanban)
organize the activities by dividing them into four main groups: to do, doing, done and review code. Check my [trello](https://trello.com/b/Ke2jn3vM/final-project-spotify-episodes-recommender)

### Canva
To create the presentation.

### Python
I divide the work done in python into two notebooks.
In the [Data collection](https://github.com/cosfer2804/FCDATA/blob/main/python/classification_eda.ipynb):
* Collect up to 10000 episodes from Spotify API;
* Filter episodes search by 11 different topics using them as key words in the episodes title;
* Define a function to download more then 50 episodes at the same time as Spotify has a limit;
* Export the dataframe to a new csv.

In the [final model](https://github.com/cosfer2804/FCDATA/blob/main/python/classification_final.ipynb) 
* EDA - 
* Preprocessing
* Data tranformation
* Cosine similarity application
* User interface

#### MVP 1 - User interface
Despite achieving only 69.6% accuracy, this model is the most ideal for implementing a marketing strategy that will focus on potential customers without losing those who have already accepted the offer. 

<img width="400" alt="KNeighbors" src="https://github.com/cosfer2804/FCDATA/blob/main/screenshot/knn_best1.png">

### Insights
* The average balance increases esponentially from Q1 to Q3 in category A, while it  remains invariate in category D. Categories B and C have a linear average balance   grow from Q1 to Q3 and drop from Q3 to Q4.
* 62% of the clients that accepted the offer has low credit rating, followed by 26%  with medium creadit rating and only 12% with high credit rating.
* It seems that there is a preference in receiving the offer through postcard in the group who accepted the offer.

### Next Steps
To further deep dive into the study we might need some more demographic (age) and geographic (residence) information about the target. For istance, in some countries, people tend to go to holidays during Q2 and Q3, so therefore more money are kept in the bank account. Also, during holidays, people might need a credit card?

