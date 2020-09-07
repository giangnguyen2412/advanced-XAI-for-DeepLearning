# Sanity Checks for Saliency Maps

Adebayo et al. (2018) explores when certain saliency
maps (a type of attribution-based explanation) fail to
reflect true feature importance. Specifically, they found
that certain attribution methods present visually identical explanations when a trained model’s parameters
are randomized (and hence features are made irrelevant
to prediction). This suggests that attribution methods
are making mistakes, perhaps by assigning high attributions to unimportant features (false positives) and
low attributions to important features (false negatives).
