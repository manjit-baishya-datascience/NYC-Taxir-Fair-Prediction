# **NYC Taxi Fare Prediction**

This project aims to predict taxi fare amounts in New York City using a dataset of historical taxi rides. We employ machine learning techniques to create models that can estimate the total fare amount based on various features of the trips.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Feature Engineering](#feature-engineering)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Results](#results)

## Introduction
The goal of this project is to build a machine learning model that can predict the total fare of a taxi trip given several input features such as pickup and dropoff locations, time of day, trip duration, and other relevant attributes.

## Dataset
The dataset used in this project is the NYC Taxi Trip Data. The data includes information such as pickup and dropoff dates and times, locations, passenger count, trip distance, and fare amount.

## Data Preprocessing
We start by loading the dataset and performing the following preprocessing steps:

1. **Convert datetime columns**: Split the pickup and dropoff datetime columns into separate date and time columns to capture temporal features more effectively.
2. **Calculate trip duration**: Compute the trip duration in minutes, which is a critical feature for fare estimation.
3. **Handle missing values**: Impute or drop rows with missing values to ensure data quality.
4. **Encode categorical variables**: Use one-hot encoding to transform categorical features into a format suitable for machine learning algorithms.

## Feature Engineering
Feature engineering involves creating new features or transforming existing ones to improve model performance. For this project, we consider:

- **Categorical features** such as rate codes, pickup and dropoff locations, payment types, and trip types.
- **Numerical features** including the number of passengers, trip distance, fare components (base fare, extras, taxes, tips, tolls, improvement surcharges, and congestion charges), and trip duration.

## Modeling
We use various regression models to predict the total fare. The models used include:

- **Random Forest Regressor**: A robust ensemble learning method that builds multiple decision trees and merges them to get a more accurate and stable prediction.
- **Decision Tree Regressor**: A simple yet powerful model that splits the data into subsets based on the feature that results in the most significant information gain.

## Evaluation
The performance of the models is evaluated using the following metrics:

- **Mean Absolute Error (MAE)**: Measures the average magnitude of the errors in a set of predictions, without considering their direction.
- **Mean Squared Error (MSE)**: Measures the average of the squares of the errors, which gives more weight to larger errors.
- **Root Mean Squared Error (RMSE)**: The square root of the mean squared error, providing a measure of error in the same units as the target variable.
- **R-squared (R²)**: Indicates the proportion of the variance in the dependent variable that is predictable from the independent variables.

## Results
The results section includes the performance metrics for each model, comparing how well they predict the total fare amount. This helps in understanding which model performs best and could be used for real-world fare prediction.

By following these steps, we aim to create a reliable model for predicting NYC taxi fares, which can be useful for various stakeholders including taxi companies, passengers, and policymakers.