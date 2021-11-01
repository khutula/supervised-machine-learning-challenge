# GT Bootcamp Supervised Machine Learning Homework: Predicting Credit Risk

## Table of Contents
1. [Introduction](#introduction)
2. [Objectives](#objectives)
3. [Technologies & Tools](#technologies)
4. [Files & Links](#files)
5. [Analysis](#analysis)

<a name="introduction"></a>
### Introduction
In this assignment, I will be using data provided through LendingClub API to create a machine learning model that attempts to predict whether a loan will become high risk or not.  I will specifically be comparing the accuracy of the Logistic Regression model and Random Forest Classifier model.

<a name="objectives"></a>
### Objectives
Generate and test the accuracy of two supervised machine learning models by:
* Reading in the train and test datasets from the provided CSVs
* Dropping unneeded columns for both the test and train data sets
* Converting categorical data to numeric dummy variables for both the test and train data sets
* Separating out the target feature for both the test and train data sets
* Adding missing dummy variable to testing data set using calculations
* Training Logistic Regression model and Random Forest Classifier model on unscaled data
* Scaling the training and testing data sets
* Training Logistic Regression model and Random Forest Classifier model on scaled data

<a name="technologies"></a>
### Technologies & Tools
This project uses: 
* Python
* SKLearn Library
* Pandas Library
* Jupyter Notebook

<a name="files"></a>
### Files & Links

* [Credit Risk Evaluator Notebook]("Credit Risk Evaluator.ipynb"): GeoJSON data used for my map (earthquakes over last 30 days with a minimum magnitude of 4.5)
* [Raw Data Transformation](Resources/Generator): this raw data and generator file were provided in order to create the cleaner data files for use in model making
* [Train Data](Resources/2019loans.csv): 2019 data used to train our models
* [Test Data](Resources/2020Q1loans.csv): 2020 Q1 data used to test the accuracy of our models


<a name="analysis"></a>
### Analysis

#### Unscaled Models Prediction
I would expect the Random Forst Classifier to perform better on the unscaled data. Even though it is prone to overfitting, RFC is able to determine how much each feature contributes to the prediction, whereas Logistic Regression is going to see all features and weight them based on their scale, rather than their true value to the prediction.

#### Unscaled Models Comparison
On unscaled data, the Random Forest Classifier performed better. As stated above, it did perform some overfitting, but it was better able to determine the importance of each feature rather than weighting the importance based on the scale of the feature as Logisitc Regression did.

#### Scaled Models Prediction
I would expect the Logistic Regression to perform better on the scaled data. Now that the data has been scaled, one of the major drawbacks to Logistic Regression (being that it weights features based on their scale rather than true importance) has been eliminated. I would expect Random Forst Classifier to perform generally the same on the scaled data, since it generally isn't very susceptible to scaling differences in the first place, and I would expect it to again show some overfitting.

#### Scaled Models Comparison
On scaled data, the Logistic Regression performed much better. As stated above, removing issues with weighting features due to unscaled data has provided Logistic Regression with a clearer picture without pitfalling into overfitting. Random Forest Classifier overfitted again and as expected, performed generally the same as the unscaled data.