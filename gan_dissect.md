# Summary
How does a GAN represent our visual world internally? What causes the artifacts in GAN results? How do architectural choices affect GAN learning? Answering such questions could enable us to develop new insights and better models.

Authors present a general method for visualizing and understanding GANs at different levels of abstraction, from each neuron, to each object, to the contextual relationship between different objects. They first identify a group of interpretable units that are related to object concepts. Second, they directly intervene within the network to identify sets of units that cause a type of objects to disappear or appear (for example buildings have door but trees do not), since quantifying the causal effect of these units using a standard causality metric. Finally, authors examine the contextual relationship between these units and their surrounding by inserting the discovered object concepts into new images. Researchers study where they can insert object concepts in new images and how this intervention interacts with other objects in the image.
Also, they show several practical applications enabled by the framework, from comparing internal representations across different layers, models, and datasets, to improving GANs by locating and removing artifact-causing units, to interactively manipulating objects in the scene.

# Research questions
**Despite this tremendous success, many questions remain to be answered. For example, to produce a
church image (Figure 1a), what knowledge does a GAN need to learn? Alternatively, when a GAN
sometimes produces terribly unrealistic images (Figure 1f), what causes the mistakes? Why does one
GAN variant work better than another? What fundamental differences are encoded in their weights?**

**In this work, we study the internal representations of GANs. To a human observer, a well-trained
GAN appears to have learned facts about the objects in the image: for example, a door can appear on
a building but not on a tree. We wish to understand how a GAN represents such structure. Do the
objects emerge as pure pixel patterns without any explicit representation of objects such as doors and
trees, or does the GAN contain internal variables that correspond to the objects that humans perceive?
If the GAN does contain variables for doors and trees, do those variables cause the generation of
those objects, or do they merely correlate? How are relationships between objects represented?**

# My summary
The authors firstly identify the presence of class c in a representation (activation of a layer). If the class k found, they then try to remove - insert 
this class concept to the final image to dissect the causal effect to the final generation x. 

To find if the class k is in the representation or not, with an image, they do segmentation for class k, then calculate the IoU value between this segmentation and the 
upsampled-and-threholded feature map (from r). The top classes of k will be selected.

To remove-insert, they change the activation value of 0-the mean value of activation and observe the final generation.

# Contribution
This paper gives us huge understanding of GANs as well as compare, debug, modify, and reason about a GAN models. There is no theoretical contribution or any deep analysis since the paper presents a new methodological idea, which allows for nice practical contribution but it can help further researches to be significantly explicit and powerful.
# Comment
The paper is well-written and organized. The dissection and intervention for finding relationships between representation units and objects are simple, straightforward and meaningful. Almost representation focus on the generator, it provides a window into the internal mechanisms of a GAN.
# Conclusion
This is one of the first extensive studies that target the understanding and visualization of generative models. Focusing on the most popular generative model – Generative Adversarial Networks, it reveals significant insights about generative models. One of the main findings is that the larger part of GAN representations can be interpreted. It shows that GAN’s internal representation encodes variables that have a causal effect on the generation of objects and realistic images. This work provides a basis for analysis, debugging and understanding of Generative Adversarial Network models.
