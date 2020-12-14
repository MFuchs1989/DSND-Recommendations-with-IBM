

![IBM](images/IBM.png)


# Recommendations with IBM
This project was part of the Data Science Nanodegree with Udacity. The aim of the project is to develop a recommendation engine for suggesting new articles to the IBM Watson Community users.

## Introduction
This project focuses on analyzing interactions between users and articles on the IBM Watson Studio platform. New article recommendations are made to users based on their interactions. Based on the data available, we can use various methods to make these recommendations. The methods used here are Rank Based, Collaborative Filtering, and Matrix Factorization.

## Rank Based Recommendations
Since there are no ratings for articles the most popular articles are represented by their interactions with users. We only know if the user has or has not interacted with an article. We can simply count the amount of times an article was interacted with by users and proclaim it to be the most popular. This is especially useful for making recmomendations to new users for whom we have no existing data.

## User-User Collaborative Filtering
Finding similar users based on article interactions may lead to better and more personalized recommendations. First step is to create a user-item matrix where each row is a unique user and each column is a unique article. Each interaction is represented by a 1 which results in the creation of a sparse matrix. Similarity refers to a pair of users reading same articles. This involves identifying similar users, extracting the articles which they read, and recommending unique articles which were seen by one user but not the other.

Content-based recommendations were performed based on NLP methods; text similarity of the article titles was calculated as the dot product of text vectors for each title. CountVectorizer and Tidf

## Matrix Factorization
Here we can use the user-item matrix again to provide recommendations by performing Singular Value Decomposition (SVD). Using this method allows for predicting the user-article interaction. By breaking down the user-item matrix into a product of three matrices we can extract latent features (Sigma matrix) which indicate some relationship between the user and article. Predictions are made by varying the amount of latent features we choose to keep.

## Installations:
There is no installation required. You just need Jupyter-Notebook, e.g. from an Anaconda installation. Make sure that you also have Numpy, Pandas, Matplotlib, and pickle.

## Project Motivation: 
Goal was to develop concepts for the recommendation of articles.
