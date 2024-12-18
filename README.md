
# Titanic: Kaggle Challenge Solution

This repository contains my solution for the famous Titanic Kaggle Challenge. The goal of the challenge is to predict whether a passenger survived or not based on specific features provided in the dataset.

## Problem Statement

The Titanic dataset is a classification problem where the target variable is `Survived`, indicating whether a passenger survived (`1`) or did not survive (`0`). Participants are tasked with building a predictive model based on the given passenger features such as age, sex, class, and fare.

## Features Used

- **Pclass**: Ticket class (1st, 2nd, 3rd)
- **Sex**: Gender of the passenger
- **Age**: Age of the passenger
- **SibSp**: Number of siblings or spouses aboard
- **Parch**: Number of parents or children aboard
- **Fare**: Ticket fare price
- **Embarked**: Port of Embarkation (C, Q, S)

## Solution Approach

### Data Cleaning and Preprocessing
- Minimal preprocessing, as **CatBoost** handles categorical variables natively.
- Handled missing values in features like `Age` and `Embarked`.


### Model Selection
- **CatBoost Classifier** was chosen due to its ability to handle categorical data without the need for one-hot or label encoding and its efficiency in handling missing values.
- The model was trained with the following parameters:
  - `iterations=1000`
  - `learning_rate=0.1`

### Model Training
- Code snippets for CatBoost model are available in the repository.

## Results

The model achieved an accuracy of **76.55%**.


## Future Work

- Experiment with additional feature engineering techniques.
- Test more advanced ensemble methods.
- Automate hyperparameter tuning with Bayesian Optimization.