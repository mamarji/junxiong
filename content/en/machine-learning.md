---
lang: en
slug: machine-learning
title: Apply deep Learning to remote sensing domain?
date: 2016-01-13
tags: earthengine
---
<!-- more -->
![](http://oouh9u8nz.bkt.gdipper.com//machine-learning.jpg)

Data analysis and machine learning have become an integrative part of the modern scientific methodology, offering automated procedures for the prediction of a phenomenon based on past observations, unraveling underlying patterns in data and providing insights about the problem. Yet, caution should avoid using machine learning as a black-box tool, but rather consider it as a methodology, with a rational thought process that is entirely dependent on the problem under study. In particular, the use of algorithms should ideally require a reasonable understanding of their mechanisms, properties and limitations, in order to better apprehend and interpret their results.

Deep learning is the ability of machine learning algorithms to acquire feature hierarchies from data and then persist those features within multiple non-linear layers which comprise the machine’s learning center, or neural network.

Two years ago, questions were mainly about what deep learning is, and how it might be applied to problems in science, engineering, and finance. Over the past year, however, the climate of interest has changed from a curiosity about what deep learning is, and into a focus on acquiring hardware and software in order to apply deep learning frameworks to specific problems across a wide range of disciplines.

Fairly recently, a major framework was released as open-source: Google’s TensorFlow. IBM is also planning to release its own deep learning software, in cooperation with its openPOWER partner NVIDIA. IBM’s framework, however, will be not just be a software framework, but will be an entire open-source platform, consisting of an OS, the open source Apache Spark application for data collection, and SystemML for data analysis. Some of the applications in IBM’s deep learning stack have been around for a number of years, such as SystemML and Apache Spark, while others will be entirely new. Nervana Systems also recently open-sourced its formerly proprietary deep learning software, Neon.

### TensorFlow
While new to the open source landscape, Google’s TensorFlow deep learning framework has been in development for years as proprietary software. It was developed originally by the Google Brain Team for conducting research in machine learning and deep neural networks. The framework’s name is derived from the fact that it uses data flow graphs, where nodes represent a computation and edges represent the flow of information – in Tensor form – from one node to another.

TensorFlow offers a good amount of documentation for installation, as well as learning materials/tutorials which are aimed at helping beginners understand some of the theoretical aspects of neural networks, and getting TensorFlow set up and running relatively painlessly.

Unlike any other framework, TensorFlow has the ability to do partial subgraph computation, which involves taking a subsample of the total neural network and then training it, apart from the rest of the network. This is also called Model Parallelization, and allows for distributed training.

It is worth noting that one of the Theano frameworks, Keras, supports TensorFlow. The author of Keras, François Chollet, has recently ported Keras to TensorFlow. This means the Keras framework now has both TensorFlow and Theano as backends. Keras is a particularly easy to use deep learning framework. Now, any model previously written in Keras can now be run on top of TensorFlow.

In terms of speed, TensorFlow is slower than Theano and Torch, but is in the process of being improved. Future releases will likely see performance similar to Theano and Torch.
ddd
Watchdog