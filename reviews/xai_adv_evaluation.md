# Explainable AI for Natural Adversarial Images

## One-sentence summary

Authors measured the effectiveness of a saliency-based and an example-based explanation (these two methods are newly introduced in this paper) on natural and [adversarial examples](https://arxiv.org/pdf/1907.07174.pdf).

## Ideas and method

### Ideas

### Method (experiment design)

- The size of samples: 89 input images from 30 classes

- Tested on 160 participants

- Experiment protocol was approved by an IRB of Rutgers University.

- In this paper' human task, they show the GT label to humans and ask humans to do binary classification between the GT label and another label. The definition of the two labels shown to humans is described here:

> We used these target images in a
two alternative forced choice task, where participants were **asked to predict the model classifications**.
The two options are referred to as the **target** category and the **alternative** category.

> For misclassified images the target category is the model prediction, and the alternative category is
the ground truth. For correctly classified images the target category is the model’s predicted category,
and the alternative category is the category most confusable with the target category, according to
the confusion matrix constructed on ResNet-50’s predictions on the standard ImageNet’s validation
set.

## Evaluation

