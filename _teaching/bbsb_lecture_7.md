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
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_16_2.jpg" width="25000">  | **Validation** includes spliting the data into **a training dataset** which will be used for training the model and **a test dataset** which will be used to measure the performance of a model on a previously not seen data||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_17_2.jpg" width="25000">  | However, if the data is split only once onto a training and a test set, there is a chance that a performance of a model appears better or worse by chance. **k-fold cross validation** approach splits a training data k times into k folds (often k = 5 (**5-fold cross validation**) but the actual value depends on the size of a data). k - 1 folds are used for training a model. The kth fold is used for a performance measurement. And then a separate test data is used to evaluate on a completely unseen data. Ideally, an unseen test data should come from the independent cohort or experiment||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_18_2.jpg" width="25000">  |<ul>**Leave-one-out** is a special case of k-fold cross validation approach where k = number of samples in a dataset. <li>Use a single sample as validation set</li><li>Remaining samples as training data</li><li>Repeat until every sample has been used exactly once as validation data.</li><li>It is used for a small dataset size</li><li>The approach is slow</li></ul>||

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
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_47.jpg" width="25000">  | <ul>Measuring classification model performance:<li>Classes have actual values: e.g., belonging to postive and negative classes</li><li>For each sample, a model predicts those values: if a sample is predected to belong to a positive or negative class</li><li>If an actual positive class is predicted to be positive, these are **True Positive** (**TP**) predictions</li><li>If an actual negative class is predicted to be negative, these are **True Negative** (**TN**) predictions</li><li>If an actual negative class is (falsely) predicted to be positive, these are **False Positive** (**FP**) predictions</li><li>If an actual positive class is (falsely) predicted to be negative, these are **False Negative** (**FN**) predictions</li></ul>|[Classification performance](https://www.evidentlyai.com/classification-metrics/accuracy-precision-recall)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_48.jpg" width="25000">  | **Accuracy** is a proportion of **True** (TP + TN) predictions among all predictions (n). Limitation: might be misleading to measure the performance of the model with **unbalanced** classes (much larger amount of samples in one class than in the other)||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_53.jpg" width="25000">  |**Precision** is a proportion of  samples that actually belong to a positive class among all samples predicted to belong to a positive class: TP/(TP+FP). Precision is an appropriate metric fo unbalanced classes. This metric should be maximized if FP predictions are needed to be minimized. E.g.: A positive class - a suspicious money transaction. FP prediction -  to test a valid credit card (a sample belonging to a negative class) and block it because it was predicted to be suspicious (falsely predicted to be positive)||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_54.jpg" width="25000">  |**Recall** (also **sensitivity, true positive rate**) is a proportion of samples predicted to belong to a positive class among all samples that actually belong to a positive class: TP/(TP+FN). This metric should be maximized if FN predictions are needed to be minimized. E.g.: A positive class - a highly contagious disease. FN prediction -  to test a person with a disease (a sample belonging to a positive class) and decide that the person is healthy (falsely predicted to be negative)||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_57.jpg" width="25000">  |**Specificity** is a proportion of samples predicted to belong to a negative class among all samples that actually belong to a negative class: TN/(FP+TN). This metric should be maximized if FP predictions are needed to be minimized. E.g.: A positive class - a suspicious money transaction. FP prediction -  to test a valid credit card (a sample belonging to a negative class) and block it because it was predicted to be suspicious (falsely predicted to be positive)||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_57.jpg" width="25000">  |**False positive rate** is a proportion of samples that falsely predicted to be positive among all samples that actually belong to a negative class: FP/(FP+TN). FPR = 1 - Specificity||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-7_75.jpg" width="25000">  |**ROC (Receiver Operating Characteristic) Curve** plots recall (true positive rate) and false positive rate at each probability threshold. **PR (Precision/Recall) Curve** plots precision and recall (true positive rate) at each probability threshold. **AUC (Area Under the Curve)** is a metric of the model performance between 0 (poor performance) and 1 (ideal performance).||

## Machine learning concerns

| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-8_6.jpg" width="25000">  |Using too many features for the model might lead to **overfitting**: an unwanted behaviour of a model which fits the training data too closely and fails to do accurate predictions on the test data.||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-8_11.jpg" width="25000">  |<ul>Feature selection approaches:<li>Dimensionality reduction</li><li>Based on domain knowledge</li><li>Based on relation with class label: choose features that is associated with an output data</li><li>Regularization: penalizing too high model coefficients or weights</li></ul>|[Example based on a domain knowledge](https://pubmed.ncbi.nlm.nih.gov/27397505/)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-8_12.jpg" width="25000">  |<ul>Dimensionality reduction (intuition)<li>Project high-dimensional data into lower dimensions that capture the most variance</li><li>The first component captures the most dominating signal in the data</li><li>More similar points are closer to each other</li></ul>||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-8_20.jpg" width="25000">  |**Data leakage** occurs when a model unintentionally uses information that would not be available during real-world predictions.|[More data leakage examples](https://www.kaggle.com/code/hmdprs/exercise-data-leakage/notebook)|
