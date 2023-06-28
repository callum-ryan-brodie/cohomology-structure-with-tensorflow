# cohomology-structure-with-tensorflow

Notebook(s) experimenting with implementations of machine learning algorithms to learn and extract the structure (regions and polynomials) of line bundle cohomology, as an exploration of alternatives to those architectures used in the paper [Machine Learning Line Bundle Cohomology](https://arxiv.org/abs/1906.08730).

--- 
* [example-two-hyperplane-case.ipynb](https://github.com/callum-ryan-brodie/cohomology-structure-with-tensorflow/blob/main/example-two-hyperplane-case.ipynb): Considers one of the simplest cases of a surface, a product of complex projective lines.
--- 

## Comments on the prototyping process

### Comments on the architecture

* While it is conceptually clear that fixing the weights which map the hyperplane logistic regression outputs to domain labels (i.e. the weights of the layer doms_hidden) leaves the model with enough flexibility to fit the data, in practice the result is that the model very frequently becomes stuck in a bad local minimum. Making these weights trainable results in far better performance.

### Comments on training
*  In this context there is a significant problem of falling into local minima. To help counter this we implement a variable learning rate.
