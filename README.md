# 5001_GameTime_Prediction


Based on what I have learnt from MSBD5001, here are major steps for this project:
Data Pre-processing for training and testing set
Data preprocessing: filling missing data in necessary columns and determine features (is_free, genres, categories, tags, reviews etc.) which are important to modeling.
Convert genres, categories, tags to dummy columns making the inside values usable.
Ensure the alignment between columns in training and testing data (if one is missing, fill '0' for all rows) in order to prevent crash in the modeling part later.

Feature Engineering
Modeling & Tuning
