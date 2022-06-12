# This repository serves as my notebook in taking the [AWS DeepRacer Student](https://student.deepracer.com/home).

### Table of Contents

# Introduction to Machine Learning
Thanks to machine learning, exciting changes are happening across all areas of society, including:
- Recent advancements in industries such as autonomous vehicles.
- Accurate and rapid translation of the text into hundreds of languages.
- AI assistants you might find in your home.
- Worker safety improvements.
- Quicker pharmaceutical design and development.

Machine learning is a new field created at the intersection of statistics, applied math, and computer science. Because of the rapid and recent growth of machine learning, each of these fields might use slightly different formal definitions of the same terms.

## What is Machine Learning?
Machine learning is part of the broader field of artificial intelligence. This field is concerned with the capability of machines to perform activities using human-like intelligence. Within machine learning there are several different kinds of tasks or techniques:
- In **supervised learning**, every training sample from the dataset has a corresponding label or output value associated with it. As a result, the algorithm learns to predict labels or output values. We will explore this in-depth in this lesson.
- In **unsupervised learning**, there are no labels for the training data. A machine learning algorithm tries to learn the underlying patterns or distributions that govern the data. We will explore this in-depth in this lesson.
- In **reinforcement learning**, the algorithm figures out which actions to take in a situation to maximize a reward (in the form of a number) on the way to reaching a specific goal. This is a completely different approach than supervised and unsupervised learning. We will dive deep into this in the next lesson.

Nearly all tasks solved with machine learning involve three primary components:
- A machine learning model
- A model training algorithm
- A model inference algorithm

**Model training algorithms work through an interactive and iterative process.**

## Steps in Machine Learning
### 1. Define the problem
**Step 1: Define a very specific task**

Think back to the snow cone sales example. Now imagine that you own a frozen treats store and you sell snow cones along with many other products. 
You wonder, "How do I increase sales?" It's a valid question, but it's the _opposite_ of a very specific task. 
The following examples demonstrate how a machine learning practitioner might attempt to answer that question.
- **Question:** Does adding a $1.00 charge for sprinkles on a hot fudge sundae increase the sales of hot fudge sundaes?
- **Question:** Does adding a $0.50 charge for organic flavors in your snow cone increase the sales of snow cones?

**Step 2: Identify the machine learning task we might use to solve this problem**

**What exactly is a machine learning task?**

All model training algorithms, and the models themselves, take data as their input. Their outputs can be very different and are classified into a few different groups, based on the task they are designed to solve.
Often, we use the kind of data required to train a model as part of defining a machine learning task.

Two common machine learning task:
- Supervised learning
- Unsupervised learning

In **supervised learning**, there are two main identifiers that you will see in machine learning:
- A **categorical** label has a discrete set of possible values. In a machine learning problem in which you want to identify the type of flower based on a picture, you would train your model using images that have been labeled with the categories of the flower that you want to identify. Furthermore, when you work with categorical labels, you often carry out classification tasks, which are part of the supervised learning family.
- A **continuous** (regression) label does not have a discrete set of possible values, which often means you are working with numerical data. In the snow cone sales example, we are trying to predict the number of snow cones sold. Here, our label is a number that could, in theory, be any value.

In **unsupervised learning**, **clustering** is just one example. There are many other options, such as deep learning.

### 2. Build the dataset
**The most important step of the machine learning process**

Working with data is perhaps the most overlooked—yet most important—step of the machine learning process. In 2017, an O’Reilly study showed that machine learning practitioners spend 80% of their time working with their data.

**Data collection**

Data collection can be as straightforward as running the appropriate SQL queries or as complicated as building custom web scraper applications to collect data for your project. You might even have to run a model over your data to generate needed labels. Here is the fundamental question:

Does the data you've collected match the machine learning task and problem you have defined?

The quality of your data will ultimately be the largest factor that affects how well you can expect your model to perform. As you inspect your data, look for:
- Outliers
- Missing or incomplete values
- Data that needs to be transformed or preprocessed so it's in the correct format to be used by your model

Models can make assumptions about how your data is structured.

Now that you have some data in hand, it is a good best practice to check that your data is in line with the underlying assumptions of the machine learning model that you chose.

Using statistical tools, you can calculate things like the mean, inner-quartile range (IQR), and standard deviation. These tools can give you insights into the scope, scale, and shape of a dataset.

You can use data visualization to see outliers and trends in your data and to help stakeholders understand your data.

### 3. Train the model
The first step in model training is to randomly split the dataset.

This allows you to keep some data hidden during training, so that the data can be used to evaluate your model before you put it into production. Specifically, you do this to test against the bias-variance trade-off.

Splitting your dataset gives you two sets of data:
- **Training dataset:** The data on which the model will be trained. Most of your data will be here. Many developers estimate about 80%.
- **Test dataset:** The data withheld from the model during training, which is used to test how well your model will generalize to new data.

The model training algorithm iteratively updates a model's parameters to minimize some loss function.
- **Model parameters:** Model parameters are settings or configurations that the training algorithm can update to change how the model behaves. Depending on the context, you’ll also hear other specific terms used to describe model parameters such as weights and biases. Weights, which are values that change as the model learns, are more specific to neural networks.
- **Loss function:** A loss function is used to codify the model’s distance from a goal. For example, if you were trying to predict the number of snow cone sales based on the day’s weather, you would care about making predictions that are as accurate as possible. So you might define a loss function to be “the average distance between your model’s predicted number of snow cone sales and the correct number.” You can see in the snow cone example; this is the difference between the two purple dots.

The end-to-end training process is:
- Feed the training data into the model.
- Compute the loss function on the results.
- Update the model parameters in a direction that reduces loss.

Pragmatic problem solving with machine learning is rarely an exact science, and you might have assumptions about your data or problem that turn out to be false. Don’t get discouraged. Instead, foster a habit of trying new things, measuring success, and comparing results across iterations.

### 4. Evaluate the model
Model accuracy is a fairly common evaluation metric. _Accuracy_ is the fraction of predictions a model gets right.

Every step we have gone through is highly iterative and can be changed or rescoped during the course of a project. At each step, you might find that you need to go back and reevaluate some assumptions you had in previous steps. Don't worry! This ambiguity is normal.

### 5. Use the model
You're ready to deploy your model. Once you have trained your model, have evaluated its effectiveness, and are satisfied with the results, you're ready to generate predictions on real-world problems using unseen data in the field. In machine learning, this process is often called **inference**.

Even after you deploy your model, you're always monitoring to make sure your model is producing the kinds of results that you expect. There may be times where you reinvestigate the data, modify some of the parameters in your model training algorithm, or even change the model type used for training.

These steps are iterative. In practice, that means that at each step along the process, you review how the process is going. Are things operating as you expected? If not, go back and revisit your current step or previous steps to try and identify the breakdown.
The rest of the course is designed around these very important steps.

## Examples in Machine Learning
Supervised learning
- Using machine learning to predict housing prices in a neighborhood, based on lot size and the number of bedrooms.

Unsupervised learning
- Using machine learning to isolate micro-genres of books by analyzing the wording on the back cover description.

Deep neural network
- It can be used to analyze raw images from lab video footage from security cameras, trying to detect chemical spills.
