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

# Introduction to Reinforcement Learning
**In supervised learning**, every training sample from the dataset has a corresponding label associated with it, which essentially tells the machine learning algorithm what the training sample is. As a result, the algorithm can then learn from this data to predict labels for unseen data in the future.

In **unsupervised learning**, there are no labels for the training data. The machine learning algorithm tries to learn the underlying patterns or distributions that govern the data.

**Reinforcement learning** is very different to supervised and unsupervised learning. In reinforcement learning, the algorithm learns from experience and experimentation. Essentially, it learns from trial and error.

Reinforcement learning consists of several key concepts:
- Agent is the entity being trained. In our example, this is a dog.
- Environment is the “world” in which the agent interacts, such as a park.
- Actions are performed by the agent in the environment, such as running around, sitting, or playing ball.
- Rewards are issued to the agent for performing good actions.

## Reinforcement Learning with AWS DeepRacer
AWS DeepRacer is a 1/18th scale racing car, with the objective being to drive around a track as fast as possible. To achieve this goal, AWS DeepRacer uses reinforcement learning.

- The **agent** is the AWS DeepRacer car (or, more specifically, the software running on the car);
- The agent wants to achieve the goal of finishing laps around the track as fast as possible, so the track is the **environment**.
- The agent knows about the environment through the **state** which is the portion of the environment known to the agent. In the case of AWS DeepRacer, it is the images being captured by the camera.
- Once the agent knows its state in the environment, it can perform **actions** in the environment to help it achieve its goal. In the case of DeepRacer, this might be accelerating, braking, turning left, turning right, or going straight.
- The agent then receives feedback in the form of a **reward** about how well that action contributed towards achieving its goal.
- And all this happens within an **episode**. This can be thought of as a cycle of the agent performing an action in the environment (based upon the state it has observed) and then receiving feedback in the form of a reward which informs future actions it might take.

Creating a model in AWS DeepRacer Student is a six-step process:
- Name your model
- Choose track
- Choose algorithm type
- Customize reward function
- Choose duration
- Train your model

## Deep Dives
AWS DeepRacer offers two training algorithms:
- Proximal Policy Optimization (PPO)
- Soft Actor Critic (SAC)

A **policy** defines the action that the agent should take for a given state. This could conceptually be represented as a table - given a particular state, perform this action.

This is called a **deterministic policy**, where there is a direct relationship between state and action. This is often used when the agent has a full understanding of the environment and, given a state, always performs the same action.

Consider the classic game of rock, paper, scissors. An example of a deterministic policy is always playing rock. Eventually the other players are going to realize that you are always playing rock and then adapt their strategy to win, most likely by always playing paper. So in this situation it’s not optimal to use a deterministic policy.

So, we can alternatively use a **stochastic policy**. In a stochastic policy you have a range of possible actions for a state, each with a probability of being selected. When the policy is queried to return an action for a state it selects one of these actions based on the probability distribution.

This would obviously be a much better policy option for our rock, paper, scissors game as our opponents will no longer know exactly which action we will choose each time we play.

You might now be asking, with a stochastic policy how do you determine the value of being in a particular state and update the probability for the action which got us into this state? This question can also be applied to a deterministic policy; how do we pick the action to be taken for a given state?

Well, we somehow need to determine how much benefit we have derived from that choice of action. We can then update our stochastic policy and either increase or decrease the probability of that chosen action being selected again in the future, or select the specific action with the highest likelihood of future benefit as in our deterministic policy.

If you said that this is based on the reward, you are correct. However, the reward only gives us feedback on the value of the single action we just chose. To truly determine the value of that action (and resulting state) we should not only look at the current reward, but future rewards we could possibly get from being in this state.

This is done through the **value function**. Think of this as looking ahead into the future and figuring out how much reward you expect to get given your current policy.

Say the DeepRacer car (agent) is approaching a corner. The algorithm queries the policy about what to do, and it says to accelerate hard. The algorithm then asks the value function how good it thinks that decision was - but unfortunately the results are not too good, as it’s likely the agent will go off-track in the future due to his hard acceleration into a corner. As a result, the value is low and the probabilities of that action can be adjusted to discourage selection of the action and getting into this state.

This is an example of how the value function is used to critique the policy, encouraging desirable actions while discouraging others.

We call this adjustment a **policy update**, and this regularly happens during training. In fact, you can even define the number of episodes that should occur before a policy update is triggered.

In practice the value function is not a known thing or a proven formula. The reinforcement learning algorithm will estimate the value function from past data and experience.

### PPO vs SAC
The first thing to point out is that AWS DeepRacer uses both PPO and SAC algorithms to train stochastic policies. So they are similar in that regard. However, there is a key difference between the two algorithms.

**PPO** uses **“on-policy” learning**. This means it learns only from observations made by the current policy exploring the environment - using the most recent and relevant data. Say you are learning to drive a car, on-policy learning would be analogous to you reviewing a video of your most recent lesson and taking note of what you did well, and what needs improvement.

In contrast, **SAC** uses **“off-policy” learning**. This means it can use observations made from previous policies exploration of the environment - so it can also use old data. Going back to our learning to drive analogy, this would involve reviewing videos of your driving lessons from the last few weeks. Even though you have probably improved since those lessons, it can still be helpful to watch those videos in order to reinforce good and bad things. It could also include reviewing videos of other drivers to get ideas about good and bad things they might be doing.

So what are some benefits and drawbacks of each approach?
- PPO generally needs more data as it has a reasonably narrow view of the world, since it does not consider historical data - only the data in front of it during each policy update. In contrast, SAC does consider historical data so it needs less new data for each policy update.
- That said, PPO can produce a more stable model in the short-term as it only considers the most recent, relevant data - compared with SAC which might produce a less stable model in the short-term since it considers less relevant, historical data.

### Reward Functions
The purpose of the reward function is to issue a reward based upon how good, or not so good, the actions performed are at reaching the ultimate goal. In the case of AWS DeepRacer, that goal is getting around the track as quickly as possible.

So the logical question you might be asking is - "how does the reward get calculated and issued?". Well, this one is over to you - as you have control over the reward function, which is the piece of code that determines and returns the reward value.

In order to calculate an appropriate reward you need information about the state of the agent and perhaps even the environment. These are provided to you by the AWS DeepRacer system in the form of input parameters - in other words, they are parameters for input into your reward function.

There are over 20 parameters available for use, and the reward function is simply a piece of code which uses the input parameters to do some calculations and then output a number, which is the reward.

As a final tip, whenever you implement a reward function make sure you select the “Validate” button. This will check to make sure your reward function doesn’t have any errors that will prevent it from running. Note, this does not provide any assurances about how good your reward function might actually be in practice - it is simply a check to make sure there's no syntax errors.
