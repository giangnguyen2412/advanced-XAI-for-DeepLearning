# Summary
Understanding why machine learning models behave the way they do helps users in model selection, feature engineering, and finally trusting the model to deploy it. In many cases even though a non-interpretable model is more accurate on the validation data set than the interpretable one, an interpretable model is chosen. But restricting the models to just an interpretable model isn't the best option.
The paper introduces a novel technique to explain the predictions of any classifier in an interpretable and faithful manner. It also proposes a method to explain models by obtaining representative individual predictions and their explanations.
The experiments are conducted mainly on text data and image data, where models used are Random Forest (RF) and Convolutional Neural Networks (CNN). The experiments highlight utility of explanations in deciding between the models, which model is to be trusted and which is not and also improving the model based on the explanations.
# Contribution
The main contributions of this paper are summarized as follows.

•	LIME, an algorithm to explain any prediction of any model (classifier or regressor) by approximating locally with an interpretable model that is faithful to the original model locally.

•	SP-LIME, a method to select a final set of representative samples using sub-modular optimization to show to the user that pretty much captures what the original model is doing globally.

•	Experiments with simulated subjects to prove the usefulness of LIME and SP-LIME.
# Comment
The paper contains new ideas and the authors clearly explain the approaches used with reasons as to why they picked it and also highlight both weaknesses and strong points of the approaches. It seems that LIME can easily extended to regression cases and is not just limited to classification tasks, but the paper doesn't discuss anything in this regard.
# Question
The authors don't say how locally faithful the interpretable model should be to the classifier with constraints on the maximum number of features to be used, i.e, what is the sort of error (mean squared error in case of linear interpretable models) we are content with?
Conclusion
This paper successfully argues for the importance of explaining the predictions to make the model more trustworthy to the user. It proposes LIME, a comprehensive approach to faithfully explain predictions of any model in the simplest way desired. Detailed experiments demonstrating how explanations helped users pick models or discard models are provided.
