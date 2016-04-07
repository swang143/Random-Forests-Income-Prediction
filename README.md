# Random-Forests-Income-Prediction

A random forest is a kind of ensemble model. Ensembles combine the predictions of multiple models to create a more accurate final prediction. It is the most powerful method to reduce decision tree overfitting. In this repository, we'll construct and apply random forests.

Again, we will use the dataset about United States individual income. The data is from the 1994 Census, and contains information on an individual's marital status, age, type of work, and more. What we want to predict, is whether they make less than or equal to 50k a year (0), or more than 50k a year (1).

When we choose models to construct the ensemble, the more diverse or dissimilar, the models are, the stronger the combined predictions will be (assuming that all models have about the same accuracy). Ensembling a decision tree and a logistic regression model, which use very different approaches, will result in stronger predictions than ensembling two decision trees with similar parameters.

A random forest is an ensemble of decision trees. If we don't make any modifications to the trees, each tree will be the exact same, so we'll get no boost when we ensemble them. In order to make ensembling effective, we have to introduce variation into each individual decision tree model. There are two main ways to introduce variation in a random forest -- bagging and random feature subsets.

Bagging: in a random forest, each tree isn't trained using the whole dataset. Instead, it's trained on a random sample of the data, or a "bag". This sampling is performed with replacement. 

Random feature subsets: we first pick a maximum number of features that we want to split the tree. Every time we split, we pick a random sample of features from the data. We then compute the information gain for each feature in our random sample, and pick the one with the highest information gain to split on. We're repeating the same process to select the optimal split for a node, but we'll only evaluate a constrained set of features, selected randomly. 
