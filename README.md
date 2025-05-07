# Machine Learning 2 Final Project Repository

## Overview 

The goal of this project was to predict the outcome of all hypothetical matchups between both mens and womens NCAA teams in order to correctly predict each stage of the NCAA March Madness Tournaments. The task was to forecast the probability of one team beating another across all possible matchups for the 2025 tournaments. This task was originally taken on as an independent project during the semester, and was submitted to the March Machine Learning Mania Kaggle competition. After the competition the project was continued and improved upon for final presentation and submission. 

## Data

The primary dataset this project uses was provided by Kaggle as a measure of the competition, and can be reproduced as long as one has a Kaggle account and signs up for the same competition. This data included historical results for mens and womens teams for both the regular season and tournament. The dataset also provided data on coaches win records, conference results, etc. For a comprehensive descriptions of the data please visit the [Kaggle competition page](https://www.kaggle.com/competitions/march-machine-learning-mania-2025/data). 
Additionally for the XGBoost model outside data was implemented. 538 Rankings were leveraged to provide a 'score' for a team other than seed, so that seed wasn't leaned on so heavily in the model.

## Models Implemented

### 1. Deep Learning Model

- Utilized a neural network to learn complex, non-linear relationships in historical tournament data.
- Input features included detailed statistics such as shooting percentages, rebounds, assists, turnovers, and historical seed differences.
- The model was trained to minimize mean squared error (MSE), corresponding to the Brier Score evaluation metric.

### 2. Matrix Completion Model

- Implemented matrix completion techniques (specifically SVD++) to estimate missing values and predict outcomes.
- Matrix was constructed using historical regular season data to generate a score difference between two teams.
- Regularized model to manage overfitting and capture long-term patterns in team performance data.

### 3. XGBoost Model

- Ultimately utilized an XGBoost model heavily based on the notebook provided by Kaggle user [raddar](https://www.kaggle.com/code/raddar/vilnius-ncaa), who found that the less time he spent on the competition, the better performance he saw from his model. This simple model was the groundwork for the top performers in this years competition, and using our hindsight we built a model designed purely to win the competition.
- Model trained on engineered features including recent performance metrics, seeds, and historical matchup outcomes.
- Optimized with grid search for hyperparameters such as max depth, learning rate, and regularization terms to ensure robust predictions.


## Conclusion

This project combined deep learning, matrix completion, and gradient boosting methods to create robust predictive models for NCAA tournament outcomes. Future improvements could involve feature engineering enhancements, additional hyperparameter tuning, and model ensembling techniques to further refine predictions.
