# Summary
This paper propose a new method to better representation learning capacity for classification trees in neural networks (Deep neural decision forests – dNDF based on Random Forest algorithm). This novel algorithm introduces a stochastic, differentiable, and therefore back-propagation compatible version of decision trees, guiding the representation learning in hidden layers of deep networks. Unlike the traditional deep neural networks, a decision forest will provide the prediction in this new model. The performance of the approach is competitive with other state-of-the-art models built on Neural Network in classification task.
# Contributions
In this paper, there are some main contributions:
- Leveraging decision tree, they propose a new decision tree but using stochastic
routing instead of deterministic routing, enabling and end-to-end learning in deep
convolutional networks.
- To learn the decision node parametrization and the leaf predictions, they construct
an objective function. For updating decision node and leaf node parameters, they
use Stochastic Gradient Descent. In learning a forest, each tree can have a
different structure with a different set of decision functions, so they perform SGD
in trees sedately, reducing the computational load during training. At test time, they
average over tree predictions to produce the final outcome.
- The new decision forest model surpasses state-of-the-art when integrating it in the
GoogLeNet architecture without data augmentation.
# Possible improvement
They have replaced each Softmax layer from GoogLeNet with a forest consisting of 10 trees (each fixed to depth 15), resulting in a total number of 30 trees, as this architecture has 3 soft-max layers. However, when further architectures come, the number of trees will increase significantly, making training and inference slow because of a huge amount of computation. In addition, they choose 10 trees and 15 in depth, but no explanation for these parameters.
Experiments with other architectures should be conducted too see the efficacy on shallow/deep network.
Only CNN is considered in this research, I wonder the feasibility of this approach on RNN as we also have to perform decision making process.
