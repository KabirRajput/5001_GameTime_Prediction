# 5001_GameTime_Prediction

Jeremy is a core video game player. He has collected more than 400 video games with different types and played more than 100 of them. Your task is to predict how many hours Jeremy has spent on each game, given some of the game features including the purchased time, price, release date, popular user-defined tags, etc. 80% of the dataset is provided as the training data including playing time, the rest are used as testing data, where only features are provided. You have to submit the predicted results of these testing samples, which are then compared with the ground truth to evaluate the performance of your model.

I pick 2 models to do prediction- 
The first one is xgboosting, a tree based model, quite popular among Kaggle projects. 
The second one is K Nearest Regressor

## Major Steps 

* Data Pre-processing for training and testing set
  * Imputation
  * Datetime
  * Categorical Variable Transformation
  
* Normalization
* Feature Engineering
* Modeling & Tuning


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

What things you need to install the software and how to install them

```
xgboost, sklearn, seaborn, matplotlib, numpy, scipy, pandas, xgboost
```

## Data cleaning & Normalization

#### nan values  
Firstly, I checked nan values in every column and found two rows, row 5 and row 76 had nan values for column total_positive_values and total_negative_values. I removed NaN where I found them and had also replaced them with 0/mean/meadian where I found appropriate 

#### Categorical-based values 
I used dummy variable for one hot encoding the categorical features

#### date  
There are two columns about date. In order to utilize them better, I transformed them from text to python datetime object.
I further transformed them to difference between the dates to make better use of the data

#### True/False 
A simple boolean Transformation to 0/1

## Feature Engineering : A little insights into the features 

There are 20 different genres in total in training data. They are:

```
['Adventure', 'Casual', 'Indie', 'RPG', 'Action', 'Strategy', 'Simulation', 'Racing', 'Sports', 'Massively Multiplayer', 'Sexual Content', 'Violent', 'Free to Play', 'Early Access', 'Audio Production', 'Gore', 'Design & Illustration', 'Nudity', 'Animation & Modeling', 'Utilities']
```

There are 29 different categories in total in training data. They are:

```
['Single-player', 'Steam Trading Cards', 'Steam Cloud', 'Partial Controller Support', 'Full controller support', 'Multi-player', 'Steam Achievements', 'Steam Workshop', 'Co-op', 'Steam Leaderboards', 'Online Co-op', 'Local Co-op', 'Shared/Split Screen', 'Stats', 'Online Multi-Player', 'Cross-Platform Multiplayer', 'SteamVR Collectibles', 'Local Multi-Player', 'Remote Play on Phone', 'Remote Play on Tablet', 'Remote Play on TV', 'Valve Anti-Cheat enabled', 'Commentary available', 'Captions available', 'Includes level editor', 'In-App Purchases', 'VR Support', 'MMO', 'Includes Source SDK']

```

There are 312 different tags in total in training data. I have only chosen the top ones based on the frequency to display here
```
['Atmospheric', 'Great Soundtrack', 'Story Rich', 'Multiplayer', 'RPG', 'Open World', 'Strategy', 'Co-op', 'Fantasy', 'Sci-fi', 'Masterpiece', 'Simulation', '2D', 'First-Person', 'Puzzle', 'Third Person', 'Shooter', 'Funny', 'Casual', 'Survival', 'Difficult', 'Horror', 'Sandbox', 'Exploration', 'Female Protagonist', 'Early Access', 'Comedy', 'FPS', 'Gore', 'Point & Click', 'Online Co-Op', 'Choices Matter', 'Classic', 'Space', 'VR', 'Violent', 'Turn-Based', 'Platformer', 'Dark', 'Moddable', 'Hack and Slash', 'Local Co-Op', 'Mystery', 'Stealth', 'Nudity', 'Retro', 'Action RPG', 'Psychological Horror', 'Building', 'Isometric', 'Third-Person Shooter', 'Replay Value', 'Pixel Graphics', 'Mature', 'Walking Simulator', 'Short', 'Post-apocalyptic', 'Character Customization', 'Tactical', 'Free to Play', 'Massively Multiplayer', 'Crafting', 'Controller', 'Rogue-like', 'RTS', 'Historical']

```

## Modelling

Model  | RMSE
------------- | -------------
KNeighborsRegressor  | 3.057698
ExtraTreesRegressor   | 3.956182
AdaBoostRegressor  | 4.542664
ExtraTreeRegressor   | 4.959477
BaggingRegressor  |  5.249035
GradientBoostingRegressor   | 5.700217
RandomForestRegressor  | 5.724474
PassiveAggressiveRegressor   | 7.688060


## Authors

* **Kabir Rajput 20560795**  

## Acknowledgments

* MSBD5001 Course Team - Professor and TA 
