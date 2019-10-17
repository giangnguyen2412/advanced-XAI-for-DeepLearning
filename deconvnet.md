# Summary
Despite of breakthroughs in image classification thanks to using Convolutional Neural Networks (CNN) over the past decade, we have no idea of how and why CNNs work. In this paper, they propose a multi-layered Deconvolution Network (deconvnet) to inversely map the feature activations to pixel space. They also provide a sensitivity analysis to point out which regions of an image affect to decision making process the most. Generalization is also studied in this work to see how well a model works on another dataset.
# Contributions
In this work, authors introduce a novel approach to map features at intermediate layers back to the input pixel space. 
By doing this, we can see exactly which pixels cause a given activation. In previous paper, a deconvnet works by using the same 
components (pooling layers, filtering units) to a CNN but reversely, mapping output to input. More than that, they place a 
deconvnet at each layer of a convent, so we can continuously trace back the path without skipping any layers. 
After that, they perform un-pooling, rectification, and filtering to rebuild the activity of the previous layer. 
The process continues until we complete with the first layer. For un-pooling, rectification, and filtering, they 
use different techniques to achieve operations (record the locations of maxima for un-pooling, use transposed versions of the same filters).
They shows visualizations after training and evolution of features during training providing insights to how a 
CNN works and change during training. 
Occlusion sensitivity is as well examined as they gradually occlude the object in the image, showing that the model truly localizes the object within the scene, not by surrounding context.
Generalization study reveals that model trained on ImageNet can efficiently extract features from other datasets like Caltech, but less well to the PASCAL data because of dataset bias.
# Possible improvement
There are few improvements could be done in this paper:
-	They only verify the generalization of model trained on ResNet with other smaller datasets, 
so verification on larger datasets should be conducted to study how smaller dataset can help generalize bigger datasets.
-	This visualization method in this paper only focuses on a single activation, hence we can propose a new method to 
visualize the join activity within the network leveraging deconvnet.
