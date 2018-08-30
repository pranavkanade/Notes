# Naive Bayes

* __According to Wiki :__ Naive Bayes is a simple technique for constructing classifiers; Models that assigns labels to problem instances.
* These problems are represened as vectors of feature values __(exactly similar to mathematical vctors)__.
* And the class labels are drawn from some _finite set_.

## Principle

* Assume that the value of a particular feature is __independent__ of the value of any other feature, given the class variable.

    __e.g. :__ It finds the probability that given fruit is say an apple, regardless of any possible correlation between the _color_, _roundness_ and _diameter_ features.

* A naive Bayes classifier considers each of these features to contribute independently to the probability of the classification.
* According to the study in 2006 showed that NBC is outperformed by other approaches:
  * __boosted trees__
  * __random forest__
* An advantage of NBC is that it only requires a small number of training data to estimate the parameters necessary for classification.

## None Sense

* For some types of probalility models, NB classifiers can be trained very efficiently in a __supervised learning__ setting.
* In many practical applications, parameter estimation for NB models uses the method of [maximum likelihood](https://en.wikipedia.org/wiki/Maximum_likelihood) __=__ one can work with the NB model without accepting Bayesian probability or using any Bayesian methods.

* [wiki](https://en.wikipedia.org/wiki/Naive_Bayes_classifier)

