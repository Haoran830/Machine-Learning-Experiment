# 3. Model Selection

## Types of Errors 
![Types of Errors](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/2-Model-Evaluation-and-Validation%20/images/3-1.png)

## Model Complexiy Graph 
![Model Complexiy Graph](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/2-Model-Evaluation-and-Validation%20/images/3-2.png)

## Cross Validation
However, it breaks the golden rule(**Never use your testing data for training**).
Then,
![Cross Validation](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/2-Model-Evaluation-and-Validation%20/images/3-3.png)

## K-Fold Cross Validation
Train model K times, each time use randomly choosed points as testing seting and remaining points as training set. Then, average the results and get the final model.
![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/2-Model-Evaluation-and-Validation%20/images/3-4.png)

## Leaming Curves 
Detecting Overfitting and Underfitting
![](https://raw.githubusercontent.com/Haoran830/Machine-Learning/master/2-Model-Evaluation-and-Validation%20/images/3-5.png)