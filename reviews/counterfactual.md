# Summary
To know why a class is classified, authors introduce a term “counterfactual explanation”. 
More particularly, to understand which attributes might change a classification decision if present in 
an image (e.g., “This is not a Scarlet Tanager because it does not have black wings.”). They perform changing 
colors on features of an images (wing color for example) rather than perturbing features which is not observable by human. 
They first determine discriminative phrases by inspecting the description of image. Once candidate counterfactual 
evidence has been extracted, they verify which counterfactual evidence is not present in the image using an evidence checker. 
Candidate counterfactual evidence which is not present in the image can be considered counterfactual evidence and is used to 
generate explanations. After determining candidate counterfactual evidence and determine possible counterfactual evidence with 
the evidence checker, they generate fluent textual explanations using a rule-based negation system and append the noun phrases 
to explanatory text which indicates which counter-class is being compared to.
# Contributions
-	Introduce a new procedure to explain the prediction of a classifier based on counterfactual sentences.
-	Propose two evidence checkers generating two different way of explanation for prediction: phrase-critic (based on positive and negative phrases) and classifier (based on combining visual features and textual feature, then predict a score indicating whether or not a phrase is in the image).
# Possible improvement
-	Chunking To determine candidate counterfactual evidence, is an important step but the tool is weak. Using more powerful extractor would improve the overall performance.
-	In case of we cannot extract all features for a class. For example, class cat, only extracting 4 legs, 1 tail and two ears, how this model can discriminate cat from dog? In an image, many features could be extracted.
-	The model relies mainly on an explanation model (Explanation generator), so the explanation could fail if wrong description is given from Explanation generator. This weak point should be improved.
-	In Figure 1, if there are some features has low probability, which feature should be picked to explain the prediction?  Choosing only one evidence with the minimum score seems not to be feasible.
