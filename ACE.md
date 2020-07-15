# Towards Automatic Concept-based Explanations

## Summary

Most of the current explanation methods provide explanations through feature importance scores, which identify features that are important for each individual input.
However, how to systematically summarize and interpret such per sample feature importance scores itself is challenging.
In this work, they propose principles and
desiderata for concept based explanation, which goes beyond per-sample features
to identify higher level human-understandable concepts that apply across the entire
dataset. They develop a new algorithm, ACE, to automatically extract visual concepts.

## My summary

They devised Desiderata for a Concept-based Explanation. 1) Meaningfulness 2) Coherency 3) Importance

The outline of ACE algo is as follows:

![](https://github.com/luulinh90s/paper-review-interpretable-machine-learning/blob/master/images/ACE.PNG)

ACE takes a trained classifier and a set of
images of a class as input. It then extracts concepts present in that class and returns each concept’s
importance.

Fig a) starts with segmentation of the given class images. They segmented at various resolution to obtain simple (black stripes) to complex (objects) concepts.

Fig b) groups similar segments as a concept and removes outliers.

in Fig(c), concepts are given importance scores.

## I learned more

- In saliency maps, each pixel in every image is assigned an importance score for the correct
prediction of that image typically by using the gradient of prediction with respect to each pixel.
