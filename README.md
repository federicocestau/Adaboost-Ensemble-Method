# Adaboost-Ensemble-Method.
Adaboost was the first ensemble method. The core principle of AdaBoost is to fit a sequence of weak learners, such as decision stumps, on repeatedly modified versions of data. A decision stump is a decision tree that is only one level deep, i.e., it consists of only a root node and two (or more) leaves. Like Random Forest, we use CART as a base estimator inside the Adaptive Boosting algorithm.
Boosting iterations consist of applying weights to each of the training samples (observations). Initially, those weights are equal across all observations, so the first step trains a weak learner on the original data.
For each successive iteration, the sample weights are individually modified, and the learning algorithm is reapplied to the reweighted data. Those training examples that were incorrectly predicted at the previous step have their weights increased. Meanwhile, the ones that were correctly predicted have their weights decreased. Hence, each subsequent weak learner is thereby forced to concentrate on the examples missed by the previous ones.
In the end, combining all of the weak learners into a final prediction generates a much “flatter” distribution of predictions. This is because the algorithm deliberately reduced the weights on the most confident examples and shifted focus towards harder to classify ones. 
AdaBoost Limitation
The resulting “flat” probability distribution of AdaBoost is its main limitation. Depending on your use case, it may not be an issue for you. Say if you only care about assigning the correct class, then the prediction probability is less relevant.
However, if you care more about the probability itself, you may want to use Random Forest.
The core principle of AdaBoost is to fit a sequence of weak learners, such as decision stumps, on repeatedly modified versions of data. A decision stump is a decision tree that is only one level deep, i.e., it consists of only a root node and two (or more) leaves. 
Due to its simplicity of only trees with only one deep level there more advanced ensemble methods such as Gradient Boosting and its variations.
Gradient boosting and its variations accept trees with deeper levels, having models more robust for large dataset. 
In the case of AdaBoost, the shifting is done by UP-WEIGHTING observations that were misclassified before, while Gradient Boosting identifies the difficult observations by large RESIDUALS computed in the previous iterations.
