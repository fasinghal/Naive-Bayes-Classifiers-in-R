# Naive-Bayes-Classifiers-in-R
CS6301: R For Data Scientists : Training Naive Bayes Classifiers in R

Classification Problems
We now turn our attention to classification problems …
In this setting, we have predictor variables as before (real, nominal, categorical),
but our response variable is categorical
We will often assume a binary response for now, but the methods we will explore
can work with multi-valued response variables
Most of these methods (often called classfiers) will rely on approximating a
probability for the (categorical) value of y, as opposed to approximating the value
directly
The method we look at here is Naïve Bayes, and (despite the name) is still a widely
used technique

Classification Problems - Notes
Classification problems tend to be easier to solve than regression problems
These come up in many situations (default vs no default, spam vs ham, win vs lose)
Often times it is a good idea to see if a regression problem can be converted to a
classification problem ….
◦ Instead of predicting the person’s age, can we predict adult versus child?
Suppose we are given data which is not labeled … can we still do a classification
problem?
◦ Yes – do clustering to find an optimal number of clusters, and assign cluster numbers to
the data points. Then build a classifier to predict the cluster a data point belongs to

Bayes Theorem
Recall from probability theory that Bayes Rule (or Bayes Theorem) related
onditional probabilities: If A and B are events, then
 P(B|A) = [ P(A|B) . P(B) ] / P(A)
 
 We often use the Law of Total probability to replace the P(A) term in the
denominator …
How can we use this to approximate a value for y? Idea: Given the training set, we
will try to approximate the probabilities for the values of y … then pick the value with
the largest probability

Bayes Optimal Classifier
Let’s state this more formally:
Suppose our response variable y takes on values {v1, v2, ... , vk} and we have n
predictors (this is the general case).
Suppose we are given a new predictor value a =< a1, a2, … ,an >, and suppose
each attribute is categorical. We want to find

max j { P(vj | < a1, a2 , ... an>)}
This is called the Bayes Optimal Classifier (or just Bayes Classifier)
 
Key assumption: The variables that make up the attribute tuple are conditionally independent, so
we can calculate the conditional probability as

 P(< a1, a2 , ... an> | vj) = Product over j { P(ai | vj) }

The “independence” assumption does not seem to hurt in practice
Naïve Bayes is a good classifier for larger data sets, because it tends to be fast
Another advantage – this approach is easy to evolve, since there is no model
◦ If data is changing or flowing, simply update the probabilities – do not use the entire
dataset to compute a model
Downside – not good at predicting response variables that depend on
combinations of predictors
