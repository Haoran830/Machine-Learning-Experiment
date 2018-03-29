# 3. Decision Trees
Decision trees are a structure for decision-making where each decision 
leads to a set of consequences or additional decisions. 
## Entropy 
![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/3-Supervised-Learning/images/3-1.png)

### Entropy Formula
![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/3-Supervised-Learning/images/3-2.png)

### Information Gain 
![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/3-Supervised-Learning/images/3-3.png)

## Random Forests
![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/3-Supervised-Learning/images/3-6.png)

1. Pick some of the columns randomly. Build a Decision Tree in those columns. 
2. Pick some other columns randomly and build a Decision Tree in those
3. Do it again.
4. At last, just let the trees vote. When we have a new data point, say this person over here, we just let all the trees make a prediction and pick the one that appears the most.

## Hyperparameters for Decision Trees

These are some of the most important hyperparameters used in decision trees:

#### 1. Maximum Depth
The maximum depth of a decision tree is simply the largest length between the root to a leaf. A tree of maximum length k k k can have at most 2k 2^k 2k leaves.

![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/3-Supervised-Learning/images/3-4.png)

- Large depth very often causes overfitting, since a tree that is too deep, can memorize the data. 
- Small depth can result in a very simple model, which may cause underfitting.

#### 2. Minimum number of samples per leaf
When splitting a node, one could run into the problem of having 99 samples in one of them, and 1 on the other. This will not take us too far in our process, and would be a waste of resources and time. If we want to avoid this, we can set a minimum for the number of samples we allow on each leaf.

This number can be specified as an integer, or as a float. If it's an integer, it's the number of minimum samples in the leaf. If it's a float, it'll be considered as the minimum percentage of samples on each leaf. For example, 0.1, or 10%, implies that a cut will not be allowed if in one of the leaves there is less than 10% of the samples on that node.

![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/3-Supervised-Learning/images/3-5.png)

- Small minimum samples per leaf may result in leaves with very few samples, which results in the model memorizing the data, or in other words, overfitting. 
- Large minimum samples may result in the tree not having enough flexibility to get built, and may result in underfitting.

#### 3. Minimum number of samples per split
This is the same as the minimum number of samples per leaf, but applied on any split of a node.

#### 4. Maximum number of features
Oftentimes, we will have too many features to build a tree. If this is the case, in every split, we have to check the entire dataset on each of the features. This can be very expensive. A solution for this is to limit the number of features that one looks for in each split. If this number is large enough, we're very likely to find a good feature among the ones we look for (although maybe not the perfect one). However, if it's not as large as the number of features, it will speed up our calculations significantly.

Maximizing Information Gain 

Hyperparameters 
Decision Trees in sklearn 
Titanic Survival Model with Decisio„. 
[Solution] Titanic Survival Model 





