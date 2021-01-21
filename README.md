# song-popularity-prediction
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/damilare-akin/song-popularity-prediction/main?filepath=popularity_prediction.ipynb)

This is a machine learning project to predict the popularity of a track on [Spotify](https://www.spotify.com/us/). 

## About the dataset
The dataset was sourced from [Kaggle](https://www.kaggle.com/yamaerenay/spotify-dataset-19212020-160k-tracks). The dataset contains 170,653 tracks from 1921 to 2020. It also contains 16 features. Visualizing feature importances reveals that 'year' is the most important predictor of the popularity of a track (Well, the Spotify documentation does state that popularity is calculated with respect to year). 

## Predicting popularity
The approach to predict popularity is simple. It is broken into four steps:
1. Create a simple decision tree model
2. Optimize the decision tree model with GridSearchCV
3. Tweak only the max_leaf_nodes parameter of the decision tree model
4. Create a random forest model

The random forest model has the best results, with a mean absolute error of 6.75.
Model | MAE
--- | ---
Simple decision tree | 9.196
Decision tree (GridSearchCV) | 6.942  
Decision tree (max_leaf_nodes) | 6.829  
Random Forest | 6.750 
