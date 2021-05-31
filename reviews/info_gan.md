# Summary
In this figure below, the input noise vectors of men with glasses are manipulated to give vectors that result in women with sunglasses. This indicates that there are structures in the noise vectors that have meaningful and consistent effects on the output of the generator.
 
However, there’s no systematic way to find these structures. The only thing affecting to the generator output is the noise input, so we have no idea how to modify the noise to generate expected images. This paper would like to come up with a disentangled representation to this problem. The idea is to provide a latent code, which has meaningful and consistent effects on the output. For instance, let’s say you’re working with the MNIST hand-written digit dataset. You know there are 10 digits, so it would be nice if you could use this structure by assigning part of the input to a 10-state discrete variable. The hope is that if you keep the code the same and randomly change the noise, you get variations of the same digit.
# Contributions
In this paper, they introduce InfoGAN which applies concepts from Information Theory to transform some of the noise terms into latent codes that have systematic, predictable effects on the outcome. The traditional objective function of GANs is modified my adding a regularization term.
 
The I(c;G(z,c)) term is the mutual information between the latent code c and the generator output G(z,c). They use an approximate lower bound using standard variational arguments to measure the mutual information. This give a new objective function like this:
 
In architecture, they propose a new architecture because a new second input to generator is introduced.
 
For experiments, they conduct on MNIST hand-written digit dataset. The authors specified a 10-state discrete code – c1 (hoping it would map to the hand-written digit value), as well as two continuous codes – c2 between -1 to +1. For comparison, they trained a regular GAN with the same structure but did not use the regularization term that maximizes the mutual information.
# Possible improvement
There are few improvements could be made for this paper:

•	The datasets used for experiments are such easy, I think experiments on more challenging datasets (3D object or others) should be conducted.

•	A problem of GAN is stabilization in training, this InfoGAN could be a promising option when we want to use pre-training for training a GAN. 

•	Gaussian mixture prior to help the model to learn a more spread latent space with less ambiguous areas, the authors may want to carefully define what is the ambiguous area
