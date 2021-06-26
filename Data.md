# Outliers
1. https://medium.com/analytics-vidhya/how-to-remove-outliers-for-machine-learning-24620c4657e8
2. https://www.kdnuggets.com/2018/08/make-machine-learning-models-robust-outliers.html
3. https://www.kdnuggets.com/2017/01/3-methods-deal-outliers.html

# Q & A
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
