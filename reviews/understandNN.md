
# Summary
In this paper, authors introduce 2 tools for understanding Deep Neural Networks; 
the first one is for plotting the activations produced on each layer of a trained DNN;
and the second one is to visualize learned features by each individual neuron. The first tool simply 
plots the activation values for the neurons in each layer of a convnet in response to an image or video. T
he second tool works like this to find the synthetic images causing largest activations: First, when images comes, 
it will find an image x* in which it maximizes this equation: 

equation 1 of paper
 
Where ai(x) is the activation of the image x on neuron i (an index that runs over all units on all layers). 
Rθ is the regularization term. Then, using gradient descent, we can compute x.

equation 2
 
Lastly, they try 4 different types of regularization to find expected images. 
Shortly, authors are trying to find an input image that maximally activates a given unit or class score 
to visualize what the network is looking for.
# Contributions
The main contributions of this paper is as:
-	Provide a live, interactive visualization of every neuron in a trained convnet as it responds to a user-provided image or video.
-	Add several new types of regularization, which produce more fine-grained interpretability for images.
-	From the tools, insights could be gained for future research such as (representations on some layers seem to be surprisingly local; for example, detectors for text, flowers, fruit, and faces on conv4 and conv5 or the DNNs are very sensitive on the last layers with small changes – which is vulnerable against adversarial attack; last layers are sensitive to small input changes, much of the lower layer computation is more robust and durable).
# Possible improvement
-	The first tool seems straightforward but the second tool is not clearly explained in this paper although the method is really interesting and novel.
-	The tools could give summarization about observation (which neurons are most active? Which layers should be transferred or clusters of dataset representative) rather than only visualization. I think the tools could be greatly improved.

# Highlights
1)	An oft-cited reason for the vulnerability of DNNs is that discriminative training leads networks to ignore non-discriminative information in their input, e.g. learning to detect jaguars by matching the unique spots on their fur while ignoring the fact that they have four legs.
2)	Representations on later convolutional layers tend to be somewhat local

