# Sanity Checks for Saliency Maps

Adebayo et al. (2018) explores when certain saliency
maps (a type of attribution-based explanation) fail to
reflect true feature importance. Specifically, they found
that certain attribution methods present visually identical explanations when a trained model’s parameters
are randomized (and hence features are made irrelevant
to prediction). This suggests that attribution methods
are making mistakes, perhaps by assigning high attributions to unimportant features (false positives) and
low attributions to important features (false negatives).

Our methodology derives from the idea of a statistical randomization test, comparing the natural
experiment with an artificially randomized experiment. We focus on two instantiations of our general
framework: a model parameter randomization test, and a data randomization test.

- **The model parameter randomization test** compares the output of a saliency method on a trained
model with the output of the saliency method on a randomly initialized untrained network of the
same architecture. If the saliency method depends on the learned parameters of the model, we should
expect its output to differ substantially between the two cases. Should the outputs be similar, however,
we can infer that the saliency map is insensitive to properties of the model, in this case, the model
parameters. In particular, the output of the saliency map would not be helpful for tasks such as model
debugging that inevitably depend on the model parameters.

- **The data randomization test compares a given saliency method applied to a model trained on a labeled data set with the method applied to the same model architecture but trained on a copy of the data set in which we randomly permuted all labels**. If a saliency method depends on the labeling of
the data, we should again expect its outputs to differ significantly in the two cases. An insensitivity to
the permuted labels, however, reveals that the method does not depend on the relationship between
instances (e.g. images) and labels that exists in the original data. 

Speaking more broadly, any explanation method admits a set of invariances, i.e., transformations
of data and model that do not change the output of the method. If we discover an invariance that is
incompatible with the requirements of the task at hand, we can safely reject the method. As such, our
tests can be thought of as **sanity checks** to perform before deploying a method in practice.

## Findings

- Gradients & GradCAM pass the sanity checks, while Guided BackProp & Guided GradCAM fail.
