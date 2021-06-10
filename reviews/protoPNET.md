# This Looks Like That: Deep Learning for Interpretable Image Recognition

## One-sentence summary
This paper introduces a deep network architecture – prototypical part network (ProtoPNet), or more precisely, they add **a NEW prototype layer** to existing deep network architectures (e.g. VGG or ResNet), which makes case-based reasoning and exposes network interpretability.

## Ideas and method
We know what a standard image classifier looks like. Encoder + Decoder

Encoder is a feature extractor and Decoder will use these features to classify objects.

In this type of network, encoder stay unchanged, while decoder is replaced by a prototype layer g_{p} and a last FC layer. When we have an image, the network will analyze each part of this image (segment), then computes similarity score of this patch vs some prototypes (**these prototypes and weights of the prototype layer are learned during training**). Then they combine scores to make the predictions.

The schematic is as follows:

![](https://github.com/luulinh90s/paper-review-interpretable-machine-learning/blob/master/images/protoPNET.png)


The prototypical patches are learned by a clustering algorithm included in the first Equation of 2.2. The step 1 of the training algo finds prototypes, while step 2 will update these prototypes.


## Evaluation
They found that when adding the new prototype layer, the accuracy on deep networks (e.g. DenseNet and ResNet) does not drop but even increase. Therefore, we achieve both high prediction performance + interpretability.

So far, we always believe that there is a trade-off between performance vs. interpretability -- especially with Deep neural networks (i.e. [here](https://medium.com/@erdemkalayci/the-tradeoff-in-machine-learning-accuracy-vs-explainability-fbb13914fde2) -- but this argument was countered by this paper and also a talk by [Rudin](https://www.youtube.com/watch?v=sl78EgrT4TY) (one author of this paper).