# This repository serves as my notebook in learning Data Science.

In this learning process, I'll follow [Tina Huang](https://www.youtube.com/channel/UC2UXDak6o7rBm23k3Vv5dww)'s process of learning just enough, doing a project, and iterating it.

**In self studying, it is important to hold yourself accountable.**

These are the resources that I am following:
- I am following this GeekForGeeks' [How to Become Data Scientist – A Complete Roadmap](https://www.geeksforgeeks.org/how-to-become-data-scientist-a-complete-roadmap/).

### Table of Contents
[Introduction](#introduction)

[Machine Learning and Data Science Framework](#machine-learning-and-data-science-framework)
1. [Programming](#programming)
      - [Basics of Python](#basics-of-python)
      - [Python Data Science Libraries](#python-data-science-libraries)
      - [Databases](#databases)
2. [Mathematics](#mathematics)
      - [Statistics](#statistics)
      - [Linear Algebra](#linear-algebra)
      - [Calculus](#calculus)
      - [Probability](#probability)
3. [Data Visualization](#data-visualization)
4. [Exploratory Data Analysis](#exploratory-data-analysis)
5. [Machine Learning](#machine-learning)
6. [Data Scraping/APIs](#data-scrapingapis)
7. [Deep Learning](#deep-learning)

# Introduction
**What is Machine Learning?**
Machine Learning is the science of getting computers to act without being explicitly programmed. It is predicting results based on incoming data.

The harder things become to describe, the harder it is for us to tell machines what to do. Things that only humans can do and computers couldn't do before can now be done with Machine Learning. It makes machines act more and more like humans.

The process of training a Machine Learning Model is to feed inputs, train the machine to learn based on the input that we fed, so that it gives us an output the next time we feed a new input.

**Data Analysis vs Data Science**
Data Analysis is looking at a set of data and gaining an understanding of it by comparing different examples, different features, and making visualizations like graphs.

It asks the question of "What do they have in common?"

Data Science is running experiments on the set of data with the hopes of finding actionable insights within.

# Machine Learning and Data Science Framework
This framework will help you on how to think in solving problems. I used Daniel Bourke's [A 6 Step Field Guide for Building Machine Learning Projects](https://www.mrdbourke.com/a-6-step-field-guide-for-building-machine-learning-projects/) as a reference.

3 parts of Machine Learning:
## 1. Data Collection
### 1. Problem Definition
"What problem are we trying to solve?"

In this part, we should ask "Is it a Supervised or Unsupervised learning problem? and "Is it a Classification or Regression problem?"

When shouldn't you use machine learning?
- If coding can solve the problem.

Main Types of Machine Learning
#### Supervised Learning
Supervised Learning is used when you have data and labels. A machine learning algorithm tries to use data to predict a label. If it guesses it wrong, the algorithm corrects itself and tries again. This act of correction is why it's called supervise. A supervised learning algorithm repeats this process over and over again to make the model better.

There are two types of Supervised Learning, namely Classification and Regression.

**Classification** problems involves predicting if something is one thing or another. If there are only two options, it's called **Binary classification**. If there are more than two options, it's called **Multi-class classification**

**Regression** problems involve trying to predict a number which can go up or down, a continous number. It is commonly used in predictions such as the market value of a house.

**"I know my inputs and outputs."**

#### Unsupervised Learning
In Unsupervised Learning, you have the data but you don't have the labels. It uses patterns to create a label in which the data is classified.
- Transfer Learning
- Reinforcement Learning

**I'm not sure of the outputs but I have inputs.**

#### Transfer Learning 
Transfer Learning leverages what one machine learning model has learned in another machine learning. Although computers are very fast at making calculations, making calculations aren't free. So instead of reinventing the wheel, or starting from scratch, we can find a similar machine learning model and fine tune and adjust it to our problem.

**I think my problem may be similar to something else.**

#### Reinforcement Learning
Reinforcement Learning involves having a program perform some actions within a defined space and rewarding it for doing it well and punishing it for doing poorly. Although exciting and promising, Reinforcement Learning has yet to find its way to many practical applications.

### 2. Data
Data is a requirement for any machine learning project.

We should examine and ask "What kind of data do we have?", "Is it a Structure or Unstructured data?"

Data comes in many different shapes and sizes, but we can classify their types as **structured** and **unstructured**.

**Structured data** have all of the samples in similar format. They are commonly CSV's or Excel spreadsheets.

**Unstructured data** comes in varying format. They are things like images, natural language, transcribed phone calls, videos, and audio files.

Within these two data types, there's **static** and **streaming** data.

**Static data** is data which doesn't change over time. While **Streaming data** is data which is constantly changed over time.

### 3. Evaluation
"What defines success for us?"

In Evaluation, we define what success for the project means. It may come in the form of a percentage of machine learning model accuracy.

### 4. Features
"What do we already know about the data?"

### 5. Modelling
"Based on our problem and data, what model should we use?"

### 6. Experiments
"How could we improve/what can we try next?"

## 2. Data Modelling
## 3. Deployment


# Programming
## Basics of Python
- Variables
- Functions
- Loops
- OOP

## Python Data Science Libraries
- NumPy
- Pandas

## Databases
- SQL
- NoSQL

# Mathematics
## Statistics
- Mean
- Median
- Mode
- Variance
- Standard Deviation
- Correlation
- Distribution

What do these represent?

## Linear Algebra
- Vectors
- Matrices
- Matrices Operations

How to manipulate data using matrices?

## Calculus
- Derivatives

## Probability
- Odds
- Random Experiment
- Conditional Probability
- Bayes Theorem
- Normal Distribution
- Binomial Distribution
- Poisson Distribution

# Data Visualization
- Microsoft Excel
- Matplotlib
- Seaborn

# Exploratory Data Analysis
- Exploring a Data Set
- Are there missing data?
- How many variables are there?
- How many rows/cols do you have?
- Are there categorical and/or continous variables?
- What's the distribution of each variable?

# Machine Learning
## Supervised Learning
The data that will be fed into the machine already has categories.

In a Supervised Learning scenario, we can do Classification or Regression.

## Unsupervised Learning
The data that will be fed into the machine is unclassified or doesn't have groups and labels. We let the machine create these categories for us.

In a Unsupervised Learning scenario, we can do Clustering or Association Rule Learning.

- Semi-supervised

## Reinforcement Learning
In Reinforcement Learning, we are teaching the machine through trial and error and through rewards and punishment. It learns by interacting with the data millions of times to learn from the data that we fed and predict something.

In a Reinforcement Learning scenario, we can do Skill Acquisition or Real Time Learning.

- Logistic Regression
- Linear Regression
- Decision Tree
- Sci-kit Learn

# Data Scraping/APIs

# Deep Learning
- Artificial Neural Network
- Convolutional Neural Network
- Recurrent Neural Network
- TensorFlow

**Most of the initial resources and insights here are not mine. I will write down my input as I go about my learning.**
