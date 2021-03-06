# Merck_Challenge_Hyperparameter_Tuning
**Author:** Yuhsiang (Sean) Hong

## Introduction
Hyperparameters tuning has been an exceptional technique for scientists to optimize the machine learning models. However, different models contain various hyperparameters. The questions of which hyperparameters are suitable to tune or if there is an optimal hyperparameter configuration for each model across all the real-world datasets or if there is a best method to tune hyperparameters have been investigated by many researchers. Therefore, the paper will base on the concept in the reference paper (Probst et al.) and focus on the tunability of hyperparameters and inspecting the methods that is practical and productive in tuning hyperparameters for QSAR datasets.


## Evaluation Strategy
There are several steps should be done before hyperparameters tuning. First of all, since the dependent variables of QSAR datasets are continuous, both MSE (mean squared error) and RMSE (root-mean-squared error) are simple and clear to compare the performance of different models. Therefore, RMSE will be used as my evaluation criteria. Secondly, applying K-fold cross-validation for each hyperparameter combination can reduce overfitting and selection bias. The mean of the average of K test RMSE across all the datasets will be the evaluation standard for different hyperparameter combinations. Lastly, the hyperparameter combination with the lowest mean of RMSE across datasets will be the optimal hyperparameter combination. Namely, what should be done for each trial in hyperparameter tuning methods is to create different models on different datasets but with the same hyperparameter combination. The objective function is the mean of test RMSE across all the datasets and the goal is to minimize it.

## Dataset
The simulated datasets are generated by the package `make_friedman1` from `sklearn.datasets` in Python. There are 27 datasets in total with different numbers of rows, numbers of columns, and noises. For the QSAR datasets, there are 15 datasets with over 150,000 observations and train and test datasets are provided seperately.

## Package
All the following packages are used in this project:
`pandas`, `numpy`, `sklearn`, `optuna`, `xgboost`, `seaborn`, `matplotlib`.

## Result
Awarded 1st place from the BARDS research group at Merck and Statistics Deparemnt at Rutger University
