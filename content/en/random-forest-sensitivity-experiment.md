---
lang: en
slug: random-forest-sensitivity-experiment
title: Sensitivity of the RF classifier - Experiment
date: 2017-04-25
tags: randomforest
---
<!-- more -->
![](http://oouh9u8nz.bkt.gdipper.com//random-forest-sensitivity-experiment.jpg)

Based on review papers we found RF can handle some complex situation and we don’t need to care about feature selection. But many features mean computing cost and incomplete image. That means we still need to make some decision.

To evaluate the sensitivity of RF models to parameterization, we selected two datasets form our research area. The first studies quality-control metrics in next-generation sequencing [6] and comprises 15 features (sequencing quality metrics) with 720 training samples and 576 validation samples, and thus reflects low p/n ratio studies. Each sample was classified as “good library” or “bad library” based on information external to the 15 features, and our models aimed to predict this binary response variable.

I’ve a had quite a few requests for code to do this. Unfortunately, most random forest libraries (including scikit-learn) don’t expose tree paths of predictions. The implementation for sklearn required a hacky patch for exposing the paths. Fortunately, since 0.17.dev, scikit-learn has two additions in the API that make this relatively straightforward: obtaining leaf node_ids for predictions, and storing all intermediate values in all nodes in decision trees, not only leaf nodes. Combining these, it is possible to extract the prediction paths for each individual prediction and decompose the predictions via inspecting the paths.