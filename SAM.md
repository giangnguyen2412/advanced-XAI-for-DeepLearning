# SAM: The Sensitivity of Attribution Methods to Hyperparameters

## Summary 

First, ML techniques often have a set of hyperparameters to be tuned empirically and most attribution methods
are not an exception. For example, window size (k) in PDA (Prediction Difference Analysis).

Second, aside from being faithful, an
explanation needs to be reproducible and invariant to arbitrary hyperparameter choices.

The problem can be reflected in the below image:

![](https://github.com/luulinh90s/paper-review-interpretable-machine-learning/blob/master/images/SAM1.JPG)

On 4 different attribution-based interpretability methods, they found that with different hyperparameters, they behaved
differently.

The main research question: How sensitive are attribution maps to their hyperparameters?

This paper has done a really good job in summarizing attribution-based methods (**Read section. 2**).

They propsed to evaluate the sensitivity to hyperparameters as an evaluation metric for attribution methods.
