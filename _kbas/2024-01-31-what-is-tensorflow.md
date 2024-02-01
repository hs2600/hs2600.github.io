---
layout: post
title:  What is TensorFlow?
date:   2024-01-31 00:00:00 -0800
description: Google's powerful open-source platform for machine learning.
author: horacio 
image:  '/images/tensorflow.png'
tags:   [technology]
tags_color: '#477690'
---

## Article Contents

[The Background](#the-background)

[How Does TensorFlow Work?](#how-does-tensorflow-work?)

[TensorFlow Use Cases](#tensorflow-use-cases)

[It’s All About Machine Learning](#its-all-about-machine-learning)

[Tensorflow Playground](#tensorflow-playground)

[TensorFlow](https://www.tensorflow.org/) is an open-source library, developed by Google, created for the specific purpose of numerical computation using data-flow graphs as its source. Two of the more important applications of TensorFlow are machine learning and deep neural networks research.

Unlike many libraries, TensorFlow works on just about every conceivable platform, from CPUs, GPUs, mobile and embedded devices, and Tensor Processing Units (specialized pieces of hardware that use tensor math).

**The Background**
------------------

TensorFlow was originally created as a deep learning project of the Google Brain Team. Since its inception, TensorFlow has been deployed across the entire Google ecosystem, in tools like:

*   Google Assistant
*   Google Photos
*   Gmail
*   Google search

And considering Google has the greatest machine learning infrastructure on the planet, it made sense for the company to be able to allow other businesses and developers to benefit from their platform. However, it wasn’t until TensorFlow was created that Google was able to share that vast platform. With the TensorFlow library of tools, any developer can add deep learning to their software.

**How Does TensorFlow Work?**
-----------------------------

TensorFlow uses a particular set of modules (which includes APIs for [Python](/blog/python-object-oriented-programming), C, and C++) to enable the construction and execution of TensorFlow computations. The data flow graphs that result from those computations are stateful, meaning that the program keeps track of the state of interaction.

To be more specific, TensorFlow sorts through layers of data, called Nodes, to uncover more and more complicated data about an image. As TensorFlow dives into deeper Nodes, it can ask more complicated questions.

For example: on the first node, it might recognize a round shape. As TensorFlow dives deeper, it might recognize the shape of an eye. Even deeper and that eye becomes feline. This process of input, that flows through layers of data up until the output is called a tensor.

The current iteration of TensorFlow allows you to write code that then builds a computational graph, which is a data structure that describes the computation you want to perform. There are a number of advantages to this process. For one, the graphs can be executed immediately or saved and later executed on numerous platforms. The graphs can also be deployed into a production environment without having to also deploy the building code. The only thing that is necessary is an available runtime that supports the TensorFlow graph.

Another advantage is that the TensorFlow graph can be easily optimized for any given platform. This makes it possible to train on a much larger platform and then transfer to a much less powerful platform (such as a mobile device).

**TensorFlow Use Cases**
------------------------

The application of TensorFlow is fascinating. With the help of tensors, an application, such as Google Photos, is able to accurately recognize locations in images. For example, Photos use it to spot a particular item in a photo (say, a bridge or a statue) and know exactly where that photo was taken. The TensorFlow-enabled application can then act on that new information.

All that can work like this: the application views a user’s images, spots the Empire State Building and knows the photo was taken in New York. The application can then display New York-specific advertisements to the user.

TensorFlow isn’t just limited to images. Another use case is voice and sound recognition. In fact, voice and sound recognition is one of the most widely used applications of TensorFlow. Google Assistant is the most obvious example, but there are other very important uses cases TensorFlow can be applied to, such as:

*   Image recognition
*   Object tagging videos
*   Self-driving cars
*   Sentiment analysis
*   Flaw detection
*   Text summarization
*   Mobile image and video processing
*   Air, land, and sea drones

### **The Components of TensorFlow**

TensorFlow has a number of pieces that come together to make the whole. Some of those pieces include:

### **TensorFlow.js**

Allows the use of standard JavaScript models and can build and train models directly in [JavaScript](/blog/scripting-languages#1-javascriptecmascript).

### **TensorFlow Federated**

An open-source framework for experimenting with machine learning, using decentralized data.

### **TF Privacy**

A library for training privacy-centric machine learning models.

### **tf.function**

Allows the transforming of a subset of Python syntax into portable, high-performance graphs.

### **TensorFlow Probability**

A Python library for the combining of probabilistic models and deep learning.

### **Tensor2Tensor**

A library of deep learning models and datasets.

**Its All About Machine Learning**
-----------------------------------

Machine learning is in everything. With the help of machine learning, devices continue to grow smarter and more efficient. Considering that data is the lifeblood of businesses, every company has become dependent on the information it provides. From customer data to B2B information (and everything in between), businesses have become profoundly reliant on data.

With the help of TensorFlow and machine learning, your business is better equipped to leverage the available data. That’s because it can help you to do the following:

*   Predict customer behaviors and purchasing patterns to help you refine your interactions with customers and better recommend products.
*   Predict machine maintenance needs.
*   Eliminate manual data entry.
*   Detect spam.
*   Analyze financial data.
*   Use images for data, pattern recognition, and database knowledge discovery.
*   Diagnose medical conditions.
*   Improve cybersecurity.

Imagine how challenging tackling all those issues would be without the help of machine learning—especially when big data is applied to the equation. Although you might be able to effectively handle some of those tasks with smaller amounts of data, once you’re dealing with thousands and hundreds of thousands of data points, making sense out of that data manually becomes impossible.

And predicting behavior? Unless your company has a data scientist on-hand, that’s a non-starter. In other words, for any reliable level of predictive computing, you need machine learning. And because TensorFlow was released with an open-source license, you can (with the right development team) integrate this incredible technology into your apps and systems.

**Tensorflow Playground**
-----------------------------------

Google’s TensorFlow [Playground](https://playground.tensorflow.org) is an interactive visualisation of neural networks. With it, you can simulate small neural networks in real-time in your browser, and see the results instantly.

Google’s TensorFlow Playground is an interactive visualisation of neural networks. With it, you can simulate small neural networks in real-time in your browser, and see the results instantly.

Here, we we will train your first little neural network and help to familiarise you with the concept of artificial neural networks (ANNs). 

### The concept of ANNs

The main purpose of this task is to explore a bit of what is happening inside the most famous machine learning algorithms and to understand how typical parameters influence learning.

### The Task:

#### 1. [Go to playground.tensorflow.org](https://playground.tensorflow.org)

#### 2. Settings

In the top part of the menu you’ll see the network hyperparameter (settings):

*   Learning rate; how fast the network learns
*   Activation function (a mathematic function – don’t worry, you can just try different ones if you like; ReLu learns fastest);
*   Epoch; the number of times that the ANN will work through the entire training dataset
*   Regularisation; ensures better training

#### 3. Data

*   Select the type of data you want to use from Data (on the left side) and the classification type problem
*   NB. There are four types of classification and two types of regression (regression means that one does not just predict classes, but also real values, e.g. the colour intensity in these examples).

#### 4. Increasing the number of neurons – Linear activation

*   Try increasing the number of neurons in the hidden layer from 1 to 2, and also try changing from a linear activation to a nonlinear activation like ReLU.\_\_

#### 5. Increasing the number of neurons – Nonlinear activation

*   Try increasing the number of neurons in the hidden layer from 2 to 3, using a nonlinear activation like ReLU.

#### 6. Adding or removing hidden layers

*   Continue experimenting by adding or removing hidden layers and neurons per layer. Feel free to change learning rates, regularisation and other learning settings.
