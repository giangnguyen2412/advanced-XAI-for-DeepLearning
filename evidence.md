# Summary
This article presents the prediction difference analysis method
for visualizing the response of a deep neural network to a specific input. 
When classifying images, the method highlights areas in a given input image that provide evidence for 
(removing it would decrease the confidence of the classifier in the given class) or against (increase) a certain class. 
The method introduced in this paper follows weight of evidence approach from Robnik-Šikonja & Kononenko (2008). 
The basic idea is that the relevance of a feature xi can be estimated by measuring how the prediction changes if the feature is unknown. 
A large prediction difference means that the feature contributed substantially to the classification, whereas a small difference 
indicates that the feature was not important for the decision. In weight of evidence approach, they use an assumption for 
approximation of p(xi|x\i); (assuming that feature xi is independent of the other features), but authors of this paper claim 
that this is very crude approximation especially with image data. In images for example, a pixel’s value is highly dependent 
on its neighbor pixels. For a pixel, we can find a square patch that contain the pixel satisfying the approximation (y_hat is the patch).
 
Several features could also be removed at once. It is not only interesting to analyze the input-output relation of the 
classifier, but also to look at what is going on inside the hidden layers of the network. Hence, authors propose activation 
difference to observe how the units of any layer of the network influence a node from a deeper layer.

* Conditional sampling: Instead of a crude approximation from Robnik-Šikonja & Kononenko (crude approx), authors use conditional sampling which is a better approximation method based on the relationships amongs consequent pixels in an image.
* Multivariate analysis: They also support removing multiple features from an image to see the changes in the prediction of the classifiser.
* Deep visulization: Activation map visualization of intermediate layers.
# Experiments
- We can see that conditional sampling leads
to results that are more refined in the sense that they concentrate more around the object. We can
also see that marginal sampling leads to pixels being declared as important that are very easily
predictable conditioned on their neighboring pixels (like in the saxophone example). Throughout our
experiments, we have found that conditional sampling tends to give more specific and fine-grained
results than marginal sampling. For the rest of our experiments, we therefore show results using
conditional sampling only.
# Contributions
-	Propose a new method visualizing deep neural networks by using a more powerful conditional, multivariate model.
-	The results provide insights for future research as showing which pixels of a specific input image are positive or 
negative against a node in the network.
# Possible improvement
-	How can we know exactly which k and l should be used? What is the effect when changing k and l?
-	In the algorithm, they use a sliding window of size kxk, but this greedy search will consume computation significantly. 
We can improve by applying better algorithm and shorten this searching.
