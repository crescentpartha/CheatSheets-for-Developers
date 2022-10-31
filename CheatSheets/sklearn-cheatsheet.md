---
title: Scikit-learn CheatSheet
description: The most important and useful methods and functions of scikit-learn are given here.
created: 2022-10-31
---

## Table of Contents

- [Scikit-learn CheatSheet for Developers](#scikit-learn-cheatsheet-for-developers)
  - [Training, Validation, and Test Sets](#training-validation-and-test-sets)
  - [Preprocessing](#preprocessing)
  - [Modeling](#modeling)
    - [Supervised Learning](#supervised-learning)
      - [`Linear Regression`](#linear-regression)
      - [`Logistic Regression`](#logistic-regression)
      - [`Support Vector Machines`](#support-vector-machines)
      - [`Naive Bayes`](#naive-bayes)
      - [`KNN`](#knn)
      - [`Decision Tree`](#decision-tree)
      - [`Gradient Boosting`](#gradient-boosting)
      - [`Random Forest` (Bagged Decision Trees)](#random-forest-bagged-decision-trees)
    - [Unsupervised Learning](#unsupervised-learning)
      - [`PCA`](#pca)
      - [`k-Means Clustering`](#k-means-clustering)
  - [Additional Notes](#additional-notes)
    - [Decision Tree Boosting](#decision-tree-boosting)
    - [Cross Validation and Grid Search](#cross-validation-and-grid-search)

# Scikit-learn CheatSheet for Developers

## Training, Validation, and Test Sets

> [train_test_split](http://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html) - [scikit-learn.org](https://scikit-learn.org/stable/)

```python
from sklearn.model_selection import train_test_split
x_trn, x_other, y_trn, y_other = train_test_split(x, y, train_size=0.7, random_state=0)
x_val, x_tst, y_val, y_tst = train_test_split(x_other, y_other, test_size=0.33, random_state=1)
```

**[🔼Back to Top](#table-of-contents)**

## Preprocessing

> For many machine learning models, various preprocessing techniques not only help improve efficiency, but often are important for ensuring meaningful results.

- [StandardScaler](http://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html) (aka Z-score)
- [Normalizer](http://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.Normalizer.html) (vector normalization)
- [Binarizer](http://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.Binarizer.html)
The typical process is:
  1. Choose appropriate preprocessing method and import it
  2. Construct a rescale object by fitting the chosen method to the training set only!
  3. Transform your training, validation, and test sets using constructed rescale object.

```python
# Example:  Standarization / Z Scoring
#   -- the procedure is the same for Normalizer and Binarizer
from sklearn.preprocessing import StandardScaler
rescale = StandardScalar.fit(x_trn)
xx_trn = rescale.transform(x_trn)
xx_val = rescale.transform(x_val)
xx_tst = rescale.transform(x_tst)
```

**[🔼Back to Top](#table-of-contents)**

## Modeling

> Scikit-Learn makes modeling really easy. The recipe is:

1. Construct
2. Fit
3. Predict
4. Evaluate

In the subsections that follow, we cover the first 3 steps. Model evaluation is covered in the next section.

**[🔼Back to Top](#table-of-contents)**

### Supervised Learning

#### `Linear Regression`

> [Function Documentation](http://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)

```python
from skearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(xx_trn, y_tr)
y_pred = model.predict(xx_val)
```

**[🔼Back to Top](#table-of-contents)**

#### `Logistic Regression`

> [Function Documentation](http://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)

```python
from skearn.linear_model import LogisticRegression
model = LogisticRegression()
model.fit(xx_trn, y_tr)
y_pred = model.predict(xx_val)
```

**[🔼Back to Top](#table-of-contents)**

#### `Support Vector Machines`

> [Documentation](http://scikit-learn.org/stable/modules/svm.html)

```python
from skearn.svm import SVC
model = SVC(kernel='linear') # other kernels: polynomial, rbf, sigmoid
model.fit(xx_trn, y_tr)
y_pred = model.predict(xx_val)
```

**[🔼Back to Top](#table-of-contents)**

#### `Naive Bayes`

```python
from skearn.naive_bayes import GaussianNB
model = GaussianNB()
model.fit(xx_trn, y_tr)
y_pred = model.predict(xx_val)
```

**[🔼Back to Top](#table-of-contents)**

#### `KNN`

```python
from skearn.neighbors import KNeighborsClassifier
model = KNeighborsClassifier(n_neighbors=3)
model.fit(xx_trn, y_tr)
y_pred = model.predict(xx_val)
```

**[🔼Back to Top](#table-of-contents)**

#### `Decision Tree`

```python
from skearn.tree import DecisionTreeClassifier
model = DecisionTreeClassifier(criterion='entropy', max_depth=10, random_state=0)
model.fit(x_trn, y_tr)  # Vars do not have to be normalized/standardized for DTs!
y_pred = model.predict(x_val)
```

**[🔼Back to Top](#table-of-contents)**

#### `Gradient Boosting`

```python
from skearn.ensemble import GradientBoostinClassifier
model = GradientBoostinClassifier(max_depth=5, n_estimators=1000, 
  subsample=0.5, random_state=0, learning_rate=0.001)
model.fit(x_trn, y_tr)  # Vars do not have to be normalized/standardized for DTs!
y_pred = model.predict(x_val)
```

**[🔼Back to Top](#table-of-contents)**

#### `Random Forest` (Bagged Decision Trees)

```python
from skearn.ensemble import RandomForestClassifier
model = RandomForestClassifier(n_estimators=1000, criterion='entropy', 
   n_jobs=4, max_depth=10)
model.fit(x_trn, y_tr)  # Vars do not have to be normalized/standardized for DTs!
y_pred = model.predict(x_val)
```

**[🔼Back to Top](#table-of-contents)**

### Unsupervised Learning

#### `PCA`

```python
from skearn.decomposition import PCA
model = PCA(n_components=0.95)
model.fit(xx_trn, y_tr)
#y_pred = model.predict(xx_val)
```

**[🔼Back to Top](#table-of-contents)**

#### `k-Means Clustering`

```python
from skearn.cluster import KMeans
model = KMeans(n_clusters=3, random_state=1)
model.fit(xx_trn, y_tr)
#y_pred = model.predict(xx_val)
```

**[🔼Back to Top](#table-of-contents)**

---------------------------------------------

## Additional Notes

### Decision Tree Boosting

> This is basically what is happening...

```python
from skearn.tree import DecisionTreeClassifier
model = DecisionTreeClassifier(max_depth=2, random_state=0)
N_estimators = 3
for i in range(N_estimators):
  model.fit(x_trn, y_trn)  
  y_res = y_trn - model.predict(x_trn)
y_pred = y_res
```

**[🔼Back to Top](#table-of-contents)**

### Cross Validation and Grid Search

- [StratifiedKFold](http://scikit-learn.org/stable/modules/generated/sklearn.model_selection.StratifiedKFold.html)
- [GridSearchCV](http://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html)

```python
#from sklearn.cross_validation import StratifiedKFold
from sklearn.grid_search import GridSearchCV
###
#skf = StratifiedKFold(n_splits=2)
model_type = GradientBoostingClassifier(n_estimators=500, learning_rate=.01)
params = {"max_depth": [3, 5, 7]}
###
model = GridSearchCV(model_type, param_grid=params, verbose=2)
model.fit(x_trn, y_trn)
```

**[🔼Back to Top](#table-of-contents)**
