# SQ-Offensive-Rebounding

Link to Kaggle Leaderboard (I came in first place!): https://www.kaggle.com/competitions/shotquality-rebounding/leaderboard

# **Predicting Offensive Rebounds in Basketball: A Location-Based Approach**

Basketball is a fast-paced sport, rich in strategies and opportunities for data analysis. One critical moment that can shift the momentum of a game is the rebound after a missed shot. The ability to anticipate and secure an offensive rebound can create additional opportunities to score, making it a valuable skill on the court. The challenge presented here is to leverage the on-court location data of players to predict the probability of a team securing an offensive rebound after a shot miss.

## Dataset Overview

The datasets provided for this challenge come in two flavors:

1. *Play-by-Play Data (PBP)*: This dataset captures play-level details. Crucially, it records the team names, and for the training set, whether a rebound is offensive or defensive.

2. *Location Data (Locs)*: This is the centerpiece of the challenge. For each play, it records the on-court coordinates of each player **at the moment a shot is taken**. This dataset differentiates between the shooter, the offensive players, and the defensive players.

A critical note is that all the shots considered in both the training and test sets are misses, which are then rebounded either offensively or defensively.

## Objective

Given this data, the task is to predict the likelihood of an offensive rebound post a missed shot. The prediction will be based on the positions of the players at the time of the shot.

## My Approach

In my exploration of this problem, I have undertaken a comprehensive approach to feature engineering and model testing:

1. <u>Distance Features</u>:           Calculated distances between key players and positions to gauge the immediate opportunity or challenge in securing a rebound.

2. <u>Angle Features</u>:              Considered angles to understand players' relative positions to the basket.

3. <u>Box-Out Responsibility</u>:      Paired players based on potential matchups, considering 'boxing out' in rebound scenarios.

4. <u>Complex Feature Engineering</u>   Developed features using the results of EDA and basketball domain knowledge

4. <u>Hyperparameter Tuning</u>:        Tuning hyperparameters using gridsearch crossvalidation.

5. <u>Building an Ensemble</u>:         Combining the prediction power of several diverse ML algorithms to leverage the strengths of each model.

6. <u>Model Exploration</u>:           Beyond traditional algorithms, I experimented with Graph Neural Networks (GNNs) and Convolutional Neural Networks (CNNs) to capture the spatial relationships between players.
