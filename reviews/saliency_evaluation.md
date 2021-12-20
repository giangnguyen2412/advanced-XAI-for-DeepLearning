# Evaluation of Saliency-based Explainability Methods

## One-sentence summary

This paper conducts extensive experiments to quantify the effectiveness of attribution methods both backpropagation-based and activation-based. 

## Ideas and method

Tested method:

(1) Saliency (Simonyan et al., 2013)

(2) GradCAM (Selvaraju et al., 2017)

(3) Contrastive Excitation Backprop (c-EBP)

(4) FullGrad (Srinivas & Fleuret, 2019):

(5) Integrated Gradients (IG) (Sundararajan et al., 2017)

(6) DeepLIFT (Shrikumar et al., 2017)

(7) Gradient SHAP (GradSHAP) (Lundberg & Lee, 2017)

(8) SmoothGrad (SG) (Smilkov et al., 2017)

Most of them are noisy and are gradient-based, so I am not sure how they can help users distinguish birds. Moreover, no perturbation-based methods were tested.

They used Animals with Attributes 2 (AWA2) and CUB-200 datasets. 

They have three tasks:

- Predictability: This measure also captures the class-discriminativeness of the generated explanations. Participants are presented with the explanations for the top- 4 predicted class for an image, including the explanation for the ground truth class. Shown in Fig. 1a.

- Reliability

- Consistency

## Evaluation