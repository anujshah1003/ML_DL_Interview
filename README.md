# ML_DL_Interview

# Questions & Answers
1. How can you convert a given distribution to distribution of zero mean and unit variance

Ans: Subtract the mean and divide by the standard deviation: (x-mean(x))/std(x)
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

2. How can you convert a given distribution to distribution of any desired mean and variance
Ans: First convert the given distribution to zero mean and unit variance, then multiply the new distribution with the desired standard deviation(std=square_root(variance)) and add the desired mean. 
```
eg. x = [10,20,30,40,50,60]
suppose you want a distribution of desired mean 2 and desired variance 9.
First convert to zero mean and unit variance
x_new = (x-np.mean(x))/np.std(x) # [-1.46385011, -0.87831007, -0.29277002,  0.29277002,  0.87831007,1.46385011]

Then,
d_mean = 2
d_var = 9
d_std = np.sqrt(d_var) = 3

y = d_std*x_new + d_mean # [-2.39155033, -0.6349302 ,  1.12168993,  2.87831007,  4.6349302 ,6.39155033]

np.mean(y) # 2
np.std(y) # 3
np.var(y) # 9
```
3. Given a 10 class classification how many nuerons/nodes you would use in the last layer?
Ans. 16 

4. can you use less number of neurons/nodes in the output?
Ans. Yes , by using some oter representation of the output class instead of decimal [0,1,2,...15]. for e.g binary representation. instead of 16 you can use 4 nodes
```
how to reprsent16 classes with 4 output nodes

2^4 = 16
class 0 : 0000
class 1 : 0001
class 2 : 0010
...
...
class 16 : 1111

```


# Resources & Questions

## Understanding Metrics like - Accuracy, ROC, AUC, Precision, Recall, Sensitivity, Specificty, True Positive Rate, False Positive Rate

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

