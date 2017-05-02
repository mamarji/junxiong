---
lang: en
slug: petapixel-scale-analysis
title: What is Petapixel Scale Analysis?
date:  2016-10-04
tags: earthengine
---
<!-- more -->
![](http://oouh9u8nz.bkt.gdipper.com//petapixel-scale-analysis.jpg)

Google announces availability of cost-free Landsat and Sentinel-2 satellite imagery on the Google Cloud, the full range of public datasets can be find [here](http://cloud.google.com/public-datasets/). Remote sensed imagery, used to be expensive in all aspect to obtain, process them, now is free. With dozens of public satellites in orbit and many more scheduled over the next decade, the size and complexity of geospatial imagery continues to grow. However, it has become increasingly difficult to manage this flood of data and use it to gain valuable insights. 

I put some notes here for tracking, will keep updates: 

###  Google Earth Engine
[Google Earth Engine](https://earthengine.google.com/) is a cloud-based platform with following components:

1. Vast catalog of public data, free access if you have an earthengine account;
1. Web-based geospatial visualization tools: very impressive;
1. Web scripting interface as a testbed and fast prototype-builder;
1. Possibilities to process these dataset through [Google Compute Engine](https://cloud.google.com/compute/), which enable you more flexibility and freedom;
1. Integrated with [Google Cloud Machine Learning](https://cloud.google.com/products/machine-learning/) and other Google Cloud services.

### Descartes Labs
[Descartes Labs](http://www.descarteslabs.com/) combines machine learning and geospatial data to forecast global crop production. They don’t develop models but train existing ones using specialized algorithms to correlate historical inputs with historical outputs on the their own Descartes Platform, which could be a computing system with machine learning facilities. They also make [weekly forecasts](https://www.descarteslabs.com/forecast.html) available to the public.

### Spaceknow
[Spaceknow](https://spaceknow.com/) develops Urban Growth Index analyzes massive amounts of multispectral imagery in China. Using a TensorFlow-based deep learning framework capable of predicting semantic labels for multi-channel satellite imagery, Spaceknow determines the percentage of land categorized as urban-type for a specified geographic region. Furthermore, its China Satellite Manufacturing Index uses proprietary algorithms to analyze Landsat 7 and 8 imagery of over 6,000 industrial facilities across China, measuring levels of Chinese manufacturing activity.