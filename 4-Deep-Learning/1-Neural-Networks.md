# 1. Neural Networks
## Log-loss Error Function - 14
- many times local minimum will give us a pretty good solution to a problem
- Error function can not be discrete, it should be continuous.
- The error function should be continuous
- The error function should be differentiable (Why?)
- The error function should not be normalized (Why?)

## Discrete vs Continuous - 15
|Discrete | Continuous|
|-----|----|
|Step function | Sigmoid Function|
|Yes / No | 80% Like / 16% Like|

## Softmax - 16
Classification Problem - problem has 3 or more classes
![image](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/4-Deep-Learning/images/1-1.png)

```python
import numpy as np

def softmax(L):
    expL = np.exp(L)
    sumExpL = sum(expL)
    result = []
    for exp in expL:
        result.append(exp/sumExpL)
    return result
```

## One-Hot Encoding - 17
| Original |      | Wrong |
| :------: | :--: | :---: |
|   Duck   |  ->  |   1   |
|  Beaver  |  ->  |   2   |
|   Duck   |  ->  |   1   |
|  Walrus  |  ->  |   3   |
|  Beaver  |  ->  |   2   |
It would not work because it would assume dependencies between the classes that we can't have.

The right way is:
![image](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/4-Deep-Learning/images/1-2.png)

## Cross Entropy - 20
Cross-entropy loss, or log loss, measures the performance of a classification model whose output is a probability value between 0 and 1. Cross-entropy loss increases as the predicted probability diverges from the actual label. So predicting a probability of .012 when the actual observation label is 1 would be bad and result in a high loss value. A perfect model would have a log loss of 0.
![image](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/4-Deep-Learning/images/1-3.png)

Multi-Class Cross-Entropy 
![image](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/4-Deep-Learning/images/1-4.png)

## Logistic Regression Algorithm - 23
1. Take your data
2. Pick a random model
3. Calculate the error(Error Function)
4. Minimize the error, and obtain a better model(Gradient Descent)
5. Enjoy!
### Error Function
![image](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/4-Deep-Learning/images/1-5.png)
### Gradient Descent 
*To minimize the error function*
##### Procedure
![image](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/4-Deep-Learning/images/1-6.png)
##### Math
After [calculation](https://classroom.udacity.com/nanodegrees/nd009t/parts/0ac87c1d-350a-417b-93c8-392dbf9cb8c2/modules/8c602bd6-1bde-454e-80d3-0ed8476baf10/lessons/d00ecaa9-56de-405d-ba6e-530b44a59836/concepts/0d92455b-2fa0-4eb8-ae5d-07c7834b8a56) we can get
$$
\frac{\partial }{\partial b} E = -(y - \hat{y})
$$
which means
$$
\triangledown E = -(y - \hat{y})(x_{1}, \cdots, x_{n}, 1)
$$
Thus,
$$
w_{i}^{′} \leftarrow w_{i} + \alpha(y-\hat{y})x_{i}
$$
$$
b^{′} \leftarrow b + \alpha(y-\hat{y})
$$
Then, the procedure becomes
![image](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/4-Deep-Learning/images/1-7.png)
