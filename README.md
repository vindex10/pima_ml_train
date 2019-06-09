PIMA
====

Observations:
------------

* 'BloodPressure', 'SkinThickness', 'BMI', 'Insulin', 'Glucose' - have zeros which are actually missing data
* 'Glucose', 'SkinThickness' - look like poisson distribution
* 'Insulin', 'DiabetesPedigreeFunction' - look like exponential

Methods:
-------

* replace missing values with median 
* poisson distribution can be reduced to gaussian by applying [Anscombe transform](https://en.wikipedia.org/wiki/Anscombe_transform)
* exponential distribution I normalize with `log`. We are more interested in differences between low values than large.

Ways to improve:
---------------

* [Standardize exponential](https://stats.stackexchange.com/questions/154396/translate-exponential-distribution-into-normal-distribution)
* [Standardize exponential 2](https://datascience.stackexchange.com/questions/18933/convert-exponential-to-normal-distribution)
* Missing values: better would be to guess distribution and generate random values relying on it 
