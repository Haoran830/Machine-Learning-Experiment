## Training and Testing Models
### Stats Refresher
Courses
- [Descriptive](https://www.udacity.com/course/intro-to-descriptive-statistics--ud827)
- [Inferential statistics](https://www.udacity.com/course/intro-to-inferential-statistics--ud201)

### Numpy and Pandas
Courses
- [Numpy and Pandas Tutorial](https://classroom.udacity.com/courses/ud725-nd/lessons/5454078888/concepts/54758106780923)
- [Scikit Learn Tutorial](https://classroom.udacity.com/courses/ud725-nd/lessons/5430830847/concepts/6a282140-f39d-4b43-8c91-539571a30fad)

### Loading data into Pandas
```python
import pandas
data = pandas.read_csv("file_name.csv")
```
### NumPy Arrays
```python
# extract column A
>> df['A']

# extract more columns
>> df[['B', 'D']]

# turn a DataFrame df into a NumPy array
>> numpy.array(df)
```

### Training models in sklearn
```python
# fit the classifier to the data (which we call X, y):
classifier.fit(X,y)

# Here are the main classifiers we define, together with the package we must import:

# Logistic Regression
from sklearn.linear_model import LogisticRegression
classifier = LogisticRegression()

# Neural Networks(note: This is only available on versions 0.18 or higher of scikit-learn)
from sklearn.neural_network import MLPClassifier
classifier = MLPClassifier()

# Decision Trees
from sklearn.tree import DecisionTreeClassifier
classifier = DecisionTreeClassifier()

# Support Vector Machines
from sklearn.svm import SVC
classifier = SVC()

# Example: Logistic Regression
from sklearn.linear_model import LogisticRegression
classifier = LogisticRegression()
classifier.fit(X,y)

```
### Tuning Parameters Manually

```python
>>> classifier = SVC(kernel = 'poly', degree = 2)
```

- **kernel** (string): 'linear', 'poly', 'rbf'.

- **degree** (integer): This is the degree of the polynomial kernel, if that's the kernel you picked (goes with poly kernel).

- **gamma** (float): The gamma parameter (goes with rbf kernel).

- **C** (float): The C parameter.

### Testing your models

Golden rule (never break)

- **Never use your testing data for training.**

