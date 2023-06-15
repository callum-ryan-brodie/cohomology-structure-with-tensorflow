# cohomology-structure-with-tensorflow
Neural networks for learning the region and polynomial structure of line bundle cohomology

## Comments on the prototyping process

### Comments on the architecture

* While it is conceptually clear that fixing the weights which map the hyperplane logistic regression outputs to domain labels (i.e. the weights of the layer doms_hidden) leaves the model with enough flexibility to fit the data, in practice the result is that the model very frequently becomes stuck in a bad local minimum. Making these weights trainable results in far better performance.

### Comments on training
*  To avoid local minima we also implement a variable learning rate.
