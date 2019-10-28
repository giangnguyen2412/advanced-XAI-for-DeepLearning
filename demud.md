# Summary
The discovery of new or unusual observations within large data sets is a key element of 
the scientific process, since unexpected observations can inspire revisions to current knowledge and
overturn existing theories. Once an observation is identified as novel or anomalous, the next question is generally, “Why?” 
To investigate the anomaly, users need to know what properties of the observation caused it to be selected. 
For images, these properties might include color, shape, location, objects, content, etc. 
Authors of this paper propose a new method to select, visualize and explain the anomalous features in abnormal samples.

# Contributions
Novelty detection: This paper propose to detect novel images using DEMUD algorithm. 
This algorithm utilizes an SVD (Singular value decomposition) model, then the novelty of an image is estimated using Reconstruction 
error R.

<equation 1>

Where U is the current set of top K eigenvectors from the SVD of a set of already selected items and µ is the mean of 
all previously seen items. The items having the maximum R will be chosen for a set of similar items.
CNN features for Image Content Representation: Authors propagate images through a trained neural network (could be an auto-encoder or a
NN) trained on a large and diverse image dataset could be used.
Visualization of Explanations: Up-convolutional (UC) network is utilized for visualization. 
They intend to visualize DEMUD reconstruction and residual (not real images). This visualization provides image of what is expected and what is abnormal. 
Experiments show that this approach achieves strong discovery performance even in challenging datasets. 
This method could be used to better analysis and discovery in a variety of application areas.

# Possible improvement
There are two improvements could be made in this papers:
-	In novelty detection, they use SVD with top K eigenvectors; however, this value K is not particularly specified. I am assuming this is one hyper-parameter like K-means algorithm, so the K will affect the final results quite much.
-	Experimental part of this paper could be enhanced by using more advanced techniques to visualize CNN features.
