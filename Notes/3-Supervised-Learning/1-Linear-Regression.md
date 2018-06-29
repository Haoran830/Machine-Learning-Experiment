# 1. Linear-Regression
Linear regression is a very effective algorithm to nredict numerical data. 

## Fitting a Line Through Data 
### Moving a Line 
- Absolute Trick = Mean Absolute Error 
- Square Trick  = Mean Squared Error
![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/3-Supervised-Learning/images/1-1.png)
![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/3-Supervised-Learning/images/1-2.png)

## Mini-batch Gradient Descent 
[Gradient descent](https://en.wikipedia.org/wiki/Gradient_descent)

- Stochastic gradient descent
	- By applying the squared (or absolute) trick at every point in our data one by one, and repeating this process many times.
- Batch gradient descent
	- By applying the squared (or absolute) trick at every point in our data all at the same time, and repeating this process many times.
- **Mini-batch gradient descent (Best)**
	- Split your data into many small batches. Each batch, with roughly the same number of points. Then, use each batch to update your weights. 

## Absolute Error vs Squared Error
Most of time, squared error is better

## Linear Regression in scikit-learn 
```python
from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(x_values, y_values)

# The reason for predicting on an array like [127] and not just 127, is because you can have a model that makes a prediction using multiple features.
print(model.predict([ [127], [248] ]))
# [[ 438.94308857, 127.14839521]]
```
## Higher Dimensions 
![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/3-Supervised-Learning/images/1-3.png)

## Linear Regression Warnings 
Linear regression comes with a set of implicit assumptions and is not the best model for every situation. Here are a couple of issues that you should watch out for.

#### Linear Regression Works Best When the Data is Linear
Linear regression produces a straight line model from the training data. If the relationship in the training data is not really linear, you'll need to either make adjustments (transform your training data), add features (we'll come to this next) or use another kind of model.
![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/3-Supervised-Learning/images/1-4.png)
#### Linear Regression is Sensitive to Outliers
Linear regression tries to find a 'best fit' line among the training data. If your dataset has some outlying extreme values that don't fit a general pattern, they can have a surprisingly large effect.

![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/3-Supervised-Learning/images/1-5.png)

- In this first plot, the model fits the data pretty well.
- However, adding a few points that are outliers and don't fit the pattern really changes the way the model predicts. 
- In most circumstances, you'll want a model that fits most of the data most of the time, so watch out for outliers!


## Polynomial Regression 
![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/3-Supervised-Learning/images/1-6.png)

## Regularization 
Balance accuracy and performance
![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/3-Supervised-Learning/images/1-7.png)

![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/3-Supervised-Learning/images/1-8.png)

| Ll Regularization | L2 Regularization |
| ---- | ---- |
| Computationally Inefficient(unless data is sparse) | Computationally Efficient|
| Sparse Outputs | Non-Sparse Outputs |
| Feature Selection | No Feature Selection |

