![alt text](https://github.com/newgala/Final-Project/blob/main/pics/spotify.png) 

# FINAL PROJECT - SPOTIFY PODCASTS EPISODES ENGINE RECOMMENDER

By: <br/>
[Angela Wang](https://www.linkedin.com/in/angela-wang-716632b1/)

## Table of Contents
- [Scenario](#scenario)
- [Objective](#objective)
- [Tools and Methods](#tools-and-methods)

## Scenario

![alt text](https://github.com/newgala/Final-Project/blob/main/pics/chart.jpg) 

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

[Spotify API data collection](https://github.com/newgala/Final-Project/blob/main/Spotify%20episodes%20recommender%20-%20wrapper%20API.ipynb):
* Collect up to 10000 episodes from Spotify API;
* Filter episodes search by downloading titles that only contains our 11 selected topics as keywords;
* Define a function to download more then 50 episodes/time as Spotify has a limit of 50 episodes/time;
* Export the dataframe to a new csv.

[Spotify user interface](https://github.com/newgala/Final-Project/blob/main/Spotify%20podcasts%20recommender%20-%20MVP%201%20user%20interface%20.ipynb) 

* Data cleaning: drop nulls values, check for duplicates, tokenize and lemmatize the text;
* Preprocessing: Transfor text into vectors using TfidfVectorizer;
* Apply cosine similarity to text (description+title) to find the similarity scores of the whole episodes;
* Built user interface.
