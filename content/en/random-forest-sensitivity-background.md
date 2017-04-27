---
lang: en
slug: random-forest-sensitivity-background
title: Sensitivity of the RF classifier - Background
date: 2017-04-25
tags: randomforest
---
<!-- more -->
![](http://oouh9u8nz.bkt.gdipper.com//random-forest-sensitivity-background.jpg)

The [Random Forest (RF)](http://en.wikipedia.org/wiki/Random_forest) algorithm for supervised machine learning is an ensemble learning method widely used in science and many other fields. Its popularity has been increasing, but relatively few studies address the parameter selection process. 

Remotely sensed data rarely have normal distributions. Supervised parametric classifiers such as Maximum Likelihood Classification (MLC) deliver excellent results when dealing with unimodal data. CART, SVM and ANN classifiers don’t make any assumptions regarding frequency distribution and have therefore become increasingly popular for classifying.

In the last years the attention of the remote sensing community has turned to ensemble classifiers ^[Miao, X., Heaton, J.S., Zheng, S., Charlet, D.A., Liu, H., 2012. Applying tree-based ensemble algorithms to the classification of ecological zones using multi- temporal multi-source remote-sensing data. Int. J. Remote Sens. 33, 1823–1849.]. These classifiers can be based on an individual supervised classifier or on a number of different supervised classifiers that are trained using bagging or boosting approaches, or variations of these approaches. 

 In the bagging/bootstrap aggregation approach each classifier in the ensemble is trained on a random subset of a training samples set, whereas in the boosting approach the ensemble classifiers are trained iteratively using all of the training samples, increasing the weightings for the incorrectly classified samples during the training procedure. Previous work has shown that using boosting and bagging ensemble methods achieved greater accuracy than using single classifiers such as decision tree classifiers, as well as being more stable and robust to noise in the training data.

The RandomForestClassifier is trained using bootstrap aggregation, where each new tree is fit from a bootstrap sample of the training observations z_i = (x_i, y_i). The out-of-bag (OOB) error is the average error for each z_i calculated using predictions from the trees that do not contain z_i in their respective bootstrap sample^[T. Hastie, R. Tibshirani and J. Friedman, “Elements of Statistical Learning Ed. 2”, p592-593, Springer, 2009.]. RF classification may be attractive when a small sample size is used in combination with high dimensional data inputs.

Two parameters need to be set in order to produce the forest trees: the number of decision trees to be generated (Ntree) and the number of variables to be selected and tested for the best split when growing the trees (Mtry). 


^[[Use Random Forest: Testing 179 Classifiers on 121 Datasets](http://machinelearningmastery.com/use-random-forest-testing-179-classifiers-121-datasets/)]

# Training samples
The samples used to train the supervised classifiers need to fulfill a number of requirements: 

1. training and validation data must be statistically independent, 
1. training samples must be class balanced, 
1. training samples must be representative of the target classes, and 
1. the training sample needs to be large enough to accommodate the increasing number of data dimensions (to mitigate the Hughes phenomenon).

So it is important to evaluate the sensitivity of RF classification to sampling design and imbalanced training samples.



Outputs from random forest provide unique complements to traditional accuracy assessment, including: 

1. cross-validation, using the out-of-bag sample of training data to evaluate relative accuracy of each model prior to a formal accuracy assessment; 
2. classification confidence, or probability, calculated by the number of times a given class was designated as the final class out of the total number of trees, with a resulting value range of 0–1; 
3. mean decrease in accuracy, calculated per input data layer, giving insight to how influential a layer was on the overall accuracy; and
4. Gini index, which aids in evaluating the influence of input layers on the structure of the decision trees.