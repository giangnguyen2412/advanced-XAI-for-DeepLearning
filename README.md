# This hub contains ADVANCED and PROMISING directions in XAI for Deep Neural Networks
There has been a lot of approaches to achieve interpretability in DL; however, there are only few research directions that are promising in 2021. Therefore, I only consider NEW and likely PROMISING directions here. 

## Categories

<!-- I took this picture from [Linardatos et al.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7824368/) to show how people are categorizing interpretability methods for Deep Learning smh.

![](images/IML_method_categorization.png) -->
Below is the layout of this hub:

- Network conceptualization

- Prototype-based explanations

- Inherently-interpretable DNNs

- Evaluation of explanations on down-stream tasks



Other categorizations are reasonable as well (i.e. from [Anh Nguyen](https://github.com/anguyen8/XAI-papers), [Molnar](https://christophm.github.io/interpretable-ml-book/taxonomy-of-interpretability-methods.html), or [lopusz](https://github.com/lopusz/awesome-interpretable-machine-learning)). However, I'd like to curate my own layout.

I also like this [distinction](https://www.youtube.com/watch?v=sl78EgrT4TY)(1:45) between Explainable ML and Interpretable ML by Rudin Cynthia.

### Network conceptualization
This line of research assigns human concepts to learned concepts of DNNs, which can make explanations more human-friendly and specific. Here I just picked a few representative papers, please contribute if any.


- <a name="todo"></a> Network Dissection: Quantifying Interpretability of Deep Visual Representations (**CVPR2017**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/reviews/Network_dissection.md)
- <a name="todo"></a> Interpretability Beyond Feature Attribution: Quantitative Testing with Concept Activation Vectors (TCAV) (**ICML2018**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/reviews/TCAV.md)
- <a name="todo"></a> Towards Automatic Concept-based Explanations (**NeurIPS2019**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/reviews/ACE.md)

### Prototype-based explanations
This line of research explains DNNs' decisions using the prototypes (or examples). Hence, it is inherently difficult to evaluate approaches quantitatively.

- <a name="todo"></a> This Looks Like That: Deep Learning for Interpretable Image Recognition (**NIPS2019**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/reviews/protoPNET.md)


### Inherently-interpretable DNNs
This line of research turns existing black-box DNNs (e.g. VGG or ResNet) into white-box models by altering and forcing them to behave in a human understandable manner.

- <a name="todo"></a> Stop explaining black box machine learning models for high stakes decisions and use interpretable models instead (**Nature Machine Intelligence**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/reviews/rudin_nature.md)
- <a name="todo"></a> Concept Whitening for Interpretable Image Recognition (**Nature Machine Intelligence**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/reviews/concept_whitening.md)
- <a name="todo"></a> Exploring the cloud of variable importance for the set of all good models (**Nature Machine Intelligence**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/reviews/cloud_variable.md)
- <a name="todo"></a> This Looks Like That: Deep Learning for Interpretable Image Recognition (**NIPS2019**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/reviews/protoPNET.md)

### Evaluation of explanations on down-stream tasks
As humans being the target end-users of explanations, this line of research investigates the actual effectiveness of explanations to humans in various decision-making tasks.

- <a name="todo"></a> The effectiveness of feature attribution methods and
its correlation with automatic evaluation scores (**arxiv2021**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/reviews/anhnguyen_effect.md)

- <a name="todo"></a> Explainable AI for Natural Adversarial Images (**ICLR2021**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/reviews/xai_adv_evaluation.md)

- <a name="todo"></a> Evaluation of Saliency-based Explainability Methods (**ICMLW2021**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/reviews/NA.md) 

- <a name="todo"></a> Quality Metrics for Transparent Machine Learning
With and Without Humans In the Loop Are Not Correlated (**ICMLW2021**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/reviews/NA.md) 

- <a name="todo"></a> How Can I Explain This to You? An Empirical Study of Deep Neural Network Explanation Methods (**NeurIPS2020**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/reviews/jeyakumar2020can.md)






<!-- ### 2021
- ICLR 2021
  - Attribution/saliency maps:
    - Decoy-enhanced Saliency Maps
    - Ablation Path Saliency
    - Variational saliency maps for explaining model's behavior
    - A-FMI: Learning Attributions from Deep Networks via Feature Map Importance

  - Evaluating visual explanation:
    - Exemplary Natural Images Explain CNN Activations Better than State-of-the-Art Feature Visualization
    - Evaluations and Methods for Explanation through Robustness Analysis
    - Investigating and Simplifying Masking-based Saliency Methods for Model Interpretability

- CVPR 2021

### 2020

- <a name="todo"></a> SAM: The Sensitivity of Attribution Methods to Hyperparameters (**CVPR2020**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/SAM.md) 
- <a name="todo"></a> Interpreting Latent Space of GANs for Semantic Face Editing (**CVPR2020**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/interfacegan.md) 
- <a name="todo"></a> Image Processing Using Multi-Code GAN Prior (**CVPR2020**) - [review ](https://github.com/luulinh90s/paper-review-generative-models/blob/master/mganprior.md) 
- <a name="todo"></a> Semantic Hierarchy Emerges in Deep Generative Representations for
Scene Synthesis (**arXiv**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/Hi_GAN.md) 
- <a name="todo"></a> Does the Whole Exceed its Parts? The Effect of AI Explanations on Complementary Team Performance (**arXiv**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/gagan1.md) 
- <a name="todo"></a> Shortcut Learning in Deep Neural Networks (**arXiv2020**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/shortcut_learning.md)
- <a name="todo"></a> Are Visual Explanations Useful? A Case Study in Model-in-the-Loop Prediction (**arXiv2020**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/chu_paper.md)
- <a name="todo"></a> How Useful Are the Machine-Generated Interpretations to General Users? A Human Evaluation on Guessing the Incorrectly Predicted Labels (**arXiv2020**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/shen_paper.md)


### 2019
Neural Networks
- <a name="todo"></a> GAN Dissection: Visualizing and Understanding Generative Adversarial Networks (**ICLR2019**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/gan_dissect.md) 
- <a name="todo"></a> This Looks Like That: Deep Learning for Interpretable Image Recognition (**NeurIPS2019**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/protoPNET.md) 
- <a name="todo"></a> Towards Automatic Concept-based Explanations (**NeurIPS2019**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/ACE.md)
- <a name="todo"></a> A Benchmark for Interpretability Methods in Deep Neural Networks (**NeurIPS2019**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/ROAR.md)
### 2018
- <a name="todo"></a> Generating Counterfactual Explanations with Natural Language (**ICML2018**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/counterfactual.md) 
- <a name="todo"></a> Interpretable Discovery in Large Image Data Sets (**ICML2018**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/demud.md) 
- <a name="todo"></a> Towards Providing Explanations for AI Planner Decisions (**IJCAI/ECAI2018**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/XAI-plan.md) 
- <a name="todo"></a> Learning to Explain: An Information-Theoretic Perspective on Model Interpretation (**ICML2018**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/L2X.md) 
- <a name="todo"></a> Anchors: High-Precision Model-Agnostic Explanations (**AAAI2018**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/anchors.md) 
- <a name="todo"></a> Benchmarking Attribution Methods with Relative Feature Importance (**arXiv2018**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/BAM.md) 
- <a name="todo"></a> Sanity Checks for Saliency Maps (**NeuRIPS2018**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/sanity_checks.md) 
### 2017
- <a name="todo"></a> Visualizing Deep Neural Network Decisions: Prediction Difference Analysis (**ICLR2017**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/evidence.md) 
- <a name="todo"></a> Interpretable Deep Models for ICU Outcome Prediction (**AMIA 2016**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/icu_mimic.md) 
### 2016
- <a name="todo"></a> Examples are not enough, learn to criticize! Criticism for Interpretability (**NIPS2016**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/MMD-critic.md) 
- <a name="todo"></a> The Mythos of Model Interpretability (**ICML2016**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/mythos.md) 
- <a name="todo"></a> Deep Neural Decision Forests (**IJCAI2016**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/forests.md) 
- <a name="todo"></a> InfoGAN: Interpretable Representation Learning by Information Maximizing Generative Adversarial Nets (**NIPS2016**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/info_gan.md) 
- <a name="todo"></a> "Why Should I Trust You?": Explaining the Predictions of Any Classifier (**arXiv**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/lime.md) 
### 2015
- <a name="todo"></a> Understanding Neural Networks Through Deep Visualization (**ICML2015**) - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/understandNN.md) 
### 2013
- <a name="todo"></a> Visualizing and Understanding Convolutional Networks - [review ](https://github.com/luulinh90s/paper-review-interpretable-DL/edit/master/deconvnet.md)  -->
