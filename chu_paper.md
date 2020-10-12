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
### Treatments
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

### Metrics
We measure and analyze four quantities: (1) the error of the user’s guess (the absolute value of the
difference between the guess and the ground-truth age label), (2) trust (quantified as the absolute
value of the difference between the guess and the model’s prediction), (3) the time spent making
the guess, and (4) answers to post-survey questions on how the model prediction was used in their
decision-making process and how reasonable the explanations seemed. 

## Analysis and Results
### How do model predictions and explanation quality affect model-in-the-loop accuracy?
#### Participants in the Empathetic, Show Top-3 Range, and Explain-strong treatments performed best and outperformed humans without AI.

The results are also a reminder of the importance of the design of the human-AI system, with
the Empathetic and Show Top-3 Range treatments equally or more effective as our explanationbased treatments. 

For example, the Empathetic
and Explain-strong treatments both increase trust, and it could be that the former does so through an
emotional approach while the latter does so through more logical means.

Improved accuracy is not attributable to the amount of time spent making guesses

#### The addition of explanations did not improve accuracy

indicate the limited utility of these explanations for
such a visual classification task. Survey responses indicate that participants did indeed examine the
highlighted areas and focus on important features such as location-specific wrinkles, but could not
extract information that would boost their performance.

It is possible that our results would change if users were extensively trained to interpret and use the
saliency maps, instead of only being presented with our short guide. We do note, however, that prior
work on training users to interpret saliency map explanations in a different task did not increase
performance when model predictions were also shown [26, 25]. We believe nevertheless that one
broader takeaway remains the same — designers of human-AI systems should question the utility of
pixel-level saliency explanations when designing ML-powered tools.

#### The quality of explanations had little effect on accuracy
This is likely related to how explanation quality had little
impact on the trust participants placed in the model predictions, discussed in the following section

### How does explanation quality affect human trust and understanding?
#### Faulty explanations did not significantly decrease trust in model predictions

These findings, coupled with the large differences in accuracy between the H+M- and H-M+ settings
and the decrease in accuracy in the H+M- setting (Figure 3), raise the question to what degree humans
can identify and ignore erroneous model predictions. For example, a model that is accurate 98% of
the time but makes large errors in the remaining 2% can be very dangerous in a high-stakes scenario
if humans default to trusting all model predictions

#### Most participants claimed that explanations appeared reasonable, even when they were obviously not focused on faces

Participants shown a strong explanation rated the explanations 5.37 / 7,
versus 5.05 and 4.71 for the spurious and random explanations.

### How did humans incorporate model predictions and explanations into their decision making process?

Responses to the post-survey question “How did you use
the model’s prediction in your decision-making process?”
provide some clues to the workings of our human-AI system. Participants in the Explain-random treatment did
highlight the randomness of the saliency maps, with one
saying “I took it slightly into consideration but didn’t
weight it heavily because it looked like the model was
picking inaccurate locations...”. However, many others
focused simply on the accuracy of the prediction, with one
stating “Well it did a poor job recognizing face or features
but the ages sound mostly correct so i sort of went with
it”. We again note, however, that faulty explanations did
not significantly decrease trust even in the presence of
inaccurate model predictions

We also examined responses for the top 75 guessers in terms of mean error, (collective MAE of 5.19).
Answers to how the model prediction was used were bucketed into 6 categories: (1) 10.3% ignored it,
(2) 17.9% considered it, (3) 5.1% used it if they were unsure, (4) 28.2% used the model prediction as
a starting point, (5) 21.8% had their own initial guess and adjusted based on the model prediction, (6)
9.0% used the model prediction if it seemed reasonable; otherwise gave their own guess.
