# Summary
Existing machine learning mismatches for the real-life tasks they are meant to solve
because simplified optimization objectives fail to capture our more complex real-life goals.
Another such divergence of real-life and machine learning problem formulations emerges
when the off-line training data for a supervised learner is not perfectly representative of
the likely deployment environment. This paper aims to prove a more careful and exact
definition of what is interpretability. Authors make a first step towards providing a
comprehensive taxonomy of both the desiderata and methods in interpretability research.
They argue that the paucity of critical writing in the machine learning community is
problematic. When they have solid problem formulations, flaws in methodology can be
addressed by articulating new methods.
# Contributions
There are some main contributions of this paper:
- Propose a comprehensive definition for interpretability through desiderate (trust,
causality, transferability, and informativeness) of research in explainable AI.
- Analyze properties of a model that make it interpretable (transparency,
simulatability, and decomposablity).
- Give insights of post-hoc interpretability (using text, visualization, example, or local
explanations). This serves as a brief overview of effort in X-AI domain now.
- Provide useful discussion for research:
o Linear models are not strictly more interpretable than deep neural networks.
o Claims about interpretability must be qualified.
o In some cases, transparency may be at odds with the broader objectives of
AI.
o Post-hoc interpretations can potentially mislead.
- Introduce future directions for research:
o The discrepancy between real-life and machine learning objectives could
be mitigated by developing richer loss functions and performance metrics.
o Expand this analysis to other ML paradigms such as reinforcement learning.
# Possible improvement
This is a purely literature paper as they do not have any formulas or algorithms, but it is
very nice paper covering critical points in explainable AI. However, this paper only covers
supervised learning paradigm.
Although they propose to scale this definition to Reinforcement Learning, they may miss
unsupervised learning. Another hot field in AI is Embodied AI, the question: “is this work
scalable” in AI basically? 
