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
