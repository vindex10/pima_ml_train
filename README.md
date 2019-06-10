PIMA
====

Observations:
------------

* 'BloodPressure', 'SkinThickness', 'BMI', 'Insulin', 'Glucose' - have zeros which are actually missing data
* 'Glucose', 'SkinThickness' - look like poisson distribution
* 'DiabetesPedigreeFunction', 'Age'  - look like exponential
* 'Insulin' should be skipped. 50% values are 0
* all patients are women. [Kaggle dataset description](https://www.kaggle.com/uciml/pima-indians-diabetes-database)

Methods:
-------

* replace missing values with generated radom values from hist
* poisson distribution can be reduced to gaussian by applying [Anscombe transform](https://en.wikipedia.org/wiki/Anscombe_transform)
* exponential distribution transformed to gaussian by applying inverse distribution integral

Ways to improve:
---------------

* no idea how to deal with exponentially distributed data. any normalization?
* analysis of data. pick more ideas from [here](https://easydsrp.com/posts/2018-11-06-diabetes-among-the-pima-indians-an-exploratory-analysis/)
