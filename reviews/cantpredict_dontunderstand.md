# What I Cannot Predict, I Do Not Understand: A Human-Centered Evaluation Framework for Explainability Methods

This paper is very close to [Giang's paper](https://arxiv.org/abs/2105.14944), from the research questions they raised and findings they obtained. I think there is a clear bridge between them. 

It is clear to me that attribution maps's effectiveness are ultimately unveiled. 

## One-sentence summary

This paper proposes a human-centered framework to evaluate attribution methods based on faithfulness (derived from [Deletion](https://proceedings.neurips.cc/paper/2019/file/fe4b8556000d0f0cae99daa5c5c5a410-Paper.pdf) paper).


## Ideas and method

The image below show their experiment:

![](https://github.com/luulinh90s/paper-review-interpretable-machine-learning/blob/master/images/fel_etal1.PNG)

In my own words, they first train users using a triple (image, explanation, AI's prediction) K times and then ask them to perform a **binary** classification task (e.g. Kit Fox vs. Red Fox).

The image below may capture the best their 3 tasks.

![](https://github.com/luulinh90s/paper-review-interpretable-machine-learning/blob/master/images/fel_etal2.PNG)


## Evaluation

For the metric, they use *Utility-K* score as equation (1). This metric is interesting as it not only presents the utility of attribution maps but the effectiveness of the size of training set to humans as well.

In equation (1):
```
We denote ψ(0) human meta-predictions after participants were trained on the same dataset but without explanations to offer baseline accuracy scores.
```

## Comparison with prior works

Here I show the similar/dissimilar things with Giang's. 

Similarities:

-- In Fig. 1, they said: **Surprisingly, the most faithful explanation (Saliency) seems more complex to grasp for a human observer and is likely to be of little use in real-life situations**. Meanwhile, in Giang's, we have: **We initially also tested vanilla Gradient [68], Integrated Gradient (IG) [72], and SHAP [44] methods
in a pilot study but discarded them from our study since their AMs are too noisy to be useful to users
in a pilot study** --> It is clear that **noisy** visualizations (e.g. IG) has very limited utility here.

-- They both focus on feature attribution maps.

-- They both found proxy (or surrogate -- faithfulness in this paper) metrics in attribution map evaluation correalte poorly with the actual utility.
	
Dissimilarities:

- This paper concerned about **Deletion score** while Giang et al. tried Localization error, Pointing game and IoU.

- Giang's proposed NNs as another direction of explaining models' behaviors.

- While Giang's and this paper together performed binary classification experiments, Giang's focused on how humans make decision given AI's predictions. This paper asked users to predict what AI is thinking. This is the major difference in their setups.

Findings: 

- Shown in Fig. 4, explanations do have noticeable utility for humans.
```
the explanation allows participants to better predict the model’s output (as the Utility scores are above 1).
```

- They found that *Integrated Gradients and Saliency are the worst explanations as both of them are significantly less useful than Grad-CAM*. This finding is totally aligned with Giang's as they found that **noisy** attribution maps have very minimal utility for humans.

- The Deletion score (or Faithfulness): the faithfulness score does not indicate how useful a method will be on the bias detection task. They quantify the correlation by looking at the ranking in Utility-K vs. Faithfulness.

- Explanations does not seem better than No explanations in ImageNet images (just two classes used in the paper). In ImageNet, they hardly can find the effectiveness of attribution maps.
```
ImageNet dataset, the set of methods tested (triangle marker) does not exceed 1.
```





