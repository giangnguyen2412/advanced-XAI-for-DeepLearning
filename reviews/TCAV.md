# Interpretability Beyond Feature Attribution: Quantitative Testing with Concept Activation Vectors (TCAV)

## One-sentence summary

This paper tried to answer a question: what is the importance degree to a prediction of a concept (i.e. human) in the input image.

## Ideas and method

The procedure is as follows:
![](/images/TCAV.png)

- First, we need to pick an interested concept (i.e. white-and-black stripe). Then, we collect a set of examples containing this **concept** (i.e. while-and-black stripe) and a set of random examples (e.g. cat, dog, or cactus...).

- Second, we will look for  a vector in the activation space of layer l that represents this concept. We find this vector by using a binary linear classifier which classifies the activations of two sets in the first step.

- **Ok so now a rising question is that, how can we determine the threshold which separate these two sets?** How do we train this linear classifier? What are the labels used for training? It remains a big question for me after reading this paper.

- Third, once we have the concept activation vector, we can compute the directional derivative (đạo hàm có hướng in Vietnamese) using the formula (1) in the paper. Its not so complicated.

- Last, the importance (or sensitivity as in paper) is measured using formula (2) in the paper, which can be understood as: **the fraction of k-class inputs whose l-layer activation vector was positively influenced by concept C** 

## Evaluation

