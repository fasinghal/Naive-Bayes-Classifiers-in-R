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
 
 
