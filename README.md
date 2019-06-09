PIMA
====

Observations:
------------

* 'BloodPressure', 'SkinThickness', 'BMI', 'Insulin', 'Glucose' - have zeros which are actually missing data
* 'Glucose', 'SkinThickness' - look like poisson distribution
* 'DiabetesPedigreeFunction' - look like exponential
* 'Insulin' should be skipped. 50% values are 0

Methods:
-------

* replace missing values with generated radom values from hist
* poisson distribution can be reduced to gaussian by applying [Anscombe transform](https://en.wikipedia.org/wiki/Anscombe_transform)
* exponential distribution transformed to gaussian by applying inverse distribution integral

Ways to improve:
---------------

* no idea how to deal with 'age' and 'pregnancies'. they are discrete + pregrnancies are sex dependent (so too many zeros)
* might work for pregnancies to fit non-zero values and guess zeros for women => infer sex
