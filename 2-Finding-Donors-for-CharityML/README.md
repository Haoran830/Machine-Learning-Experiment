
# Project: Finding Donors for CharityML
*Supervised Learning*

## Summary
### Main
[finding_donors.ipynb](finding_donors.ipynb)([html](others/finding_donors.html))

### Content
- Preprocess data
  - Transform skewed continuous features
  - Normalize numerical features
  - One-hot encode categorical variables
  - Shuffle and split data
- Evaluate models
  - ![1-Evaluate-models.png](others\images\1-Evaluate-models.png)
- Optimize the model using  grid search (GridSearchCV)
  - |     Metric     | Unoptimized Model | Optimized Model |
    | :------------: | :---------------: | :-------------: |
    | Accuracy Score |      0.8431       |     0.8573      |
    | F-score        |      0.6842       |     0.7242      |
- Observe feature relevance
  - ![2-Observe-feature-relevance.png](others\images\2-Observe-feature-relevance.png)
- Evaluate models with and without feature selection
  - |     Metric     |No Feature Selection|Feature Selection|
    | :------------: | :----------------: | :-------------: |
    | Accuracy Score |       0.8573       |     0.8269      |
    | F-score        |       0.7242       |     0.6528      |

## [Project Information](others/project_description.md)
### Install
This project requires **Python 2.7** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)

You will also need to have software installed to run and execute an [iPython Notebook](http://ipython.org/notebook.html)

### Run
In a terminal or command window, navigate to the top-level project  directory (that contains this README) and run the following commands.  This will open the Jupyter Notebook and project file in your browser. 
```bash
ipython notebook finding_donors.ipynb
```

### Data
The modified census dataset consists of approximately 32,000 data points, with each datapoint having 13 features. This dataset is a modified version of the dataset published in the paper *"Scaling Up the Accuracy of Naive-Bayes Classifiers: a Decision-Tree Hybrid",* by Ron Kohavi. You may find this paper [online](https://www.aaai.org/Papers/KDD/1996/KDD96-033.pdf), with the original dataset hosted on [UCI](https://archive.ics.uci.edu/ml/datasets/Census+Income).

**Features**
- `age`: Age
- `workclass`: Working Class (Private, Self-emp-not-inc, Self-emp-inc, Federal-gov, Local-gov, State-gov, Without-pay, Never-worked)
- `education_level`: Level of Education (Bachelors, Some-college, 11th, HS-grad, Prof-school, Assoc-acdm, Assoc-voc, 9th, 7th-8th, 12th, Masters, 1st-4th, 10th, Doctorate, 5th-6th, Preschool)
- `education-num`: Number of educational years completed
- `marital-status`: Marital status (Married-civ-spouse, Divorced, Never-married, Separated, Widowed, Married-spouse-absent, Married-AF-spouse)
- `occupation`: Work Occupation (Tech-support, Craft-repair, Other-service, Sales, Exec-managerial, Prof-specialty, Handlers-cleaners, Machine-op-inspct, Adm-clerical, Farming-fishing, Transport-moving, Priv-house-serv, Protective-serv, Armed-Forces)
- `relationship`: Relationship Status (Wife, Own-child, Husband, Not-in-family, Other-relative, Unmarried)
- `race`: Race (White, Asian-Pac-Islander, Amer-Indian-Eskimo, Other, Black)
- `sex`: Sex (Female, Male)
- `capital-gain`: Monetary Capital Gains
- `capital-loss`: Monetary Capital Losses
- `hours-per-week`: Average Hours Per Week Worked
- `native-country`: Native Country (United-States, Cambodia, England, Puerto-Rico, Canada, Germany, Outlying-US(Guam-USVI-etc), India, Japan, Greece, South, China, Cuba, Iran, Honduras, Philippines, Italy, Poland, Jamaica, Vietnam, Mexico, Portugal, Ireland, France, Dominican-Republic, Laos, Ecuador, Taiwan, Haiti, Columbia, Hungary, Guatemala, Nicaragua, Scotland, Thailand, Yugoslavia, El-Salvador, Trinadad&Tobago, Peru, Hong, Holand-Netherlands)

**Target Variable**
- `income`: Income Class (<=50K, >50K)