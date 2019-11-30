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



## Authors

* **Kabir Rajput 20560795** - 

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* MSBD5001 Course Team - Professor and TA 
