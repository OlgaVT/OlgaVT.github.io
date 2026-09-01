---
title: "Basics on Bioinformatics and Systems Biology: Lecture 7"
collection: teaching
type: "Lecture"
permalink: /teaching/bbsb_lecture_7
venue: "VU"
date: 2026-01-10
location: "Amsterdam, the Netherlands"
---

Here you will find the basic concepts for the Lecture 7 and links to the additional/support material

Materials:

The Kaggle course on [Machine learning](https://www.kaggle.com/learn/intro-to-machine-learning)

[The Deep Learning textbook](https://www.deeplearningbook.org/)


## Machine learning

| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_3.jpg" width="25000">  | **Machine learning** (in simple words) is a set of approaches to find a function (or a rule) that defines the relationship between an input and an output.|[Kaggle ML community](https://www.kaggle.com/)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_6.jpg" width="25000">  | **Supervised machine learning** operates with the labeled data. **Label** is the value for the **regression** task or the category for the classification task that a machine learning model is used to predict. **Unsupervised machine learning** operates with unlabeled data and is used to find patterns in such a data.||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_8.jpg" width="25000">  | <ul>Supervised machine learning terms: <li>**Predictor variables** (**also independent varianles, features**) are input values used to predict **Target variables** (**also dependent variables**).</li><li>**A model** is a rule or a function that defines the relationship between predictor and target variables.</li><li>Aim is to predict target variable from predictor</li></ul>||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_16.jpg" width="25000">  | <ul>Steps to implement a machine learning model <li>Define a problem as specific as possible(e.g., build a model to predict a cancer prognosis: bad prognosis or good prognosis)</li><li>Think what kind of data can be collected and used to address the problem and validate the model. Collect and clean the data (e.g., gene expression data from canncer patients with different prognosis)</li><li>Choose and implement an appropriate model that can address your problem.</li><li>Validate your model using an appropriate validation approach</li></ul>|[Example: Breast cancer outcome prediction](https://www.nature.com/articles/415530a)|


## Regression

| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_23.jpg" width="25000">  | **Regression** is a supervised learning technique to predict continous numerical values (e.g., survival rate, gene expression level, age, etc).||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_27.jpg" width="25000">  | **Simple linear regression** models the relationship between one predictor varioable and a continous numerical dependent variable by fitting a straight line. The model is based on a linear dunction equation.||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_27.jpg" width="25000">  | **Simple linear regression** models the relationship between one predictor variable and a continous numerical dependent variable by fitting a straight line. The model is based on a linear function equation.||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_27.jpg" width="25000">  | **Multiple linear regression** models the relationship between multiple predictor variable and a continous numerical dependent variable.||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_31.jpg" width="25000">  | <ul>Definitions:<li>**Loss function** is a function that defines the difference between the predicted target variables of a machine learning algorithm and the actual target values</li><li>**Error** is a difference between the predicted target variables of a machine learning algorithm and the actual target values for all target variables</li><li>**Learning** means finding the best model so that the error is minimal</il></ul>||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_32.jpg" width="25000">  | <ul>For the regression task, the most used loss function is **Mean squared error (MSE)**:<li>Mean squared deviation between the predicted and the actual target variables</li><li>Also in a form of **Root Mean Square Error (RMSE)** to return to the same units</li><li>Sensitive to outliers</il></ul>||

## Classification

| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_33.jpg" width="25000">  | **Classification** is a supervised learning technique to predict classes (e.g., smoking status (yes/no), cancer outcome (good/bad), response to treatment (postive/negative), etc).||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_34.jpg" width="25000">  | The classification task can be viewed as the task of finding a hyperplane that separates classes in a feature space. Learning here is finding the parameters of a hyperplane so that the error is minimal||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_35.jpg" width="25000">  | The classification task can be also adressed as the task of finding a rule that defines classes||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_36.jpg" width="25000">  | The classification task can be also adressed as the task of predicting the probability to belong to a class. Usually, a certain threshold used (e.g., p=0.5) to separate categories||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_47.jpg" width="25000">  | <ul>Measuring classification model performance:<li>Classes have actual values: e.g., belonging to postive and negative classes</li><li>For each sample, a model predicts those values: if a sample is predected to belong to a positive or negative class</li><li>If an actual positive class is predicted to be positive, these are **True Positive** (**TP**) predictions</li><li>If an actual negative class is predicted to be negative, these are **True Negative** (**TN**) predictions</li><li>If an actual negative class is (falsely) predicted to be positive, these are **False Positive** (**FP**) predictions</li><li>If an actual positive class is (falsely) predicted to be negative, these are **False Negative** (**FN**) predictions</li></ul>||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_48.jpg" width="25000">  | **Accuracy** is a proportion of **True** (TP + TN) predictions among all predictions (n). Limitation: might be misleading to measure the performance of the model with **unbalanced** classes (much larger amount of samples in one class than in the other)||
