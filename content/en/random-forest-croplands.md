---
lang: en
slug: random-forest-croplands
title: Random forest classifier in croplands mapping
date: 2017-04-25
tags: EarthEngine
---
<!-- more -->
![](http://oouh9u8nz.bkt.gdipper.com//random-forest-croplands.jpg)


# Sensitivity of the RF classifier to training samples and data dimensions
The samples used to train the supervised classifiers need to fulfil a number of requirements: 

1. training and validation data must be statistically independent, 
2. training samples must be class balanced, 
3. training samples must be representative of the target classes, and 
4. the training sample needs to be large enough to accommodate the increasing number of data dimensions (to mitigate the Hughes phenomenon).

It is important to evaluate the sensitivity of RF classification to sampling design and imbalanced training samples.

RF classification may be attractive when a small sample size is used in combination with high dimensional data inputs.

The classification accuracies obtained using correlated variables were similar to those obtained using uncorrelated variables. 



Outputs from random forest provide unique complements to traditional accuracy assessment, including: (1) cross-validation, using the out-of-bag sample of training data to evaluate relative accuracy of each model prior to a formal accuracy assessment; (2) classification confidence, or probability, calculated by the number of times a given class was designated as the final class out of the total number of trees, with a resulting value range of 0–1; (3) mean decrease in accuracy, calculated per input data layer, giving insight to how influential a layer was on the overall accuracy; and (4) Gini index, which aids in evaluating the influence of input layers on the structure of the decision trees.