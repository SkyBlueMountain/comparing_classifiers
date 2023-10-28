# comparing_classifiers


# Practical Application III: Comparing Classifiers

## Overview

In this practical application, our goal is to compare the performance of various classifiers using a dataset related to marketing bank products over the telephone. The dataset is obtained from the UCI Machine Learning repository [link](https://archive.ics.uci.edu/ml/datasets/bank+marketing). It represents the results of multiple marketing campaigns conducted by a Portuguese banking institution.

## Getting Started

The dataset, along with additional information, can be found in the link provided. To get started, please review the information in the dataset link and the accompanying article [here](CRISP-DM-BANK.pdf) for a better understanding of the data and its features.

## Problem 1: Understanding the Data

The dataset represents a total of 17 marketing campaigns conducted by the Portuguese banking institution.

## Problem 2: Read in the Data

We read the dataset using Pandas and assigned it to the variable `df`.

## Problem 3: Understanding the Features

Upon examining the features in the dataset, we found that there are no missing values, and the data types are correctly assigned to each column.

## Problem 4: Understanding the Task

Our business objective is to predict whether a client subscribed to a term deposit ('yes' or 'no') based on the given features.

## Problem 5: Engineering Features

We prepared the features and target column for modeling by encoding categorical variables using one-hot encoding. The relevant features (columns 1 - 7) were selected for modeling, and the target variable was mapped to binary values ('yes' -> 1, 'no' -> 0).

## Problem 6: Train/Test Split

The dataset was split into training (70%) and testing (30%) sets to evaluate model performance.

## Problem 7: A Baseline Model

We established a baseline accuracy of approximately 88.76% for the target variable 'y' (subscription to a term deposit).

## Problem 8: A Simple Model

We built a basic Logistic Regression model and achieved an accuracy of 88.76%.

## Problem 9: Score the Model

The Logistic Regression model achieved an accuracy of 88.76%.

## Problem 10: Model Comparisons

We compared the performance of the Logistic Regression model with other classifiers, including K Nearest Neighbor, Decision Tree, and Support Vector Machines (SVM). The results are presented below:

| Model               | Train Time (s) | Train Accuracy | Test Accuracy |
| ------------------- | --------------- | -------------- | ------------- |
| Logistic Regression | 0.3655          | 0.8876         | 0.8874        |
| KNN                 | 17.0196         | 0.9098         | 0.8812        |
| Decision Tree       | 0.8913          | 0.8912         | 0.8771        |
| SVM                 | 291.3415        | 0.8953         | 0.8839        |

## Problem 11: Improving the Model

In our pursuit to improve the model, we explored several avenues:

### More Feature Engineering and Exploration

1. **Gender Feature**: We considered the 'sex' feature but did not include it in the models. Further analysis is needed to determine its impact on the target variable.

### Hyperparameter Tuning and Grid Search

2. **Logistic Regression**: We performed hyperparameter tuning but did not achieve a significant improvement. Further exploration of hyperparameters is warranted.

### Adjusting the Performance Metric

3. **Performance Metric**: We noted that precision, recall, F1 Score, and ROC AUC were low, especially for the positive class ('yes'). Adjusting the performance metric to prioritize recall or F1 Score may be necessary, given the imbalanced dataset.

The improvement process will continue iteratively through feature engineering, hyperparameter tuning, and performance metric adjustment to enhance model accuracy and effectiveness.
