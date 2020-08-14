# Adult Salary 
## Project Motivation
Many binary classification tasks do not have an equal number of examples from each class, e.g. the class distribution is skewed or imbalanced.

A popular example is the adult income dataset that involves predicting personal income levels as above or below $50,000 per year based on personal details such as relationship and education level. There are many more cases of incomes less than $50K than above $50K, although the skew is not severe.

This means that techniques for imbalanced classification can be used whilst model performance can still be reported using classification accuracy, as is used with balanced classification problems.
## About the Data
The dataset provides 14 input variables that are a mixture of categorical, ordinal, and numerical data types. The complete list of variables is as follows:

Age.
Workclass.
Final Weight.
Education.
Education Number of Years.
Marital-status.
Occupation.
Relationship.
Race.
Sex.
Capital-gain.
Capital-loss.
Hours-per-week.
Native-country.
The dataset contains missing values that are marked with a question mark character (?).

There are a total of 48,842 rows of data, and 3,620 with missing values, leaving 45,222 complete rows.

There are two class values ‘>50K‘ and ‘<=50K‘, meaning it is a binary classification task. The classes are imbalanced, with a skew toward the ‘<=50K‘ class label.

‘>50K’: majority class, approximately 25%.
‘<=50K’: minority class, approximately 75%.
## Explore the Data
Imbalanced Classification with the Adult Income Dataset
by Jason Brownlee on March 6, 2020 in Imbalanced Classification
Tweet  Share
Many binary classification tasks do not have an equal number of examples from each class, e.g. the class distribution is skewed or imbalanced.

A popular example is the adult income dataset that involves predicting personal income levels as above or below $50,000 per year based on personal details such as relationship and education level. There are many more cases of incomes less than $50K than above $50K, although the skew is not severe.

This means that techniques for imbalanced classification can be used whilst model performance can still be reported using classification accuracy, as is used with balanced classification problems.

In this tutorial, you will discover how to develop and evaluate a model for the imbalanced adult income classification dataset.

After completing this tutorial, you will know:

How to load and explore the dataset and generate ideas for data preparation and model selection.
How to systematically evaluate a suite of machine learning models with a robust test harness.
How to fit a final model and use it to predict class labels for specific cases.
Discover SMOTE, one-class classification, cost-sensitive learning, threshold moving, and much more in my new book, with 30 step-by-step tutorials and full Python source code.

Let’s get started.

Develop an Imbalanced Classification Model to Predict Income
Develop an Imbalanced Classification Model to Predict Income
Photo by Kirt Edblom, some rights reserved.

Tutorial Overview
This tutorial is divided into five parts; they are:

Adult Income Dataset
Explore the Dataset
Model Test and Baseline Result
Evaluate Models
Make Prediction on New Data
Adult Income Dataset
In this project, we will use a standard imbalanced machine learning dataset referred to as the “Adult Income” or simply the “adult” dataset.

The dataset is credited to Ronny Kohavi and Barry Becker and was drawn from the 1994 United States Census Bureau data and involves using personal details such as education level to predict whether an individual will earn more or less than $50,000 per year.

The Adult dataset is from the Census Bureau and the task is to predict whether a given adult makes more than $50,000 a year based attributes such as education, hours of work per week, etc..

— Scaling Up The Accuracy Of Naive-bayes Classifiers: A Decision-tree Hybrid, 1996.

The dataset provides 14 input variables that are a mixture of categorical, ordinal, and numerical data types. The complete list of variables is as follows:

Age.
Workclass.
Final Weight.
Education.
Education Number of Years.
Marital-status.
Occupation.
Relationship.
Race.
Sex.
Capital-gain.
Capital-loss.
Hours-per-week.
Native-country.
The dataset contains missing values that are marked with a question mark character (?).

There are a total of 48,842 rows of data, and 3,620 with missing values, leaving 45,222 complete rows.

There are two class values ‘>50K‘ and ‘<=50K‘, meaning it is a binary classification task. The classes are imbalanced, with a skew toward the ‘<=50K‘ class label.

‘>50K’: majority class, approximately 25%.
‘<=50K’: minority class, approximately 75%.
Given that the class imbalance is not severe and that both class labels are equally important, it is common to use classification accuracy or classification error to report model performance on this dataset.

Using predefined train and test sets, reported good classification error is approximately 14 percent or a classification accuracy of about 86 percent. This might provide a target to aim for when working on this dataset.

Next, let’s take a closer look at the data.

Want to Get Started With Imbalance Classification?
Take my free 7-day email crash course now (with sample code).

Click to sign-up and also get a free PDF Ebook version of the course.

Download Your FREE Mini-Course
Explore the Dataset
The Adult dataset is a widely used standard machine learning dataset, used to explore and demonstrate many machine learning algorithms, both generally and those designed specifically for imbalanced classification.

First, download the dataset and save it in your current working directory with the name “adult.csv”

https://archive.ics.uci.edu/ml/datasets/Adult 
