# Debugging Tests for Model Explanations

## One-sentence summary

This paper assesses explanation methods' ability to: detect spurious correlation artifacts (data contamination), diagnose mislabeled training examples (data contamination), differentiate between a (partially) re-initialized model and a trained one (model contamination), and detect out-of-distribution inputs (test-time contamination).

## Compare with prior works

This paper and [Giang's paper](https://arxiv.org/abs/2105.14944) are closely related. While Giang's was also trying to use attribution maps to help users debug OOD inputs (i.e. adversarial examples) in **test** time, Giang's additionally concerns about how attributions maps help users improve human accuracy in AI-human decision making. 

Same with Giang's, this paper strongly focuses on **feature attribution methods**.	

## Ideas and method

The idea of this paper is simple but yet novel when they taxonomized bugs that a model can encounter.

I do love this picture as it comprehend the possible bugs in a Machine learning system. In each phase, we have bugs.


![](https://github.com/luulinh90s/paper-review-interpretable-machine-learning/blob/master/images/bugs.PNG)

Let's go deeper into bugs:

--  Contamination bugs are caused by defects in the training data, either in the input features, the labels, or both. For example, a few incorrectly labeled data can cause the model to learn wrong associations. Another bug is a spurious correlation training signal. For example, consider an object classification task where all birds appear against a blue sky background. A model trained on this dataset can learn to associate blue sky backgrounds with the bird class; such dataset biases frequently occur in practice (Badgeley et al., 2019; Ribeiro et al., 2016).

-- Model Contamination bugs are caused by defects in the model parameters. For example, bugs in the code can cause accidental re-initialization of model weights.

-- Test-Time Contamination bugs are caused by defects in test-input, including domain shift or pre-processing mismatch at test time.

Table 1 of this paper presents more precisely the types of examples they used in experiments.

## Evaluation