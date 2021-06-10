# Amazon-Book-Recommendation-Framework

## CHAPTER 1-  OBJECTIVES AND INTRODUCTION 

### 1.1 OBJECTIVE : 
The main objective is to create a machine learning model to recommend relevant books to users based on popularity and user interests.
In addition to the ML Model prediction, we also have taken into account the book recommendation for a totally new user.  

### 1.2 INTRODUCTION:  			

During the last few decades, with the rise of Youtube, Amazon, Netflix, and many other such web services, recommender systems have taken more and more place in our lives. From e-commerce (suggest to buyers articles that could interest them) to online advertisement (suggest to users the right contents, matching their preferences), recommender systems are today unavoidable in our daily online journeys.   

In a very general way, recommender systems are algorithms aimed at suggesting relevant items to users (items being movies to watch, text to read, products to buy, or anything else depending on industries).   

Recommendation systems are really critical in some industries as they can generate a huge amount of income when they are efficient or also be a way to stand out significantly from competitors. The main objective is to create a book recommendation system for users.   

Since, here we are trying to recommend books to users based on their past purchases or ratings the user gave previously, we are basically trying different models like Popularity based recommender system, Collaborative filtering based recommender system (user-item or item-item) etc. We will be using the Popularity based recommender system to deal with the cold start problem, where we do not have history of past purchases of a particular user or where the user is totally new.  

The next chapters have the following sections which are the steps involved for solving the Book Recommendation System,   
Section 1 - Data collection   
Section 2 - Data preparation  
Section 3 - Exploratory data analysis   
Section 4 - Feature Engineering  
Section 5 - Working different models  
Section 6 - Evaluating model  

## CHAPTER 2 -  DATA COLLECTION AND DATA PREPARATION

### 2.1 Data Summary:
We are using Book-Crossing dataset to train and test our recommendation system. Book-Crossings is a book ratings dataset compiled by Cai-Nicolas Ziegler. It contains 1.1 million ratings of 270,000 books by 90,000 users. The ratings are on a scale from 1 to 10. The Book-Crossing dataset comprises 3 files.   
● Users   
This .csv file contains the users. Note that user IDs (User-ID) have been anonymized and map to integers. Demographic data is provided (Location, Age) if available. Otherwise, these fields contain NULL values.   
● Books   
Books are identified by their respective ISBN. Invalid ISBNs have already been removed from the dataset. Moreover, some content-based information is given (Book-Title, Book-Author, Year-Of-Publication, Publisher), obtained from Amazon Web Services. Note that in the case of several authors, only the first is provided. URLs linking to cover images are also given, appearing in three different flavors (Image-URL-S, Image-URL-M, Image-URL-L), i.e., small, medium, large. These URLs point to the Amazon website.  
● Ratings     
Contains the book rating information. Ratings (Book-Rating) are either explicit, expressed on a scale from 1-10 (higher values denoting higher appreciation), or implicit, expressed by 0  
 
### 2.2 Data Collection  
Before building any machine learning model, it is vital to understand what the data is, and what are we trying to achieve. Data exploration reveals the hidden trends and insights and data preprocessing makes the data ready for use by ML algorithms.  
 
So, let’s begin. . .  
To proceed with the problem dealing first we will load our dataset that is given to us in a .csv file into a dataframe.  
