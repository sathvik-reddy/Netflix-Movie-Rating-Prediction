# Netflix-Movie-Rating-Prediction
Objectives:

Predict the rating that a user would give to a movie that he has not yet rated.
Minimize the difference between predicted and actual rating (RMSE and MAPE)

Approach Used:

We start with doing the exploratory data analysis which helps us to know about total number of ratings given,the most frequent ratings given by most of the users,in what day of week most ratings are given etc

Then we split the data into train and test and we convert them into compressed sparse matrices

Then we try to compute user-user similarity which is very very expensive so we decide to compute the similarities only when required i.e during run time

And instead of training our models on all the users and movies we sample a subset of users and movies and then we create 13 features from the data

And then we apply various algorithms from surprise library and then we add their results also as features to our dataset and then we finally apply xgboost on the dataset to get good results

Of all the hyperparameter tuned algorithms "XgBoost with 13_features+Surprise Baseline+Surprise KNNbaseline + MF Techniques" performed well
