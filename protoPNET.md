# This Looks Like That: Deep Learning for Interpretable Image Recognition

## Summary
This paper introduces a deep network architecture –
prototypical part network (ProtoPNet), that reasons in a way: the network dissects the image by finding prototypical parts, and combines evidence from the
prototypes to make a final classification.

The experiments show that ProtoPNet can achieve comparable accuracy
with its analogous non-interpretable counterpart, and when several ProtoPNets
are combined into a larger network, it can achieve an accuracy that is on par with
some of the best-performing deep models. In addition, this can provide good interpretation.

## My summary
We know what a standard image classifier looks like. Encoder + Decoder

Encoder is a feature extractor and Decoder will use these features to classify objects.

In this type of network, encoder stay unchanged, while decoder is replaced by a prototype layer g_{p}. When we have an image, the network will analyze each patch of this image,
then compute similarity score of this patch vs some prototypes (learned already in g_{p}). Then they combine similarity scores and give conclusion.

The schematic is as follows:

![](https://github.com/luulinh90s/paper-review-interpretable-machine-learning/blob/master/images/protoPNET.png)

The training algorithm is divided into three stages: 1) stochastic gradient descent (SGD) of layers before
the last layer; (2) projection of prototypes (where prototypes are learned); (3) convex optimization of last layer.
