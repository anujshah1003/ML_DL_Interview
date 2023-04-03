# ML_DL_Interview

Read the blogs below to set yourself up for a good preparartion

## [Emma Ding - The Ultimate Guide to Acing Machine Learning Interviews for Data Scientists and Machine Learning Engineers](https://pub.towardsai.net/4-types-of-machine-learning-interview-questions-for-data-scientists-and-machine-learning-engineers-b8135805ce1b)

## [Data Related](https://github.com/anujshah1003/ML_DL_Interview/blob/master/Data.md)

# Questions & Answers

3. Given a 16 class classification how many nuerons/nodes you would use in the last layer?

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
5. Given a multi-class classification problem, what activation function you use at output layer?
Ans Softmax.

6. If it is a multi-label classifiation problem , then what activation function you will use?
Ans sigmoid

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

## Why you get NaNs during training and how to avoid
Ref: https://neptune.ai/blog/keras-loss-functions
![image](https://user-images.githubusercontent.com/20814689/229438498-eb5b5a05-7357-46ac-8b13-fe5c3ca8ccdb.png)


