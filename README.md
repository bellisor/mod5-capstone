# mod5-capstone
Final Project for Flatiron School DS program

## Problem Statement

Steam is a web-based marketplace for PC games, the largest PC game distribution platform in the world. Between 2005 and 2015 there was 6000 games in total on Steam. Now, roughly 6000 games get added per year. Now there are over 37,000 games on steam. With this amount of content on steam, it is becoming more and more difficult for users to find games they’d like to play. The aim of this project is to create a recommendation system to help users find games.

## Datasets:
•	Steam API
•	SteamSpy API
•	Kaggle Dataset

## Executive Summary

For this project, we used three datasets: two made from API calls and one from Kaggle consisting of Yser ID’s and game behavior. The first step was to call a list of all game appid’s from SteamSpy. This list was then ran through both Steam and SteamSpy to get two dataframes with information about the game. In total there was over 37,000 unique games with 3,700 unique metascores. We also engineered some features to reflect User Score based on SteamDB’s userscore algorithm. 

With all of this information, we then create a linear model to predict metascores for all games on Steam. The best model for this was an XGBoost model that gave us an RMSE of 8 which is great because that puts us within standard deviation of metascores. We chose RMSE as the evaluation metric because its more important to have scores in relationship with eachother rather than the actual number itself. 

From there, we create three matrices of user behavior (purchased or played a game), confidence (amount of hours put into a game) and scores (metascores for those games. Using collaborative filtering techniques in TensorFlow, we then train a model that predicts and recommends games.

Overall, the recommendation works fairly well. Even with such a low precision score (0.80) the games that are recommended still fall within similar genre and scope to games the user purchased. Currently, the recommendation system only contains about 3600 games. I’d like to expand its library and also create a better metric evaluation that accounts for genre and other tags. 

## Files:

## References:

Shout out to all my gamer friends who have helped me over the years to learn so much about the industry: Relgrim, Proth, Grandpoobah, and so many others. 

## Outside Sources:
1. https://www.kaggle.com/tamber/steam-video-games
2. https://www.kaggle.com/danieloehm/steam-game-recommendations
3. https://steamcommunity.com/dev
4. https://steamspy.com/
5. https://steamdb.info/blog/steamdb-rating/
6. https://nik-davis.github.io/posts/2019/steam-data-collection/


