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
