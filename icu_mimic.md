

# Summary
In today's hospitals, model interpretability is not only important but also necessary, since clinicians are 
increasingly relying on data-driven solutions for patient monitoring and decision-making. Thus, an important 
question naturally arises: how can we develop novel data-driven solutions which can achieve state-of-the-art performance
as deep learning models and at the same time can be easily interpreted by health care professionals and medical practitioners?
This paper introduces a simple yet effective knowledge-distillation approach called interpretable mimic learning,
to learn interpretable models with robust prediction performance as deep learning models. Unlike standard mimic learning, 
which uses shallow neural networks or kernel methods, this interpretable mimic learning framework uses gradient boosting trees (GBT) 
to learn interpretable models from deep learning models.
# Contributions
In this paper, authors introduce an interpretable mimic learning framework uses gradient boosting trees (GBT) 
to learn interpretable models from deep learning models. This framework is mainly based on knowledge distillation 
from Neural Networks. However, they use Gradient Boosting Trees (GBT) instead of another neural network as the student model since 
GBT satisfies our requirements for both learning capacity and interpretability. 
Gradient boosting machines are a method which trains an ensemble of weak learners to optimize a differentiable loss function by stages.
To model the dependency amongst learners, they propose to use Gated Recurrent Unit. The basic idea is that the prediction function 
F(X) can be approximated by a linear combination of several functions (under some assumptions), and these functions can be sought using
gradient descent approaches. The final model with M stages can be written as: <equation in 3.2>
 
They introduces two training procedures for mimic learning. Thanks to gradient boosting tree model, they achieve better interpretability than original deep model since they can study each feature's impact on prediction and, we can also obtain simple decision rules from the tree structures. Moreover, soft targets from the teacher deep learning model to avoid overfitting to the original data. 
Extensive experiments are conducted on Pediatric ICU dataset, and can identify features/markers important for mortality and ventilator free days prediction tasks.

# Possible improvement
1) For modeling the temporal modalities, they use GRU for more efficient computation. However, I think LSTM could be applied instead to achieve more robustness in structure and get a higher performance as LSTM provides us a memory unit more. 
2) In knowledge distillation, we could apply more advanced techniques of for distillation (in this paper they just use the conventional distillation strategy). More than that, distilling from intermediate layers could give a better result. Like in this paper (Incremental Learning Techniques for Semantic Segmentation), distilling from intermediate layers really outperforms distilling from the output layer.
