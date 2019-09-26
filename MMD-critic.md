This paper proposes to interpret the given data by providing examples that can show
the full picture – majorities + minorities.

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

Then now authors define `p` is the distribution for prototype and `q` is the distribution for criticism.
The idea is if we can maximize the difference between `p` and `q`, 

**Using both prototypes and criticisms was most effective in describing the distribution.**
