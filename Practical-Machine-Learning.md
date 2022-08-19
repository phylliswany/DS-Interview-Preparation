# Practical Machine Learning

Course Website: https://www.coursera.org/learn/practical-machine-learning

Slides: https://github.com/bcaffo/courses/tree/master/08_PracticalMachineLearning

## What is prediction?

* question -> input data -> features -> algorithm -> parameters -> evaluation

## Relative importance of steps

* question > data > features > algorithms

## In sample and out of sample error

* In sample error < out of sample error due to overfitting: capturing both signal + noise

## Prediction study design

* Define your error rate -> Split data into training, testing, and validation -> On the training set pick features using cross-validation ->  On the training set pick prediction function using cross-validation -> If no validation Apply 1X to test set / If validation Apply to test set and refine and Apply 1X to validation

* A large sample size: 60% training + 20% test + 60% validation

* A medium sample size: 60% training + 40% testing

* A small sample size: cross validation

## Types of errors

* Mean squared error (MSE): $\frac{1}{n}\sum_i(Prediction_i-Truth_i)^2$

* Root mean squared error (RMSE): $\sqrt{\frac{1}{n}\sum_i(Prediction_i-Truth_i)^2}$

* True positive: correctly identified

* False positive: incorrectly identified

* Sensitivity: TP/(TP+FN)

* Specificity: TN/(TN+FP)

* Accuracy: (TP+TN)/(TP+FP+FN+TN)

* Precision: TP/(TP+FP)

* Recall: TP/(TP+FN)

* F score: $2\frac{Precision \times Recall}{Precision + Recall}$

## ROC curves

* True positive rate vs. False positive rate

* AUC: 0.5 is random guessing and 1 is perfect classifier

## Cross validation

* Used for: picking variables to include in a model, picking the type of prediction function to use, picking the parameters in the prediction function, and comparing different predictors

* Use the training set and split it into training/test sets: Randome subsampling, K-fold, and Leave one out without replacement

## Preprocessing with principal components analysis

* Combination with the "most information" possible: reduce nuber of predictors and noise (due to averaging)

* SVD: $X=UDV^T$ where $X$ is a matrix with each variable in a column and each observation in a row

* PCA: the principal components are equal to the right singular values if you first scale the variables

## Predicting with regression

* Easy to implement and interpret

* Often poor performance in nonlinear settings

## Predicting with trees

* Easy to interpret and Better performance in nonlinear settings

* Without pruning/cross-validation can lead to overfitting, Harder to estimate uncertainity, and Results may be variable

* Basic algorithm: Start with all variables in one group -> Find the variables/split that best separates the outcomes -> Divide the data into two groups ("leaves") on that split ("node") -> Within each split, find the best variable/split that separates the outcomes -> Continue until the groups are too small or sufficiently "pure"

* Measures of impurity: $\hat{p_{mk}}=\frac{1}{N_m}\sum_{x_i in Leaf m} 1(y_i=k)$

* Misclassification error: $1-\hat{p_{mk}};k(m)=most;common;k$

* Gini index: $1 - \sum_k \hat{p_{mk}}^2$

* Deviance/information gain: $-\sum_k \hat{p_{mk}} log_2\hat{p_{mk}}$

## Bagging

* Resample cases, recalculate predictions and Average or majority vote

* Similar bias, Reduced variance but More useful for non-linear functions

* An extension is random forests

## Random forests

* Bootstrap samples, At each split bootstrap variables and Grow multiple trees and vote

* Pros: Accuracy

* Cons: Speed, Interpretability, and Overfitting

## Boosting

* Start with a set of classifiers $h_1, ..., h_k$ and Create a classifier that combines classification functions: $f(x)=sgn(\sum_t \alpha_t h_t(x))$

* Goal is tto minimize error (on training set): Iteratively select one $h$ at each step, Calculate weights based on errors, and Upweight missed calssfications and select next $h$

* One large subclass is gradient boosting

## Model based prediction

* Our goal is to build parametric model for conditional distribution $P(Y=k|X=x)$: Apply Bayes theorem $P(Y=k|X=x) = \frac{f_k(x)\pi_k}{\sum_l f_l(x)\pi_l}$, Estimate the paramaters from the data, and Classifiy to the class with the highest value of $P(Y=k|X=x)$

* Prior probabilities $\pi_k$: set in advance

* A common choice for $f_k(x)$: a Gaussian distribution

* Discriminant function: $\delta_k(x) = x^T \Sigma^{-1} \mu_k - \frac{1}{2}\mu_k  \Sigma^{-1} \mu_k + log(\mu_k )$ and $\hat{Y}(x) = argmax_x \delta_k(x)$

* Naive Bayes: $P(Y=k|X_1, ... X_m) \propto \pi_k P(X_1, ... X_m|Y=k)$ and $P(X_1, ... X_m, Y=k) \approx \pi_k P(X_1|Y=k)P(X_2|Y=k)...P(X_m|Y=k)$
