This paper proposes to interpret the given data by providing examples that can show
the full picture – majorities + minorities.

They present the MMD-critic, a scalable framework for prototype (representatives) and criticism (outliers) selection to improve
the interpretability of machine learning methods.

* Here majorities is the representatives for the dataset: 
`Some of the examples are prototypical of the entire population.` 
:arrow_forward: propotype
* Minorities could be ovserved as outliers
`Some of the examples are outliers.`
:arrow_forward:criticism

> However, examples are not enough. Relying only on examples to explain the models’ behavior
can lead over-generalization and misunderstanding. Examples alone may be sufficient when the
distribution of data points are ‘clean’ – in the sense that there exists a set of prototypical examples
which sufficiently represent the data. However, this is rarely the case in real world data. For instance,
fitting models to complex datasets often requires the use of regularization. While the regularization
adds bias to the model to improve generalization performance, this same bias may conflict with the
distribution of the data. Thus, to maintain interpretability, it is important, along with prototypical
examples, to deliver insights signifying the parts of the input space where prototypical examples do not provide good explanations. We call the data points that do not quite fit the model criticism
samples. Together with prototypes, criticism can help humans build a better mental model of the
complex data space.

Here **fitting models to complex datasets often requires the use of regularization** means when training, we add regularization to generalize both prototype and criticism then we can not see the real distribution of data.

Then now authors define `p` is the distribution for samples and `q` is the distribution for the dataset.
Selecting prototypes by minimizing MMD, and Selecting criticisms by maximizing - finding peaks in witness function.
**It is understandable as samples giving high MMD will far from the distribution of dataset => criticisms and vice versa**.

As the eq(2) in paper indicates, the *witness function* measures the maximum discrepancy between two expectations. This function is positive when Q underfits P, and negative wherever Q overfits P. Then we need to maximize (2) to separate the two expectations as far as possible. 

(2) is approximated as (5) using sample expectations.

Finally, we come up with the objective function (6). Optimizing this function allows us to correctly choose prototype and criticism. 
**Using both prototypes and criticisms was most effective in describing the distribution.**
