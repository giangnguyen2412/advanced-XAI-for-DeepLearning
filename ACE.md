# Towards Automatic Concept-based Explanations

## One-sentence summary

Detecting important concepts (which are represented by image segments) in a object class (i.e. police logi in police van of 1000-class ImageNet).

## Ideas and method


The outline of ACE algo is as follows:

![](https://github.com/luulinh90s/paper-review-interpretable-machine-learning/blob/master/images/ACE.PNG)

ACE takes a trained classifier and a set of
images of a class as input. It then extracts concepts present in that class and returns each concept’s
importance.

Fig a) starts with segmentation of the given class images (using a pretrained segmnetaion model to obtain segments of concepts (classes) from a set of images). They segmented at various resolution to obtain simple (black stripes) to complex (objects) concepts.
ACE uses SLIC network for segmentation task with three resolutions of 15, 50, and 80 segments for each image.

Fig b) groups similar segments as a concept and removes outliers. (using euclide distance for similarity and k-mean for clustering and removing outliers).

in Fig(c), concepts are given importance scores. ACE utilizes the TCAV score as a concept’s importance metric. 

By using this method, we can understand why a network gives a specific prediction. For instance, we could see that the network classifies
police vans using the van’s tire and the police logo.

![](https://github.com/luulinh90s/paper-review-interpretable-machine-learning/blob/master/images/ACE_exp1.PNG)

## Evaluation

### Human experiments

- They also conducted a human experiment to asses the *Coherency* and *Meaningfulness* of concepts. Details in Sec.4.

- They evaluated the *Importance* of concepts by the prediction accuracy on test examples as they add and remove important concepts.

