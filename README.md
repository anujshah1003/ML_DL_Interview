# ML_DL_Interview

# Questions & Answers
1. How can you convert a given distribution to distribution of zero mean and unit variance

Ans: Subtract the mean and divide by the standard deviation.
```
eg x = [10,20,30,40,50,60]

mean = np.mean(x) # 35
std = np.std(x) # 17.07825127659933
# transform the distribution to zero mean 
x_new = x - mean # [-25., -15.,  -5.,   5.,  15.,  25.]

# transform it to unit variance
x_new = x_new/std # [-1.46385011, -0.87831007, -0.29277002,  0.29277002,  0.87831007,1.46385011]

# now your new distribution has zero mean and unit variance
np.mean(x_new)  # 0
np.std(x_new)   # 1
np.var(x_new)   # 1
```


# Resources & Questions

## Understnding Metrics like - Accuracy, ROC, AUC, Precision, Recall, Sensitivity, Specificty, True Positive Rate, False Positive Rate

What is Precision and Recall?

What is ROC Curve?

What is AUC?

What is the best value for ROC curve?

What is Precision-Recall Curve?

What is the best value for Precision-Recall Curve?

What is Senitivity and Specificity?

When to use ROC curve and when to use precision-recall curve?

which is the better curve for interpreting model performance when you have imbalance dataset ROC or Precision-recall and why?

What is ACcuracy?

In case of imbalance dataset , does accuracy serve to be a better metric for model evaluation, if not why?

Links:
https://machinelearningmastery.com/roc-curves-and-precision-recall-curves-for-classification-in-python/

https://towardsdatascience.com/understanding-auc-roc-curve-68b2303cc9c5

https://towardsdatascience.com/receiver-operating-characteristic-curves-demystified-in-python-bd531a4364d0

http://www.navan.name/roc/

https://towardsdatascience.com/confused-by-the-confusion-matrix-e26d5e1d74eb

## Bagging And Boosting

What is Bagging?

What is Boosting?

Difference between bagging and boosting?

What is difference between bagging and random forest?

What are the various parameters to be tuned for Random Forest?

Can random forest be used for classification alone?

What is adaboost?

What is the stopping criterion for adaboost?

What is the disadvanatge of adaboost?

which is more robust when the data is noisy-random forest or adaboost and why?

Explain the workflow of Adaboost , how the data is weighted?

What is a weak learner? - Decision Stump(a tree with one decision node)

What is gardient Boosting?

What is XGB?

https://machinelearningmastery.com/boosting-and-adaboost-for-machine-learning/
https://towardsdatascience.com/the-ultimate-guide-to-adaboost-random-forests-and-xgboost-7f9327061c4f
https://machinelearningmastery.com/gentle-introduction-xgboost-applied-machine-learning/

