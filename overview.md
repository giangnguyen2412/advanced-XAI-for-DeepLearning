# My bird-eye views over IML on Neural Networks

## Back-propagation-based methods

Back-propagation-based methods calculate the gradient, or its variants, of a particular output with respect to the input using back-propagation to derive the contribution of features. In the simplest case, we can back-propagate the gradient[[33]](https://cacm.acm.org/magazines/2020/1/241703-techniques-for-interpretable-machine-learning/fulltext#R33). The underlying hypothesis is that larger gradient magnitude represents a more substantial relevance of a feature to a prediction. Other approaches back-propagate different forms of signals to the input, such as discarding negative gradient values at the back-propagation process[[34]](https://cacm.acm.org/magazines/2020/1/241703-techniques-for-interpretable-machine-learning/fulltext#R34), or back-propagating the relevance of the final prediction score to the input layer[[3]](https://cacm.acm.org/magazines/2020/1/241703-techniques-for-interpretable-machine-learning/fulltext#R3).

## Perturbation-based explanation methods

This line of work follows the philosophy that the contribution of a feature can be determined by measuring how prediction score changes when the feature is altered. It tries to answer the question: Which parts of the input, if they were not seen by the model, would most change its prediction? Thus, the results may be called counterfactual explanations. The perturbation is performed across features sequentially to determine their contributions and can be implemented in two ways: omission and occlusion. For omission, a feature is directly removed from the input, but this might be impractical since few models allow setting features as unknown. As for occlusion, the feature is replaced with a reference value, such as zero for word embeddings or specific gray value for image pixels. Nevertheless, occlusion raises a new concern that new evidence may be introduced and that can be used by the model as a side effect[[8]](https://cacm.acm.org/magazines/2020/1/241703-techniques-for-interpretable-machine-learning/fulltext#R8). For instance, if we occlude part of an image using a green color and then we may provide undesirable evidence for the grass class. Thus, we should be particularly cautious when selecting reference values to avoid introducing extra pieces of evidence.

## Source

- https://cacm.acm.org/magazines/2020/1/241703-techniques-for-interpretable-machine-learning/fulltext
