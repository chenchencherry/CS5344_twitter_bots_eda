# CS5344_twitter_bots
## General Information
Recently, a large number of social bots have emerged and spread on social media that can affect  users' lives in different ways. Hence, bot detection becomes more and more important and takes more public attention. In this project, we analyze the difference between the features of human accounts and bot accounts on twitter.

## Datasets
Kaggle: Twitter Bots Accounts cbbb9288-f
https://www.kaggle.com/code/kerneler/starter-twitter-bots-accounts-cbbb9288-f/data

## Features
The features for this classification model is account-level information of Twitter users.

created_at： the hour a certain account is created

default_profile: whether an account has a default profile

default_profile_image: whether an account uses default profile image

favourites_count: total number of favourites an account has made

followers_count: total number of followers

friends_count: total number of friends

geo_enabled: whether an account opens positioning

statuses_count: total number of tweets

verified: whether the account is verified

average_tweets_per_day: number of tweets posted per day

popularity: metric of account’s importance in social relationship

favourites_rate: number of favourites tweets per day

follower_rate: number of followers per day

friend_rate: number of friends per day

## EDA
1. Around ⅓ of human account using default profile, however the percentage of bot account is twice than the human account.
2. 0.7% of human account using default profile picture, versus 3.1% of bot account. This might be due to the bot account owner only requires some basic functions of the twitter account and it’s not necessary to edit profile information. 
3. Human are more likely to post this info when they visit any landmark or locate at some important places.
4. The average popularity of human is almost 3 times as much as bot which means human account are more popular and ‘active’ in the network relationship. The peak of bot pattern is close to 0 that is the majority of bot accounts have very few followers or friends.
5. Human and bot accounts are very similar in terms of average tweets per day. However, there are huge difference on the favourites count: human account has around 3.3 times as many as bot account. It’s probably that bot can imitate part of human social activities such as sending tweets. However, human may click ‘favourite’ button when they browse interesting tweets. Bot won’t spend time on it.

##  Model evaluation and results
KNN, LogisticRegression, SVM, NaiveBayes (Gaussian, Bernoulli, Multinomial), Decision Tree, RandomForest, XGBoost, LightGBM, CatBoost are the chosen models

Final model(LightGBM) scores

Accuracy: 87.74%
Precision: 80.16%
Recall: 75.61%
ROC AUC: 85.28%

## Suggestions for future work
1. Implement the text classification of the tweet text and use it as a feature to train the model.
2. Implement deep learning models such as CNN and RNN.
3. Further research on bot community detection based on graph and social network.
