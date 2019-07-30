# Capstone Project 

## Link to the blog
[Starbucks turns to machine learning for attracting customers](https://medium.com/@ddk10/starbucks-turns-to-machine-learning-for-attracting-customers-fdfd580718ee)

## Problem
The problem is to build a model that predicts whether a customer will respond to an offer from Starbucks. The following is the strategy to solve this problem:

1. Combine the offer portfolio, customer profile, and transaction data. Each row of this combined dataset will describe an offer’s attributes, customer demographic data, and whether the offer was successful.

2. Assess the accuracy and F1-score of a naive model that assumes all offers were successful. This provides a baseline for evaluating the performance of models. Accuracy measures how well a model correctly predicts whether an offer is successful. However, if the percentage of successful or unsuccessful offers is very low, accuracy is not a good measure of model performance. For this situation, evaluating a models’ precision and recall provides better insight to its performance. We chose the F1-score metric because it is “a weighted average of the precision and recall metrics”.

3. Compare the performance of logistic regression, random forest, and gradient boosting models.

4. Fine-Tune parameters of the model that has the highest accuracy and F1-score.

## Installations
- Python
- Libraries: sklearn, pandas, numpy, matplotlib
- Jupyter notebook

## Results 

The problem was to build a model that predicts whether a customer will respond to an offer. The analysis suggests that a random forest model has the best training data accuracy and F1-score. The resulting random forest model has an training data accuracy of 0.768 and an F1-score of 0.760. The test data set accuracy of 0.734 and F1-score of 0.723 suggests that the random forest model did not overfit the training data.

“Feature importance” refers to a numerical value that describes a feature’s contribution to building a model that maximizes its evaluation metric. A random forest classifier is an example of a model that estimates feature importance during training. Analysis of the training data suggests that the top five features based on their importance are:

- Offer reward
- Offer duration
- Offer difficulty (how much money a customer must spend to complete an offer)
- Customer income

Whether a customer created an account on the Starbucks rewards mobile application in 2018
Since the top three features are associated with an customer offer, it may be possible to improve the performance of a random forest model by creating features that describe an offer’s success rate as a function of offer difficulty, duration, and reward. These additional features should provide a random forest classifier the opportunity to construct a better decision boundary that separates successful and unsuccessful customer offers.
