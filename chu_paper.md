# Are Visual Explanations Useful? A Case Study in Model-in-the-Loop Prediction

## Summary

- We present a randomized controlled trial for a model-in-the-loop regression task,
with the goal of measuring the extent to which (1) good explanations of model
predictions increase human accuracy, and (2) faulty explanations decrease human
trust in the model.

- We include in our experiments both faithful explanations of a
high-quality model, via integrated gradients [40], and a variety of “faulty explanations”—saliency
maps from a model trained on data with spurious correlations and completely uninformative random
explanations, as shown in Figure 1. We find that neither faulty explanations nor accurate ones
significantly affect task accuracy, trust in the model predictions, or understanding of the model.

- We include in our experiments both faithful explanations of a
high-quality model, via integrated gradients [40], and a variety of “faulty explanations”—saliency
maps from a model trained on data with spurious correlations and completely uninformative random
explanations, as shown in Figure 1. We find that neither faulty explanations nor accurate ones
significantly affect task accuracy, trust in the model predictions, or understanding of the model.

## Experimental design
### Task
Users are shown images from the validation and test of the APPA-REAL dataset [14], which contains
7,591 images with real age labels. We sample images uniformly across ages, and many images are
seen by multiple users. We also balance the dataset shown to users by combining equal proportions
of images for which the model is more accurate than previously collected human guesses (available
in the APPA-REAL data), and vice versa. 
## Treatments
- Baseline treatments Our two main baselines are (a) the Control treatment, in which the user
guesses without the help of the model, and (b) the Prediction treatment, in which the user guesses
with the model prediction shown but without an explanation shown.

- Explanation-based treatments These treatments show explanations in addition to the model
prediction. Our explanations are pixel-wise importances, or saliency maps, calculated using integrated
gradients. Explanations of varying quality are shown in Figure 1. In addition to the strong explanations, we also
tested two versions of lower quality saliency maps. Importantly, these varying explanations are all
shown with predictions from the same strong model, which isolates the effect of the explanation. 1) Explain-strong 2) Explain-spurious 3) Explain-spurious

- “Algorithmic aversion” refers to human loss of trust in a model after seeing it make a mistake [12, 47].

- Design-based treatments We also compare against existing and novel design-based treatments,
which vary the description of the model and the way the model’s predictions are shown. We are
interested in whether these simple framing approaches can be as effective at increasing accuracy or
trust as explanation-based treatments. The Delayed Prediction treatment tests the effect of anchoring
bias [22] and was previously shown to work well for improving accuracy in [17]. We record the initial
guess, show the model prediction, then ask for a final guess. The Empathetic treatment personifies
the model as an AI named Pat, shown in Figure S1 in the appendix

## Metrics
We measure and analyze four quantities: (1) the error of the user’s guess (the absolute value of the
difference between the guess and the ground-truth age label), (2) trust (quantified as the absolute
value of the difference between the guess and the model’s prediction), (3) the time spent making
the guess, and (4) answers to post-survey questions on how the model prediction was used in their
decision-making process and how reasonable the explanations seemed. 
