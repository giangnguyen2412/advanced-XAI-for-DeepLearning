# POST HOC EXPLANATIONS MAY BE INEFFECTIVE FOR DETECTING UNKNOWN SPURIOUS CORRELATION

## One-sentence summary
In training, [spurious correlations](http://lgmoneda.github.io/2021/01/12/spurious-correlation-ml-and-causality.html) are notorious and this paper investigate do these three XAI methods - attribution maps (AMs), concept activation, high-influence training samples - help humans detect these correlations.

## Ideas and method

### Scenario

> Consider a machine learning (ML) engineer whose job is to train DNN models to detect knee arthritis from radiographs. She—the engineer—is handed a trained ResNet-50 model, to be deployed in a hospital, that relies on a hospital tag in the radiographs to detect knee arthritis. She has no prior knowledge of the model’s reliance on the spurious tags. In this work, our key concern is whether the ML engineer can use post hoc explanations to identify that the model is defective.

### Tested methods

- Attribution maps: Input-Gradient, SmoothGrad, Integrated Gradients (IG), and Guided Backprop (GBP). 

- Concepts: Follow TCAV (Kim et al. 2018) where user-defined concepts are attributed from a prediction instead of pixels in images in AMs.

- Training Point Ranking via Influence Functions: This approach ranks the training samples in order of importance/influence on the loss (or prediction) of a test example.

## Evaluation

### Conclusion

From author:

> The setup comes equipped with a spurious score and performance measures for spurious signal detection. We find that the 3 classes of post hoc explanations tested are only sometimes able to diagnose the spurious training signal even if they are used to explicitly test for model dependence on these signals. Consequently, our findings calls for, potentially, a completely different paradigm of methods that are designed to address the important and challenging question of detecting spurious training signals.

This again shows that current XAI methods are pretty ineffective as shown in many down-stream tasks in prior works [(Nguyen et al. 2021)](https://arxiv.org/abs/2105.14944), [(Kim et al. 2021)](https://arxiv.org/abs/2112.03184), ... This is mainly due to the lack of rigorous evaluation in XAI. This problem is really hot than ever! 