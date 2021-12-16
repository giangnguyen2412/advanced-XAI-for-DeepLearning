# HIVE: Evaluating the Human Interpretability of Visual Explanations

## One-sentence summary

This paper investigates the how explanations from 4 methods (2 attribution maps and 2 example-based) were perceived by users and they found that participants humans generally can not leverage existing visual explanations from AI.

## Ideas and method

This work closely resembles [Giang's](https://arxiv.org/abs/2105.14944) and [Fel's](https://arxiv.org/abs/2112.04417).

Like Giang's, they also conducted experiments on both attribution maps and example-based explanations. The four investigated methods are: ```GradCAM, BagNet, ProtoPNet, and ProtoTree``` where ``GradCAM and BagNet`` are attribution maps which were extensively investigated in Giang's.

- GradCAM: Activation-based method

- BagNet: Active attention method as defined in [this paper](https://arxiv.org/abs/2107.07013).

- ProtoPNet and ProtoTree: Prototype-based method

- ProtoTree: Each node in the tree contains a prototype which comes from a training image. At each node, the model compares a given test image to the node’s prototype and produces a similarity score. If the score is above a threshold, the model judges that the proto- type is present in the image and absent if not. The model then proceeds to the next node and repeats this process until it reaches a leaf node, which corresponds to a class.


### Task design

This paper uses ImageNet and CUB200 datasets for human studies.

In general, they have two tasks:

- Distinction: distinguish between correct and incorrect explanations. This setup is somewhat similar to [Giang's]() where they asked users to make decision based on AI prediction. 

```
In our first task, a participant is shown an image along with several explanations corresponding to dif- ferent possible outputs (e.g., different class labels in object recognition) and the goal is to distinguish the correct pre- diction from incorrect ones based on provided explanations.
```

They actually have 4 options for each trial, then the baseline here is 25%.


- Agreement: do you agree with the explanation? This task is to see if users agree with AI's explanations, which will be useful if users fail the ```Distinction``` task.


## Evaluation

There are key findings:

1. Participants struggle to distinguish between correct and incorrect explanations for all four methods. This suggests that interpretability works need to improve and evaluate their ability to identify and explain model errors.

2. Participants tend to believe explanations are correct (regardless of if they are actually correct) revealing an issue of confirmation bias in interpretability work. Prior works have made similar observations for non-visual interpretability methods; however, we substantiate them for visual explanations and demonstrate a need for falsifiable explanations in computer vision.

3. We quantify prior work's anecdotal observation that similarity of prototypes in prototype-based models are not consistent with human similarity judgements.

4. Participants prefer a model with an explanation over a baseline model. Before switching their preference, they require a baseline model to have higher accuracy (and by a greater margin for higher-risk settings).