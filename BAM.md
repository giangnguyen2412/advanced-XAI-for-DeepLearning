# Benchmarking Attribution Methods with Relative Feature Importance

## Summary 

- Despite active development,
quantitative evaluation of feature attribution
methods remains difficult due to the lack of
ground truth: we do not know which input
features are in fact important to a model. Our evaluation on several widelyused attribution methods suggests that certain methods are more likely to produce false
positive explanations—features that are incorrectly attributed as more important to model
prediction.

- Just because an explanation makes
sense to humans does not mean that it is correct. For instance, edges of an object in an image could be visually appealing but have nothing to do with prediction. 
One way to test false positives is to identify unimportant features and expect their attributions to be zero.

- The idea of this paper is: For
instance, if we paste a gray square to every training
image for all classes, we expect this square to matter
less to model predictions than the original image region being covered. The same expectation should hold
if we instead paste a dog to every image (given that
the original images do not contain anything similar to dogs). As a result, any explanations that assign higher
attributions to dogs than to original pixels covered
by dogs are false positives. False positive attributions
of dogs have a higher chance of misleading humans
because dogs are semantically meaningful.
