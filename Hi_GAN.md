# Semantic Hierarchy Emerges in Deep Generative Representations for Scene Synthesis

## My summary

Given a trained generator G, we start with a lot of latent codes c to generate a lot of synthesized images.
![](https://github.com/luulinh90s/paper-review-interpretable-machine-learning/blob/master/images/Hi_GAN1.PNG)

Then from the synthesized images, we can extract a lot of scene category and scene attributes: nature lighting, wood, foliage.

So the goal of this paper is to identify the causality b/w the random vector and predicted semantics.

How this paper works?

![](https://github.com/luulinh90s/paper-review-interpretable-machine-learning/blob/master/images/Hi_GAN2.PNG)

Firstly, from latext space, they sample latent code to generate images (synthesized image space). Secondly, they apply an
off-shelf classifier (indoor lighting/without indoor lighting classifier as in the above image).

After dividing into two attributes, they train an attribute classifier on latent space (input is latent code and label is to attributes). They 
only use a linear binary classifier for this task. After training, they have a boundary in latent space for natural lighting and indoor lighting.

![](https://github.com/luulinh90s/paper-review-interpretable-machine-learning/blob/master/images/Hi_GAN3.PNG)

They can push a latent code towards the boundary to change the attribute of the generated image. In the above image, when the latent code is being
pushed to the region of indoor lighting, the room is being brighten up.

Other attributes are also manipulated in the paper. Click for [more](https://arxiv.org/pdf/1911.09267.pdf).
