## Dennis Tran, DSI-Deckard

## Instructors: Gwen Rathgeber, Heather Robbins, Anderson Prewitt

## Problem Statement

A Multimedia Company who owns several Youtube channels specializing on reposting narrated Reddit posts seeks to automate its post collection. 
Of interest are two subreddits, r/NoSleep and r/IDontWorkHereLady, known for user submitted stories.
Our team’s task is to create a machine learning model that can determine where a post came from.


## Executive Summary

1. Using Pushift, an API for Reddit, we scraped over 20,000 user submitted posts from r/NoSleep and r/IDontWorkHereLady.
2. We then cleaned and formatted our data into a dataframe of 10,000 total posts.
3. Count Vectorized to show word frequencies.

Then we created our models by taking a 10% sample of the 10,000 dataframe. Accuracy was our primary objective:
1. Two Multinomial Naive Bayes models
2. A Ridge Regression
3. A Lasso Regression
4. Two Random Forest Classifiers


## Conclusions and Recommendations

Our Multinomial Naive Bayes models, with an accuracy score of 98.8%, were the best at predicting where a post came from. They were the least overfit, albeit by less than a single percent, than the other models we tested. We believe accuracy can be improved, but would take a considerable amount of time and resources for a very miniscule increase in percentage. A company could use our model to automatically identify which subreddit a post came from, but there are other cost-effective ways that do not involve machine learning.


## Sources

1. [r/NoSleep](https://www.reddit.com/r/nosleep/)
2. [r/IDontWorkHereLady](https://www.reddit.com/r/IDontWorkHereLady/)


## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|title|object|nosleep, tale, both|The title of the subreddit post| 
|selftext|object|nosleep, tale, both|The body of text of the subreddit post| 